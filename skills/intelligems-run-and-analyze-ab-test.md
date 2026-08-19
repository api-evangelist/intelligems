---
name: Run and analyze an Intelligems A/B test
description: Create an experience, start it, then pull performance results and statistical significance.
api: openapi/intelligems-experiences-api-openapi.yml
operations: [createExperience, performExperienceAction, getExperience, queryExperienceAnalytics, exportExperienceAnalytics]
---

# Run and analyze an Intelligems A/B test

Use the Intelligems External API (`https://api.intelligems.io`) to stand up a test and read its results.

## Auth
Send your Intelligems API key in the `intelligems-access-token` header on every request. A missing/invalid key returns `401 {"error":"Unauthorized"}`.

## Steps
1. **Create the experience** — `POST /v25-10-beta/experiences` (`createExperience`) with your org-specific configuration (variations, targeting, traffic allocation) as JSON.
2. **Start it** — `POST /v25-10-beta/experiences/{experienceId}/actions/start` (`performExperienceAction`). Valid actions are `start`, `pause`, `end`.
3. **Confirm configuration** — `GET /v25-10-beta/experiences/{experienceId}` (`getExperience`) to read back variations and targeting rules.
4. **Read results** — `POST /v25-10-beta/analytics/resource/{experienceId}` (`queryExperienceAnalytics`) for A/B performance and statistical comparison; do not use `GET` on the same path (`getExperienceAnalytics`) — Intelligems marks it deprecated and removes it when the beta ends.
5. **Export** (optional) — `POST /v25-10-beta/analytics/experience/{experienceId}/export` (`exportExperienceAnalytics`).

## Conventions & errors
- Watch the token-bucket rate limit on experience endpoints (burst 50, refill 25 / 30s); honor `x-ratelimit-remaining` / `x-ratelimit-reset` and back off on `429`.
- Validation failures return `400` with per-field messages under `properties.<field>.errors`.
- There is no idempotency key: never blindly retry `createExperience` after a timeout — list experiences and check before retrying.
- New experiences are drafts and reach no shopper until `start`; QA with `?ig-preview=<experienceId>` and `?igTg=<variationId>` first (see `sandbox/intelligems-sandbox.yml`).
- See `conventions/intelligems-conventions.yml` and `errors/intelligems-problem-types.yml`.
