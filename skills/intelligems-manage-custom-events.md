---
name: Define Intelligems custom events as test goals
description: Create or update client-side custom events (clicks, scroll depth, page views) with the External API so they can be used as goals and triggers on experiences.
api: openapi/intelligems-custom-events-api-openapi.yml
operations: [createOrUpdateCustomEvent, listExperiences, updateExperience]
---

# Define Intelligems custom events as test goals

Custom events are client-side behaviors Intelligems tracks on the storefront — a click on a
selector, a scroll threshold, a page view, an element entering the viewport, a JavaScript
event. Once defined they can be attached to an experience as a key metric or used as an
analytics filter (`triggeredCustomEvents`).

## Auth
Send the organization API key in the `intelligems-access-token` header on every request to
`https://api.intelligems.io`.

## Steps
1. **Choose the event type** — one of `clickEvent`, `scrollDepth`, `pageView`,
   `productPageView`, `collectionPageView`, `elementViewed`, `javascriptEvent`. Each type
   has its own `settings` shape; read the schema in
   `openapi/intelligems-custom-events-api-openapi.yml`.
2. **Create it** — `PUT /v25-10-beta/custom-events` (`createOrUpdateCustomEvent`) with a
   `customEvent` object carrying `type`, `name`, `settings`, and `applyToUrls` (required
   for `pageView` only; ignored for `productPageView`/`collectionPageView`).
3. **Batch** — `customEvent` also accepts an array of up to 50 event objects to create or
   update several in one request. It must be a single object or an array, nothing else.
4. **Update in place** — send the `id` returned by a previous create/update. Do **not** key
   off `identifier`: it is server-generated, read-only, and not guaranteed to stay the same
   across updates.
5. **Use it** — attach the event as a key metric on an experience
   (`updateExperience`, `experienceKeyMetrics[].experienceCustomMetricId`), or filter
   analytics by it with `triggeredCustomEvents` + `customEventsFilterType`.

## Rules that will bite you
- **This is a full replacement PUT.** When updating, the entire event configuration is
  replaced — any optional field you omit is reset to its default, not preserved.
- **403 means plan, not permission.** If the organization's plan does not include
  custom-events tracking, both create and update return `403`.
- `400` validation errors carry per-field messages under `properties.<field>.errors`.
- There is no idempotency key. A retried create makes a second event; re-send with the
  known `id` instead.
- Respect the token-bucket headers `x-ratelimit-limit` / `-remaining` / `-reset`; back off
  on `429`.

See `conventions/intelligems-conventions.yml`, `errors/intelligems-problem-types.yml`, and
`data-model/intelligems-data-model.yml`.
