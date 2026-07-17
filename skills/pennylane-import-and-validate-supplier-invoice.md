---
name: Import and validate a supplier invoice
description: Import a supplier (accounts-payable) invoice into Pennylane, update it, and validate its accounting.
api: openapi/pennylane-openapi.yml
operations: [importSupplierInvoice, getSupplierInvoice, putSupplierInvoice, validateAccountingSupplierInvoice]
---

# Import and validate a supplier invoice

Bring an accounts-payable document into Pennylane and post it to the ledger.

## Prerequisites
- Bearer token with `supplier_invoices:all` access.
- Base URL: `https://app.pennylane.com/api/external/v2`.

## Steps
1. **Import** — call `importSupplierInvoice` (`POST /supplier_invoices/import`) with the invoice file/payload. Pennylane extracts the supplier and amounts.
2. **Review** — call `getSupplierInvoice` (`GET /supplier_invoices/{id}`) to read the parsed result.
3. **Correct** — call `putSupplierInvoice` to fix supplier, category, or ledger allocations as needed.
4. **Validate accounting** — call `validateAccountingSupplierInvoice` to finalize the accounting entries once the data is correct.

## Rules
- Ids are internal Pennylane integers (v2 removed `source_id`).
- On `422`, inspect `details` for the field(s) that failed validation before re-validating.
- Rate limit: 25 req / 5 s per token.
