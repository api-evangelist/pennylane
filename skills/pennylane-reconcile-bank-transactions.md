---
name: Reconcile bank transactions to invoices
description: Pull banking transactions and match them to the customer invoices they pay, then mark the invoices paid.
api: openapi/pennylane-openapi.yml
operations: [getTransactions, getCustomerInvoices, postCustomerInvoiceMatchedTransactions, markAsPaidCustomerInvoice]
---

# Reconcile bank transactions to invoices

Automate payment matching between Pennylane banking transactions and customer invoices.

## Prerequisites
- Bearer token with banking and `customer_invoices:all` access.
- Base URL: `https://app.pennylane.com/api/external/v2`.

## Steps
1. **List transactions** — call `getTransactions` (`GET /transactions`), paging with the opaque `cursor` until no next cursor is returned.
2. **Find candidate invoices** — call `getCustomerInvoices` (`GET /customer_invoices`) filtered by amount/date/customer using the `filter` query parameter.
3. **Match** — call `postCustomerInvoiceMatchedTransactions` to link the transaction(s) that settle an invoice.
4. **Mark paid** — call `markAsPaidCustomerInvoice` when the matched amount fully settles the invoice.

## Rules
- Use cursor pagination; never assume offset paging.
- Rate limit: 25 req / 5 s per token — batch and back off on `429` using `ratelimit-reset`.
- Prefer the Change Events feed (`getCustomerInvoicesChanges`) to detect new/updated invoices between reconciliation runs rather than re-scanning everything.
