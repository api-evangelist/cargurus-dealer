# CarGurus (cargurus-dealer)

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

CarGurus is an automotive shopping and dealer marketing platform that connects car shoppers with franchise and independent dealers through data-driven listings, its Instant Market Value (IMV) deal ratings, and dealer reviews. For developers and partners, CarGurus publishes a small, purpose-built set of HTTP APIs under `/Cars/api/` rather than a broad open developer platform.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/cargurus-dealer/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/cargurus-dealer/refs/heads/main/apis.yml)

## Access model (read this first)

CarGurus does not sell metered, self-serve API access. Access is tiered by relationship:

- **Car Selector API — open.** No `appId` or `authToken` required. Intended for building new/used listing search widgets that redirect shoppers into CarGurus search results.
- **Instant Market Value, Dealer Reviews, and Dealer Stats APIs — gated.** Each requires an `appId` and `authToken` issued by CarGurus. These are made available to dealers under a CarGurus subscription and to approved analytics/marketing partners (for example vAuto, Clarivoy, Vistadash).
- **Inventory ingestion is feed-based, not a public pull API.** Dealer inventory reaches CarGurus through inventory feeds (feed providers / IMT), and **leads are delivered into dealer CRMs**, not exposed as a public REST endpoint. This entry does **not** fabricate inventory- or lead-retrieval endpoints — only the four documented API surfaces are described.

Dealer subscription packages and partner terms are quote-based and not publicly listed; CarGurus operates a published Dealer Pricing Policy but does not disclose per-tier monthly rates.

## Tags

- Automotive
- Marketplace
- Car Listings
- Dealer
- Vehicle Pricing
- Reviews
- Inventory

## Timestamps

- **Created:** 2026-07-10
- **Modified:** 2026-07-10

## APIs

### CarGurus Car Selector API

Open (no-auth) API for building your own new/used listing search widget. List available makes and models plus search distances, then construct a listing search redirect URL.

- **Human URL:** [CarSelector.html](https://www.cargurus.com/Cars/developers/docs/CarSelector.html)
- **Base URL:** `https://www.cargurus.com/Cars/api/1.0`
- Endpoints: `GET /carselector/listMakes.action`, `GET /carselector/listModels.action`, `GET /carselector/listingSearch.action`

### CarGurus Instant Market Value API

Partner/dealer-gated API to retrieve the CarGurus Instant Market Value for one or more cars, plus the deal rating (`GREAT_PRICE`, `GOOD_PRICE`, `FAIR_PRICE`, `OVERPRICED`, and more) and normalized make/model/trim/options in the CarGurus ontology.

- **Human URL:** [InstantMarketValue.html](https://www.cargurus.com/Cars/developers/docs/InstantMarketValue.html)
- **Base URL:** `https://www.cargurus.com/Cars/api/1.0`
- Endpoint: `POST /imvRequest.action` (query params `appId`, `authToken`, `body`)

### CarGurus Dealer Reviews API

Partner/dealer-gated API to retrieve the sales reviews for a specific CarGurus dealer, including 1-5 star ratings, author, body, moderation status, and optional dealership management responses. External reuse is limited to 160 characters with attribution and a link back to CarGurus.

- **Human URL:** [DealerReviews.html](https://www.cargurus.com/Cars/developers/docs/DealerReviews.html)
- **Base URL:** `https://www.cargurus.com/Cars/api/1.0`
- Endpoint: `POST /dealerReviewsRequest.action` (query params `appId`, `authToken`, `body`)

### CarGurus Dealer Stats API

Partner/dealer-gated API (v2.0) to retrieve inventory performance statistics for a dealer — phone/chat/SMS/email leads, VDPs, SRPs, printouts, map/website/social clicks, impressions, and a `daily_stats` time series. Consumed by dealer analytics partners. Response fields are modeled from CarGurus documentation and published examples.

- **Human URL:** [DealerStatsV2Daily.html](https://www.cargurus.com/Cars/developers/docs/DealerStatsV2Daily.html)
- **Base URL:** `https://www.cargurus.com/Cars/api/2.0`
- Endpoint: `POST /dealerStatsRequest.action` (query params `appId`, `authToken`, `body`)

## Artifacts

- [OpenAPI](openapi/cargurus-dealer-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Plans](plans/cargurus-dealer-plans-pricing.yml)

## WebSocket review

CarGurus does **not** expose a documented public WebSocket API. Every documented developer API is request/response HTTP over HTTPS (GET for Car Selector, POST for IMV/Reviews/Stats). See [review.yml](review.yml).

## Common Properties

- [GitHub Organization](https://github.com/cargurus)
- [LinkedIn](https://www.linkedin.com/company/cargurus)
- [Website](https://www.cargurus.com)
- [Developer Portal](https://www.cargurus.com/Cars/developers/)
- [Documentation](https://www.cargurus.com/Cars/developers/docs/CarSelector.html)
- [Sign Up (Dealers)](https://dealers.cargurus.com/)
- [Plans](plans/cargurus-dealer-plans-pricing.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
