---
name: Keep an integration in sync via Change Events
description: Poll Pennylane change-event feeds to sync invoices and suppliers without webhooks.
api: openapi/pennylane-openapi.yml
operations: [getCustomerInvoicesChanges, getSupplierInvoicesChanges]
---

# Keep an integration in sync via Change Events

Pennylane does not emit webhooks; instead it exposes change-event feeds (4-week retention) you poll to stay in sync.

## Prerequisites
- Bearer token with read access to the relevant resources.
- Base URL: `https://app.pennylane.com/api/external/v2`.

## Steps
1. **Poll customer invoice changes** — call `getCustomerInvoicesChanges` (`GET /customer_invoices/changes`) on a schedule, passing the last cursor so you only receive new changes.
2. **Poll supplier invoice changes** — call `getSupplierInvoicesChanges` similarly for accounts payable.
3. **Fetch full records** — for each changed id, read the full resource (e.g. `getCustomerInvoice`) if you need the current state.
4. **Persist the cursor** — store the returned cursor so the next poll resumes exactly where you left off.

## Rules
- Change events are retained only ~4 weeks — poll at least that often or you will miss changes and must do a full resync.
- Cursor pagination throughout; iterate until no next cursor.
- Rate limit: 25 req / 5 s per token.
