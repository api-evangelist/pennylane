---
name: Create and send a customer invoice
description: Create a draft customer invoice in Pennylane, finalize it, and email it to the customer.
api: openapi/pennylane-openapi.yml
operations: [getMe, postCustomerInvoices, finalizeCustomerInvoice, sendByEmailCustomerInvoice]
---

# Create and send a customer invoice

Use the Pennylane Company API v2 to draft, finalize, and deliver a sales invoice.

## Prerequisites
- A Bearer token (Company API token, Firm API token, or OAuth 2.0 access token with `customer_invoices:all`).
- Base URL: `https://app.pennylane.com/api/external/v2`.
- All amounts are in EUR. Company address, bank details, logo, and invoice numbering must be configured in the app before invoicing.

## Steps
1. **Confirm context** — call `getMe` (`GET /me`) to verify the token and which environment (sandbox or production) you are in.
2. **Create the draft** — call `postCustomerInvoices` (`POST /customer_invoices`) with the customer reference and line items (products from the catalog). This returns a draft invoice.
3. **Finalize** — call `finalizeCustomerInvoice` to lock the invoice and assign its legal number. Once finalized it cannot be edited.
4. **Send** — call `sendByEmailCustomerInvoice` to email the finalized invoice to the customer. If you get `409 Conflict`, the PDF is not yet generated — retry after a short delay.

## Rules
- Idempotency is NOT provided: do not blindly retry `postCustomerInvoices` on a network error; re-list and match by your own reference to avoid duplicates.
- Respect the rate limit: 25 requests / 5 seconds per token; honor `retry-after` on `429`.
- On `422`, read the `details` object in the error envelope for field-level validation messages.
