# Pennylane (pennylane)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Pennylane is a French financial and accounting operating system for SMEs and accounting firms. The Company API (v2) lets companies, firms, and integration partners access and sync invoicing, accounting, banking, and financial data over a REST interface, and automate end-to-end workflows. V2 is the stable version; V1 is deprecated. All amounts are in EUR and the platform is built around French accounting (FEC exports, Plateforme Agréée e-invoicing, SEPA/GoCardless mandates).

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/pennylane/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/pennylane/refs/heads/main/apis.yml)

## Tags

- Accounting
- Invoicing
- Fintech
- Financial Data
- Banking
- France
- SME

## Timestamps

- **Created:** 2026-07-17
- **Modified:** 2026-07-17

## APIs

### Pennylane Customer Invoicing API

Create, import, finalize, categorize, send, and match customer invoices and credit notes, including Factur-X / UBL / CII e-invoice import and quote-to-invoice conversion.

- **Human URL:** [https://pennylane.readme.io/reference/getcustomerinvoices](https://pennylane.readme.io/reference/getcustomerinvoices)
- **Base URL:** `https://app.pennylane.com/api/external/v2`

#### Tags

- Customer Invoices
- Credit Notes
- E-Invoicing

#### Properties

- [Documentation](https://pennylane.readme.io/docs/customer-invoicing)
- [API Reference](https://pennylane.readme.io/reference/getcustomerinvoices)
- [OpenAPI](openapi/pennylane-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/pennylane.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)

### Pennylane Supplier Invoicing API

Import, update, validate, and match supplier invoices, link purchase requests, and manage e-invoice lifecycle transitions for accounts payable.

- **Human URL:** [https://pennylane.readme.io/reference/getsupplierinvoices](https://pennylane.readme.io/reference/getsupplierinvoices)
- **Base URL:** `https://app.pennylane.com/api/external/v2`

#### Tags

- Supplier Invoices
- Accounts Payable
- E-Invoicing

#### Properties

- [Documentation](https://pennylane.readme.io/docs/supplier-invoicing)
- [API Reference](https://pennylane.readme.io/reference/getsupplierinvoices)
- [OpenAPI](openapi/pennylane-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### Pennylane Accounting & Ledger API

Read and write journals, ledger accounts, ledger entries and entry lines, lettering, trial balance, and fiscal years for double-entry accounting.

- **Human URL:** [https://pennylane.readme.io/reference/getledgerentries](https://pennylane.readme.io/reference/getledgerentries)
- **Base URL:** `https://app.pennylane.com/api/external/v2`

#### Tags

- Accounting
- Ledger
- Journals
- Trial Balance

#### Properties

- [Documentation](https://pennylane.readme.io/docs/create-a-ledger-entry)
- [API Reference](https://pennylane.readme.io/reference/getledgerentries)
- [OpenAPI](openapi/pennylane-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### Pennylane Accounting Exports API

Generate General Ledger, Analytical General Ledger, and French FEC (Fichier des Écritures Comptables) exports as downloadable xlsx / FEC files.

- **Human URL:** [https://pennylane.readme.io/reference/exportgeneralledger](https://pennylane.readme.io/reference/exportgeneralledger)
- **Base URL:** `https://app.pennylane.com/api/external/v2`

#### Tags

- Exports
- FEC
- General Ledger

#### Properties

- [Documentation](https://pennylane.readme.io/docs/accounting-reporting)
- [API Reference](https://pennylane.readme.io/reference/exportgeneralledger)
- [OpenAPI](openapi/pennylane-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### Pennylane Banking API

Manage bank accounts and establishments, banking transactions, and automate matching of transactions to customer and supplier invoices.

- **Human URL:** [https://pennylane.readme.io/reference/gettransactions](https://pennylane.readme.io/reference/gettransactions)
- **Base URL:** `https://app.pennylane.com/api/external/v2`

#### Tags

- Banking
- Transactions
- Reconciliation

#### Properties

- [Documentation](https://pennylane.readme.io/docs/automating-payment-matching)
- [API Reference](https://pennylane.readme.io/reference/gettransactions)
- [OpenAPI](openapi/pennylane-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### Pennylane Customers & Suppliers API

Create and manage company and individual customers and suppliers, their contacts, and analytical categorization.

- **Human URL:** [https://pennylane.readme.io/reference/getcustomers](https://pennylane.readme.io/reference/getcustomers)
- **Base URL:** `https://app.pennylane.com/api/external/v2`

#### Tags

- Customers
- Suppliers
- Contacts

#### Properties

- [Documentation](https://pennylane.readme.io/docs/filter-my-customers)
- [API Reference](https://pennylane.readme.io/reference/getcustomers)
- [OpenAPI](openapi/pennylane-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### Pennylane Products Catalog API

List, create, and update the product catalog used on invoices, quotes, and subscriptions.

- **Human URL:** [https://pennylane.readme.io/reference/getproducts](https://pennylane.readme.io/reference/getproducts)
- **Base URL:** `https://app.pennylane.com/api/external/v2`

#### Tags

- Products
- Catalog

#### Properties

- [Documentation](https://pennylane.readme.io/docs/filter-my-products)
- [API Reference](https://pennylane.readme.io/reference/getproducts)
- [OpenAPI](openapi/pennylane-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### Pennylane Quotes API

Create, update, send, and status-manage sales quotes, and convert an accepted quote into a customer invoice.

- **Human URL:** [https://pennylane.readme.io/reference/listquotes](https://pennylane.readme.io/reference/listquotes)
- **Base URL:** `https://app.pennylane.com/api/external/v2`

#### Tags

- Quotes
- Estimates

#### Properties

- [API Reference](https://pennylane.readme.io/reference/listquotes)
- [OpenAPI](openapi/pennylane-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### Pennylane Billing Subscriptions API

Create and manage recurring billing subscriptions that automatically generate monthly customer invoices, optionally linked to a GoCardless mandate.

- **Human URL:** [https://pennylane.readme.io/reference/getbillingsubscriptions](https://pennylane.readme.io/reference/getbillingsubscriptions)
- **Base URL:** `https://app.pennylane.com/api/external/v2`

#### Tags

- Subscriptions
- Recurring Billing

#### Properties

- [API Reference](https://pennylane.readme.io/reference/getbillingsubscriptions)
- [OpenAPI](openapi/pennylane-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### Pennylane Direct Debit Mandates API

Create and manage SEPA direct debit mandates and GoCardless mandates for automated customer collection.

- **Human URL:** [https://pennylane.readme.io/reference/getsepamandates](https://pennylane.readme.io/reference/getsepamandates)
- **Base URL:** `https://app.pennylane.com/api/external/v2`

#### Tags

- SEPA
- GoCardless
- Direct Debit

#### Properties

- [API Reference](https://pennylane.readme.io/reference/getsepamandates)
- [OpenAPI](openapi/pennylane-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### Pennylane Change Events API

Poll change-event feeds for invoices, customers, suppliers, products, transactions, quotes, and ledger entry lines (last 4 weeks retained) to keep integrations in sync without webhooks.

- **Human URL:** [https://pennylane.readme.io/docs/tracking-data-changes-with-pennylane-api](https://pennylane.readme.io/docs/tracking-data-changes-with-pennylane-api)
- **Base URL:** `https://app.pennylane.com/api/external/v2`

#### Tags

- Change Events
- Sync
- Webhooks Alternative

#### Properties

- [Documentation](https://pennylane.readme.io/docs/tracking-data-changes-with-pennylane-api)
- [API Reference](https://pennylane.readme.io/reference/getcustomerinvoiceschanges)
- [OpenAPI](openapi/pennylane-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### Pennylane E-Invoicing (Plateforme Agréée) API

Manage French electronic-invoicing onboarding via Plateforme Agréée (PA) registrations, and send customer e-invoices to the partner dematerialization platform.

- **Human URL:** [https://pennylane.readme.io/reference/getparegistrations](https://pennylane.readme.io/reference/getparegistrations)
- **Base URL:** `https://app.pennylane.com/api/external/v2`

#### Tags

- E-Invoicing
- Factur-X
- Plateforme Agréée

#### Properties

- [API Reference](https://pennylane.readme.io/reference/getparegistrations)
- [OpenAPI](openapi/pennylane-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

## Common Properties

- [LinkedIn](https://www.linkedin.com/company/pennylane)
- [Website](https://www.pennylane.com/)
- [Documentation](https://pennylane.readme.io/)
- [Plans](plans/pennylane-plans-pricing.yml)
- [Rate Limits](rate-limits/pennylane-rate-limits.yml)
- [Fin Ops](finops/pennylane-finops.yml)

## Authentication

Pennylane API v2 requires a Bearer token in the `Authorization` header on every request. The token can be a **Company API token**, a **Firm API token**, or an **OAuth 2.0 access token** (authorization code grant) for integration partners registered via the Partnerships team.

- Authorize: `https://app.pennylane.com/oauth/authorize`
- Token: `https://app.pennylane.com/oauth/token`
- Revoke: `https://app.pennylane.com/oauth/revoke`

Scopes follow a `resource:readonly` / `resource:all` pattern and enforce least privilege (missing scope returns `403 Forbidden`).

## Rate Limits

25 requests every 5 seconds per token. Exceeding the limit returns `429` with a `retry-after` header; all responses include `ratelimit-limit`, `ratelimit-remaining`, and `ratelimit-reset` headers.

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
