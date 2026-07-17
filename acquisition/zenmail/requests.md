# Request ledger

Requests were made on **2026-07-17**. Search requests used Google US-English
and desktop Windows where applicable.

Reusable authentication and endpoint guidance belongs in the central
[DataForSEO documentation](../../tools/dataforseo.md). Credentials are
redacted here and were not written to the repository.

## Spend summary

| Request group | Calls | Cost |
| --- | ---: | ---: |
| DataForSEO Labs | 4, including one repeated call after a local formatter failure | $0.048000 |
| Backlinks | 2 | $0.048072 |
| Content Analysis | 2 | $0.048720 |
| Ads Transparency SERPs | 2 | $0.004000 |
| Organic live SERPs | 5 | $0.010000 |
| **Total** | **15** | **$0.158792** |

The report stayed below the **$0.25** cap.

## Exact DataForSEO requests

Authentication header:

```text
Authorization: Basic [REDACTED]
Content-Type: application/json
```

### Labs

Domain Rank Overview:

```json
[{"target":"usezenmail.com","location_code":2840,"language_code":"en","ignore_synonyms":true}]
```

- Endpoint: `dataforseo_labs/google/domain_rank_overview/live`
- Task ID: `07171656-2101-0388-0000-53feb636491f`
- Cost: `$0.012000`
- Result: no items; `total_count` unavailable

Ranked Keywords, initial call:

```json
[{"target":"usezenmail.com","location_code":2840,"language_code":"en","ignore_synonyms":true,"item_types":["organic","paid"],"limit":250,"order_by":["keyword_data.keyword_info.search_volume,desc"]}]
```

- Endpoint: `dataforseo_labs/google/ranked_keywords/live`
- Task ID: `07171656-2101-0381-0000-569d1d8ce845`
- Cost: `$0.012000`
- Result: raw response not retained after a local formatter failure; the task
  ID, status, cost, and request metadata were recovered from the provider's
  free ID history

Ranked Keywords, retained retry:

```json
[{"target":"usezenmail.com","location_code":2840,"language_code":"en","ignore_synonyms":true,"item_types":["organic","paid"],"limit":250,"order_by":["keyword_data.keyword_info.search_volume,desc"]}]
```

- Endpoint: `dataforseo_labs/google/ranked_keywords/live`
- Task ID: `07171656-2101-0381-0000-5a6e2f944066`
- Cost: `$0.012000`
- Result: `items: 0`; `total_count` unavailable

Relevant Pages:

```json
[{"target":"usezenmail.com","location_code":2840,"language_code":"en","ignore_synonyms":true,"limit":50}]
```

- Endpoint: `dataforseo_labs/google/relevant_pages/live`
- Task ID: `07171657-2101-0385-0000-dc655289ee53`
- Cost: `$0.012000`
- Result: `items: 0`; `total_count` unavailable

### Backlinks

Summary:

```json
[{"target":"usezenmail.com","include_subdomains":true,"exclude_internal_backlinks":true}]
```

- Endpoint: `backlinks/summary/live`
- Task ID: `07171657-2101-0265-0000-b53275e18e04`
- Cost: `$0.024036`
- Result: no summary row

Detail:

```json
[{"target":"usezenmail.com","include_subdomains":true,"exclude_internal_backlinks":true,"mode":"one_per_domain","limit":200,"order_by":["rank,desc"]}]
```

- Endpoint: `backlinks/backlinks/live`
- Task ID: `07171658-2101-0269-0000-1b9c2e37f2ae`
- Cost: `$0.024036`
- Result: `total_count: 0`; `items: 0`

### Content Analysis

Exact domain:

```json
[{"keyword":"usezenmail.com","search_mode":"as_is","limit":100}]
```

- Endpoint: `content_analysis/search/live`
- Task ID: `07171658-2101-0463-0000-4d8f2ee8515f`
- Cost: `$0.024036`
- Result: `total_count: 0`; `items: 0`

Brand plus category:

```json
[{"keyword":"\"ZenMail\" Gmail","search_mode":"as_is","limit":100}]
```

- Endpoint: `content_analysis/search/live`
- Task ID: `07171658-2101-0463-0000-52f37e1d1dbd`
- Cost: `$0.024684`
- Result: `total_count: 19`; `items: 19`
- Interpretation: results were dominated by the older 2020 extension and
  unrelated ZenMail identities; they are not counted as current-product
  mentions

### Ads Transparency

Advertiser-name search:

```json
[{"keyword":"zenmail","location_code":2840}]
```

- Endpoint: `serp/google/ads_advertisers/live/advanced`
- Task ID: `07171658-2101-0139-0000-3547f03ac70f`
- Cost: `$0.002000`
- Result: status `40102`, “No Search Results”

Domain/creative search:

```json
[{"target":"usezenmail.com","location_code":2840,"platform":"all","format":"all","date_from":"2018-05-31","date_to":"2026-07-17","depth":40}]
```

- Endpoint: `serp/google/ads_search/live/advanced`
- Task ID: `07171659-2101-0139-0000-53ac92e29a50`
- Cost: `$0.002000`
- Result: no items

### Organic live SERPs

Every request used:

```json
[{"keyword":"[QUERY]","location_code":2840,"language_code":"en","device":"desktop","os":"windows","depth":10}]
```

Endpoint: `serp/google/organic/live/advanced`

| Query | Task ID | Cost | ZenMail result |
| --- | --- | ---: | --- |
| `zenmail email client` | `07171659-2101-0139-0000-382b7731e0d1` | $0.002000 | Homepage group rank 3, absolute rank 4 |
| `gmail client for mac` | `07171700-2101-0139-0000-72a4a495f06b` | $0.002000 | Absent from organic top 10 |
| `gmail keyboard shortcuts mac` | `07171700-2101-0139-0000-a0b9191fb277` | $0.002000 | Absent from organic top 10 |
| `mimestream vs zenmail` | `07171700-2101-0139-0000-68972c1a6cfd` | $0.002000 | Absent from organic top 10 |
| `best gmail client for mac` | `07171701-2101-0139-0000-09e4669f43d1` | $0.002000 | Absent from organic top 10 |

## Free task-ID recovery request

The first Ranked Keywords response was lost locally, so its audit identifiers
were recovered without another paid search request.

Method and endpoint:

```text
POST /v3/dataforseo_labs/id_list
```

Exact body:

```json
[{"datetime_from":"2026-07-17 13:55:00 +00:00","datetime_to":"2026-07-17 13:58:30 +00:00","limit":100,"offset":0,"sort":"asc","include_metadata":true}]
```

The provider returned status `20000` (`Ok`) at cost `$0`. The matching history
row had task ID `07171656-2101-0381-0000-569d1d8ce845`, endpoint
`dataforseo_labs/google/ranked_keywords/live`, posted/completed timestamp
`2026-07-17 13:56:34 +00:00`, status `20000`, and cost `$0.012000`. Its
metadata matched the exact initial Ranked Keywords body above. The retained
retry followed at `13:56:57 +00:00`.

## Direct public observations

| Surface | Method | Result |
| --- | --- | --- |
| Homepage | Public GET, HTML/metadata/client bundle, hero image inspection | Current message, feature/privacy claims, waitlist, PostHog wiring |
| About | Public GET | Independent one-person project; no founder name |
| Privacy | Public GET | Notion, Polar, PostHog, local-app data claims |
| Terms | Public GET | Early-access Gmail-only beta; Israel/Tel Aviv; no named entity |
| Newsroom/articles | Public GET and structured-data extraction | 15 posts, dates, metadata, claim conflicts |
| Robots/sitemap | Public GET | 20 URLs; broad search/AI crawler access |
| RSS | Repeated direct request | Advertised in markup; no successful content response during this pass |
| Waitlist | Static client inspection only | Request and event sequence; no submission |
| Hero image | Local visual inspection of public asset | Product-shaped three-pane Mac UI |
| Wayback CDX | Public index query | Empty result for the current domain |
| Reddit | Public search/result inspection | Repeated current recommendations from `snail207` |
| ZenMail comparison and Mimestream security page | Public first-party pages | Both describe direct Gmail API sync, local storage, and no intermediary sync server; ZenMail's broader comparisons remain uncited |

The main site, About, Privacy, Terms, Newsroom, robots, sitemap, and sampled
article URLs returned public content in the captured pass. A later RSS recheck
timed out and is reported as unverified rather than working or definitively
broken.

## Research boundaries

- No email address was submitted.
- No beta invitation was requested.
- No account, OAuth grant, installer, app execution, or payment was used.
- The in-app browser had no available browser session, so no rendered form
  interaction or responsive/layout test was performed.
- Public HTML, structured data, JavaScript bundles, legal text, image assets,
  public search results, and third-party indexes were inspected.
- Raw DataForSEO responses were not committed.
- One charged Ranked Keywords raw response was lost after a local formatter
  failure. Its task ID, request metadata, status, and cost were recovered from
  the free provider history endpoint; the cost remains included above.
- Exact-domain backlink/content indexes missed manually observed pages.
- Search and dynamic social results are point-in-time.

## Reliability rules

- A public claim is not a verified product capability.
- A page date is not proof of the first publication date.
- A rank is not a visit, and a visit is not a waitlist entry.
- A waitlist entry is not an invitation, activation, retained user, or sale.
- Repeated posts by one account are not multiple independent endorsements.
- Zero indexed backlinks are not proof that no links exist.
- No ads result in one US Google slice is not proof of no advertising.
- Analytics code proves measurement capability, not a working funnel report.
- No public evidence exposes actual source traffic, waitlist size, activation,
  retention, pricing conversion, or revenue.
