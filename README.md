# CarGurus (cargurus-dealer)

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
