# CarGurus

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

CarGurus is an automotive shopping and dealer marketing platform that connects car shoppers with franchise and independent dealers through data-driven listings, its Instant Market Value (IMV) deal ratings, and dealer reviews. For developers and partners, CarGurus publishes a small set of documented HTTP APIs under /Cars/api/ - an open Car Selector API for building new/used search widgets, and partner/dealer-gated APIs for Instant Market Value, dealer reviews, and dealer performance statistics (leads, VDPs, SRPs, impressions). Dealer inventory itself is ingested through inventory feeds (feed providers / IMT), not a documented public pull API, and leads are delivered to dealer CRMs rather than exposed as a public REST endpoint.

**Areas:** Automotive · Marketplace · Car Listings · Dealers · Vehicle Pricing · Reviews · Inventory

## CarGurus on APIs.io

Everything profiled for CarGurus is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/cargurus-dealer/](https://apis.io/providers/cargurus-dealer/)** — or go straight to one of the APIs or properties below.

### APIs (12)

- [CarGurus Car Selector API](https://apis.io/apis/cargurus-dealer/cargurus-dealer-car-selector-api/) — Open API for building new/used listing search widgets.
- [CarGurus Dealer Reviews API](https://apis.io/apis/cargurus-dealer/cargurus-dealer-dealer-reviews-api/) — Retrieve sales reviews for a specific dealer.
- [CarGurus Dealer Stats API](https://apis.io/apis/cargurus-dealer/cargurus-dealer-dealer-stats-api/) — Retrieve dealer inventory performance statistics.
- [CarGurus Instant Market Value API](https://apis.io/apis/cargurus-dealer/cargurus-dealer-instant-market-value-api/) — Retrieve CarGurus Instant Market Value and deal rating for cars.
- [CarGurus Dealer Stats API](https://apis.io/apis/cargurus-dealer/dealer-stats-api/) — Retrieves daily performance statistics for dealer inventory including search result page views, vehicle detail page clicks, and lead generation metrics…
- [CarGurus Instant Market Value API](https://apis.io/apis/cargurus-dealer/instant-market-value-api/) — Returns vehicle market valuations and deal ratings (Great Price, Good Price, Fair Price, etc.) based on VIN, make, model, trim, mileage, and location data,…
- [CarGurus Dealer Reviews API](https://apis.io/apis/cargurus-dealer/dealer-reviews-api/) — Provides access to consumer dealer reviews including ratings, review text, author information, timestamps, and dealer management responses, supporting…
- [CarGurus Dealer SMS API](https://apis.io/apis/cargurus-dealer/dealer-sms-api/) — Enables dealers to send SMS and MMS messages to consumers, supporting text and media content up to 1600 characters and 10 media attachments for direct…
- [CarGurus Car Selector API](https://apis.io/apis/cargurus-dealer/car-selector-api/) — Provides vehicle make and model lookup capabilities and generates search result URLs for new and used vehicle listings, supporting affiliate and partner…
- [CarGurus SEM Ad Landing Page URL Generator API](https://apis.io/apis/cargurus-dealer/sem-ad-url-generator-api/) — Generates targeted landing page URLs for Search Engine Marketing ad campaigns, enabling partners to create deep-linked pages pointing to relevant vehicle…
- [CarGurus SEM Filter Values API](https://apis.io/apis/cargurus-dealer/sem-filter-values-api/) — Supplies filter values used for constructing SEM campaigns and search configurations on the CarGurus platform, supporting dynamic ad targeting and search…
- [CarGurus Body Type Groups API](https://apis.io/apis/cargurus-dealer/body-type-groups-api/) — Provides vehicle body type classification and translation data, mapping CarGurus body type identifiers to human-readable labels for use in vehicle search…

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Cargurus Dealer Agentic Access](https://apis.io/agentic-access/cargurus-dealer/cargurus-dealer-agentic-access/)

#### Collections (3)

Postman and Open Collection request collections.

- [CarGurus Developer APIs Car Selector API](https://apis.io/collections/cargurus-dealer/open-cargurus-dealer-car-selector-api/)
- [CarGurus Developer APIs Car Selector Dealer Stats API](https://apis.io/collections/cargurus-dealer/open-cargurus-dealer-dealer-stats-api/)
- [CarGurus Developer APIs Car Selector Instant Market Value API](https://apis.io/collections/cargurus-dealer/open-cargurus-dealer-instant-market-value-api/)

#### Security (1)

Authentication, trust centre, and vulnerability disclosure.

- [Cargurus Dealer Domain Security](https://apis.io/security/cargurus-dealer/cargurus-dealer-domain-security/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Cargurus Dealer Plans Pricing](https://apis.io/plans/cargurus-dealer/cargurus-dealer-plans-pricing/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.cargurus.com)
- [Documentation](https://www.cargurus.com/Cars/developers/docs/CarSelector.html)
- [Sign up](https://dealers.cargurus.com/)
- [Blog](https://dealers.cargurus.com/drc)
- [GitHub](https://github.com/cargurus)

## API Evangelist rating

**Kin Score 28.3** — thin · rubric 0.24.0 · scored 2026-10-17

| Facet | Score |
|---|---|
| Discoverability | 57.1 |
| Contract quality | 44.4 |
| Contract governance | 0.0 |
| Operational transparency | 2.6 |
| Developer ergonomics | 40.5 |
| Access clarity | 21.1 |

**Agent readiness 17.3** — agent-aware

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | — |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | — |
| Error Semantics | — |
| OpenAPI Examples | — |
| Rate Limit Signal | — |
| Event Surface Described | — |
| Agent Skills | — |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |

**Regulatory alignment 11.8** — Horizontal (data, software, accessibility, platform)

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/cargurus-dealer/](https://apis.io/providers/cargurus-dealer/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for CarGurus: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/cargurus-dealer/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
