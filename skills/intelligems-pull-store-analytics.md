---
name: Pull Intelligems store analytics
description: Retrieve sitewide analytics snapshots, time series, and conversion funnels for a Shopify store.
api: openapi/intelligems-analytics-api-openapi.yml
operations: [getSitewideSnapshot, getSitewideTimeseries, getSitewideOrderDistribution, getSitewideConversionFunnel]
---

# Pull Intelligems store analytics

Use the sitewide analytics endpoints of the Intelligems External API to build reports and dashboards.

## Auth
Send your Intelligems API key in the `intelligems-access-token` header.

## Steps
1. **Snapshot** — `POST /v25-10-beta/analytics/sitewide/snapshot` (`getSitewideSnapshot`) for revenue per visitor, net revenue, and conversion rate. Pass a date range / filters in the JSON body.
2. **Time series** — `POST /v25-10-beta/analytics/sitewide/timeseries` (`getSitewideTimeseries`) to trend the same metrics.
3. **Order distribution** — `POST /v25-10-beta/analytics/sitewide/order-distribution` (`getSitewideOrderDistribution`).
4. **Conversion funnel** — `POST /v25-10-beta/analytics/sitewide/conversion-funnel` (`getSitewideConversionFunnel`).

## Conventions & errors
- Sitewide analytics run a tighter token bucket (burst 10, refill 5 / 30s) — respect `x-ratelimit-*` headers.
- `400` validation errors carry per-field messages under `properties.<field>.errors`; `401` means a bad `intelligems-access-token`.
- Every analytics operation accepts the shared `filters` object (audience, landing page, behavior, product, order) — see the Filters reference. Operators that expect values return `400` when the value is empty.
- Statistical metrics come back with `ci_low`/`ci_high`, `plus_minus`, `p2bb`, `p2bc` and `uplift`; report the interval, not just the point value.
- See `conventions/intelligems-conventions.yml` and `rate-limits/intelligems-rate-limits.yml`.
