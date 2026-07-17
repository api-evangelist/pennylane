---
name: Export French accounting (FEC / General Ledger)
description: Produce a French FEC export and General Ledger for a fiscal year from Pennylane.
api: openapi/pennylane-openapi.yml
operations: [getFiscalYears, getTrialBalance, exportGeneralLedger, exportFec]
---

# Export French accounting (FEC / General Ledger)

Generate the statutory exports a French accountant needs.

## Prerequisites
- Bearer token with ledger/accounting read access.
- Base URL: `https://app.pennylane.com/api/external/v2`.

## Steps
1. **Pick the fiscal year** — call `getFiscalYears` (`GET /fiscal_years`) to get the period boundaries.
2. **Sanity-check balances** — call `getTrialBalance` (`GET /trial_balance`) for the period.
3. **General Ledger** — call `exportGeneralLedger` to produce the General Ledger (or Analytical GL) as an xlsx file.
4. **FEC** — call `exportFec` to produce the French FEC (Fichier des Écritures Comptables) export file.

## Rules
- Exports may be asynchronous / large; poll for the downloadable file rather than assuming an immediate body.
- Rate limit: 25 req / 5 s per token; honor `retry-after` on `429`.
