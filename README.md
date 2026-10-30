# Intelligems

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
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Intelligems is an AI-powered A/B testing, pricing optimization, and personalization platform for ecommerce stores, built primarily as a Shopify app. Merchants use it to test and personalize product and subscription pricing, discounts and offers, shipping strategies, content and landing pages, the checkout experience, and post-purchase offers, then measure the profit impact with built-in analytics. For developers, Intelligems publishes a REST External API (v25-10-beta) that manages experiences, defines custom events, and pulls experiment, sitewide and seasonal-benchmark analytics — with its own OpenAPI 3.1 published inside the reference — plus signed webhooks for the experience lifecycle, a client-side JavaScript API (window.igData), a headless React SDK (@intelligems/headless), and an official hosted MCP server with 46 OAuth-authenticated tools that connects experiments, Shopify store data, and analytics to Claude, ChatGPT, and Gemini.

**Areas:** Company · A/B Testing · E-Commerce · Pricing · Personalization · Conversion Rate Optimization · Shopify · Analytics · Experimentation · MCP · Webhook · Profit Optimization

## Intelligems on APIs.io

Everything profiled for Intelligems is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/intelligems/](https://apis.io/providers/intelligems/)** — or go straight to one of the APIs or properties below.

### APIs (10)

- [Intelligems MCP Server](https://apis.io/apis/intelligems/intelligems-mcp-server/) — Official hosted Model Context Protocol server exposing 46 tools over HTTP and SSE — experiment discovery and lifecycle, price-test prepare/commit,…
- [Intelligems Create Custom Event API](https://apis.io/apis/intelligems/intelligems-create-custom-event-api/) — The following custom event types are supported by the Intelligems Custom Events API: - `clickEvent` — Fires when a visitor clicks an element matching one or…
- [Intelligems Create Experience API](https://apis.io/apis/intelligems/intelligems-create-experience-api/) — The following experience types are supported by the Intelligems Experiments API: - `content/advanced` — Advanced content test (custom CSS/JS injection) -…
- [Intelligems Fetch Experience Data API](https://apis.io/apis/intelligems/intelligems-fetch-experience-data-api/) — The Fetch Experience Data API from Intelligems — 3 operation(s) for fetch experience data.
- [Intelligems Fetch Experience List API](https://apis.io/apis/intelligems/intelligems-fetch-experience-list-api/) — The Fetch Experience List API from Intelligems — 1 operation(s) for fetch experience list.
- [Intelligems Fetch Sitewide Analytics API](https://apis.io/apis/intelligems/intelligems-fetch-sitewide-analytics-api/) — The Fetch Sitewide Analytics API from Intelligems — 4 operation(s) for fetch sitewide analytics.
- [Intelligems Get Experience Export API](https://apis.io/apis/intelligems/intelligems-get-experience-export-api/) — The Get Experience Export API from Intelligems — 1 operation(s) for get experience export.
- [Intelligems Get Holiday Benchmark Data API](https://apis.io/apis/intelligems/intelligems-get-holiday-benchmark-data-api/) — The Get Holiday Benchmark Data API from Intelligems — 2 operation(s) for get holiday benchmark data.
- [Intelligems Perform Experience Action API](https://apis.io/apis/intelligems/intelligems-perform-experience-action-api/) — Lifecycle actions for managing experience state transitions (start, pause, end).
- [Intelligems Update Experience API](https://apis.io/apis/intelligems/intelligems-update-experience-api/) — Updates an existing experience. This is a full PUT replacement — the entire experience configuration is replaced with the provided data. All required fields…

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### AsyncAPI (1)

Event-driven and webhook contracts.

- [Intelligems Webhooks](https://apis.io/asyncapis/intelligems/intelligems-webhooks/)

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [intelligems](https://apis.io/servers/intelligems/intelligems/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Intelligems Agentic Access](https://apis.io/agentic-access/intelligems/intelligems-agentic-access/)

#### Collections (4)

Postman and Open Collection request collections.

- [Intelligems External Analytics API](https://apis.io/collections/intelligems/open-intelligems-analytics-api/)
- [Intelligems External Custom Events API](https://apis.io/collections/intelligems/open-intelligems-custom-events-api/)
- [Intelligems External Experiences API](https://apis.io/collections/intelligems/open-intelligems-experiences-api/)
- [Intelligems External Holiday Benchmark API](https://apis.io/collections/intelligems/open-intelligems-holiday-benchmark-api/)

#### Overlays (1)

OpenAPI overlays, including conversational phrasing for each operation.

- [Intelligems External Api Overlay](https://apis.io/overlays/intelligems/intelligems-external-api-overlay/)

#### Security (2)

Authentication, trust centre, and vulnerability disclosure.

- [Intelligems Authentication](https://apis.io/security/intelligems/intelligems-authentication/)
- [Intelligems Domain Security](https://apis.io/security/intelligems/intelligems-domain-security/)

#### OAuth scopes (1)

The permissions the API asks for.

- [Intelligems Scopes](https://apis.io/scopes/intelligems/intelligems-scopes/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Intelligems Plans Pricing](https://apis.io/plans/intelligems/intelligems-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Intelligems Rate Limits](https://apis.io/rate-limits/intelligems/intelligems-rate-limits/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://intelligems.io/)
- [Documentation](https://docs.intelligems.io/)
- [Getting started](https://docs.intelligems.io/getting-started/getting-started)
- [API reference](https://docs.intelligems.io/developer-resources/external-api)
- [Pricing](https://www.intelligems.io/pricing)
- [Sign up](https://apps.shopify.com/intelligems)
- [Support](https://www.intelligems.io/company/get-in-touch)
- [Changelog](https://www.intelligems.io/resources/product-updates)
- [Blog](https://www.intelligems.io/resources/blog)
- [Terms of service](https://www.intelligems.io/terms-of-service)
- [Privacy policy](https://www.intelligems.io/privacy-policy)

## API Evangelist rating

**Kin Score 60.7** — strong · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 75.0 |
| Contract quality | 57.5 |
| Contract governance | 4.5 |
| Operational transparency | 55.3 |
| Developer ergonomics | 73.2 |
| Access clarity | 65.8 |

**Agent readiness 56.2** — agent-ready (gated down from agent-native)

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | — |
| MCP Server | verified |
| Auth Clarity | served (partial credit) |
| Idempotency | — |
| Error Semantics | documented (partial credit) |
| OpenAPI Examples | partial |
| Rate Limit Signal | documented (partial credit) |
| Event Surface Described | yes |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | served (partial credit) |
| Protected Resource Metadata | verified |
| Dynamic Client Registration | yes |
| Agentic Commerce | — |
| Pagination Ratio | na |
| Operation Distinctiveness | distinct |

**Regulatory alignment 34.3** — Horizontal (data, software, accessibility, platform)

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/intelligems/](https://apis.io/providers/intelligems/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Intelligems: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/intelligems/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
