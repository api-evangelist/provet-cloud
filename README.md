# Provet Cloud (provet-cloud)

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

Provet Cloud is a cloud-based veterinary practice management system (PIMS) built by [Nordhealth](https://nordhealth.com) for animal clinics, hospitals, and referral practices. It exposes a documented, browsable REST API (version 0.1) that gives approved integration partners programmatic access to clients, patients (animals), consultations, appointments and online booking, invoicing and payments, items, and reference data, plus a webhook system with 60+ triggers for reacting to changes in a Provet Cloud installation.

The base URL is installation-specific: `https://provetcloud.com/<provet_id>/api/0.1/` (regional domains such as `us.provetcloud.com` and `enterprise.provetcloud.com` also exist). Requests return JSON and are authorized with OAuth 2.0 — Client Credentials for backend services, or Authorization Code with PKCE for user-facing apps — via the token endpoint `https://provetcloud.com/<provet_id>/oauth2/token/` and the `restapi` scope. A legacy `Authorization: Token <key>` header exists but is deprecated. Integrations are registered and approved by Provet's support team per installation; the documentation at [developers.provetcloud.com](https://developers.provetcloud.com/restapi/) is freely browsable by any customer or developer.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/provet-cloud/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/provet-cloud/refs/heads/main/apis.yml)

## Tags

- Veterinary
- Practice Management
- PIMS
- Healthcare
- Nordhealth
- Animal Health
- Appointments
- Billing

## Timestamps

- **Created:** 2026-07-03
- **Modified:** 2026-07-03

## APIs

### Provet Cloud Clients API

Manage clients (the animal owners / bill payers) — list and filter clients, create new clients, patch client fields and communication preferences, attach phone numbers, and read or write per-client custom field values.

- **Human URL:** [https://developers.provetcloud.com/restapi/howto_clients_patients.html](https://developers.provetcloud.com/restapi/howto_clients_patients.html)
- **Base URL:** `https://provetcloud.com/{provet_id}/api/0.1`

#### Tags

- Clients
- Owners
- CRM

#### Properties

- [Documentation](https://developers.provetcloud.com/restapi/)
- [API Reference](https://developers.provetcloud.com/restapi/howto_clients_patients.html)
- [OpenAPI](openapi/provet-cloud-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/provet-cloud.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/provet-cloud.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Provet Cloud Patients API

Manage patients (the animals) linked to clients — list and filter by client, name, microchip, species, or modification date, create single patients or bulk-create many, patch patient details, and read or write per-patient custom field values.

- **Human URL:** [https://developers.provetcloud.com/restapi/howto_clients_patients.html](https://developers.provetcloud.com/restapi/howto_clients_patients.html)
- **Base URL:** `https://provetcloud.com/{provet_id}/api/0.1`

#### Tags

- Patients
- Animals
- Medical Records

#### Properties

- [API Reference](https://developers.provetcloud.com/restapi/howto_clients_patients.html)
- [OpenAPI](openapi/provet-cloud-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/provet-cloud.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/provet-cloud.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Provet Cloud Appointments API

Create appointments and drive an online booking platform — book appointments against a department, reason, and supervising user, send confirmations, create reminders, and register online-booking clients and patients.

- **Human URL:** [https://developers.provetcloud.com/restapi/howto_appointments.html](https://developers.provetcloud.com/restapi/howto_appointments.html)
- **Base URL:** `https://provetcloud.com/{provet_id}/api/0.1`

#### Tags

- Appointments
- Online Booking
- Scheduling

#### Properties

- [API Reference](https://developers.provetcloud.com/restapi/howto_appointments.html)
- [OpenAPI](openapi/provet-cloud-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/provet-cloud.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/provet-cloud.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Provet Cloud Consultations API

Create and manage consultations (clinical visits) — create and filter consultations, advance their lifecycle with `update_status`, mark them sent to external systems, and attach clinical items (medicines, procedures, supplies, foods), diagnoses, notes, and discharge instructions.

- **Human URL:** [https://developers.provetcloud.com/restapi/howto_consultations.html](https://developers.provetcloud.com/restapi/howto_consultations.html)
- **Base URL:** `https://provetcloud.com/{provet_id}/api/0.1`

#### Tags

- Consultations
- Clinical
- Treatment

#### Properties

- [API Reference](https://developers.provetcloud.com/restapi/howto_consultations.html)
- [OpenAPI](openapi/provet-cloud-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/provet-cloud.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/provet-cloud.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Provet Cloud Billing & Invoicing API

Read invoices and invoice rows, issue full or partial refunds (credit notes), record and cancel payments against finalized invoices, and record unallocated prepayments and read their balances. Supports ERP and accounting integration back-ends.

- **Human URL:** [https://developers.provetcloud.com/restapi/howto_billing.html](https://developers.provetcloud.com/restapi/howto_billing.html)
- **Base URL:** `https://provetcloud.com/{provet_id}/api/0.1`

#### Tags

- Billing
- Invoicing
- Payments

#### Properties

- [API Reference](https://developers.provetcloud.com/restapi/howto_billing.html)
- [OpenAPI](openapi/provet-cloud-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/provet-cloud.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/provet-cloud.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Provet Cloud Items & Reference Data API

Read the master item catalog (medicines, procedures, supplies, foods), departments, appointment reasons, users, custom field definitions, and code lists (species, breeds, diagnoses) used as reference data across the API.

- **Human URL:** [https://developers.provetcloud.com/restapi/endpoints.html](https://developers.provetcloud.com/restapi/endpoints.html)
- **Base URL:** `https://provetcloud.com/{provet_id}/api/0.1`

#### Tags

- Items
- Products
- Reference Data
- Departments

#### Properties

- [API Reference](https://developers.provetcloud.com/restapi/endpoints.html)
- [OpenAPI](openapi/provet-cloud-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/provet-cloud.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/provet-cloud.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Provet Cloud Webhooks API

Subscribe to changes in a Provet Cloud installation. Provet Cloud POSTs an event (with the changed object's ID) to a configured URL for 60+ triggers across clients, patients, consultations, appointments, invoices, stock, imaging, labs, and communications; webhooks can be scoped organization-wide or to a department and are retried up to 10 times.

- **Human URL:** [https://developers.provetcloud.com/restapi/webhooks.html](https://developers.provetcloud.com/restapi/webhooks.html)
- **Base URL:** `https://provetcloud.com/{provet_id}/api/0.1`

#### Tags

- Webhooks
- Events
- Notifications

#### Properties

- [Documentation](https://developers.provetcloud.com/restapi/webhooks.html)
- [API Reference](https://developers.provetcloud.com/restapi/webhook_triggers.html)
- [OpenAPI](openapi/provet-cloud-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/provet-cloud.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/provet-cloud.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [LinkedIn](https://www.linkedin.com/company/provetcloud)
- [Website](https://www.provet.cloud)
- [Documentation](https://developers.provetcloud.com/restapi/)
- [Plans](plans/provet-cloud-plans-pricing.yml)
- [Rate Limits](rate-limits/provet-cloud-rate-limits.yml)
- [Fin Ops](finops/provet-cloud-finops.yml)

## Authentication

OAuth 2.0. Two grant types are supported:

- **Client Credentials** — backend service-to-service access with no user interaction.
- **Authorization Code (with PKCE)** — user-facing apps where a user authorizes access as themselves. PKCE is required for public clients.

Token endpoint: `https://provetcloud.com/<provet_id>/oauth2/token/` · Authorization endpoint: `https://provetcloud.com/<provet_id>/oauth2/authorize/` · Scope: `restapi` (and optional `openid`). Access tokens last ~10 hours; refresh tokens ~30 days from last use. Integrations must be registered and approved by Provet's support team, which issues a `client_id` and `client_secret`. The legacy `Authorization: Token <key>` header is deprecated.

## Rate Limits

Rate limits are enforced per endpoint over a rolling 60-second window and are additive across endpoints. Exceeding a limit returns `HTTP 429 Too Many Requests` with a `Retry-After` header. Requesting a larger custom page size consumes requests proportional to the default page size. See [rate-limits/provet-cloud-rate-limits.yml](rate-limits/provet-cloud-rate-limits.yml).

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
