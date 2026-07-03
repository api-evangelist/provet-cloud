# Provet Cloud (provet-cloud)

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
