# Tock (tock-reservations)

Tock is a restaurant and hospitality reservations, events, and ordering platform used by restaurants, wineries, bars, and hotels to manage bookings, prepaid experiences, waitlists, and guest data. Tock is owned by American Express, which acquired the company from Squarespace in 2024.

**Access model:** Tock does **not** offer an open, self-serve developer API. Its data API and webhook program is **partner and enterprise-gated** - access is limited to Premium and Premium Unlimited plans and is provisioned by request. To request an API key, an Account Owner emails `integrate@tockhq.com` from an email address listed on the business' Tock Dashboard Team page. Tock publishes public **data-model reference documentation** at `api.exploretock.com`, but concrete endpoint paths, HTTP methods, and OpenAPI definitions are only shared with approved partners. The API entries in this catalog are therefore **modeled** (`endpointsModeled: true`) from the public data model and API FAQ - no endpoints are fabricated.

**Key limitation:** Reservation records **cannot** be created or manipulated through the API. The write surface is limited to ingesting basic guest information and guest-profile tags.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/tock-reservations/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/tock-reservations/refs/heads/main/apis.yml)

## Tags

- Reservations
- Restaurants
- Hospitality
- Events
- Ordering
- Guest Data
- Webhooks
- Partner API
- American Express

## Timestamps

- **Created:** 2026-07-05
- **Modified:** 2026-07-05

## APIs (modeled from public data model and API FAQ)

### Tock Data Exports API

Twice-daily export of all historical reservation and guest data for the locations in a Tock business group. Payloads follow the published Reservation data model (party, purchased experiences, options, fees, payments, refunds, payouts, feedback, notes, tables).

- **Documentation:** [Reservation Data Model](https://api.exploretock.com/docs/latest/reservation.html)
- **API FAQ:** [Tock API FAQ](https://tock.zendesk.com/hc/en-us/articles/25447494175508-API-FAQ)
- **Base URL:** `https://api.exploretock.com` (endpoints modeled - not published)

### Tock Guest Profile Ingest API

Add and update basic guest information and guest-profile tags in Tock, following the published Guest data model (patron identity, contact details, dietary restrictions, hospitality preferences, business and business-group notes and tags). Only basic guest information may be created or updated.

- **Documentation:** [Guest Data Model](https://api.exploretock.com/docs/latest/guest_profile.html)
- **API FAQ:** [Tock API FAQ](https://tock.zendesk.com/hc/en-us/articles/25447494175508-API-FAQ)
- **Base URL:** `https://api.exploretock.com` (endpoints modeled - not published)

### Tock Real-time Reservation Webhook

Real-time webhook delivering reservation updates for all locations within a Tock business group to a partner-supplied endpoint URL. The partner provides the receiving endpoint and any required authorization headers; Tock POSTs reservation events shaped by the Reservation data model.

- **Documentation:** [Reservation Data Model](https://api.exploretock.com/docs/latest/reservation.html)
- **Base URL:** `https://api.exploretock.com` (endpoints modeled - not published)

### Tock Real-time Guest Profile Webhook

Real-time webhook delivering guest-profile updates for all locations within a Tock business group to a partner-supplied endpoint URL. Tock POSTs guest-profile events shaped by the Guest data model.

- **Documentation:** [Guest Data Model](https://api.exploretock.com/docs/latest/guest_profile.html)
- **Base URL:** `https://api.exploretock.com` (endpoints modeled - not published)

## Common Properties

- [LinkedIn](https://www.linkedin.com/company/tock-hq)
- [Website](https://www.exploretock.com)
- [Documentation - Reservation Data Model](https://api.exploretock.com/docs/latest/reservation.html)
- [Documentation - API FAQ](https://tock.zendesk.com/hc/en-us/articles/25447494175508-API-FAQ)
- [Integrations](https://www.exploretock.com/join/integrations/)
- [Partnerships](https://www.exploretock.com/join/partnerships/)
- [Plans](plans/tock-reservations-plans-pricing.yml)

## Pricing

Tock sells tiered per-venue SaaS (no per-cover diner fee; a 2-3% transaction fee applies to prepaid bookings on lower tiers). API and webhook access is gated to the higher Premium / Premium Unlimited plans and provisioned by request rather than sold as a metered API product. See [plans/tock-reservations-plans-pricing.yml](plans/tock-reservations-plans-pricing.yml) and Tock's [pricing page](https://www.exploretock.com/join/pricing/) for current figures.

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
