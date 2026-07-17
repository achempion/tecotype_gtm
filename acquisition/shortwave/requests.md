# Shortwave DataForSEO request ledger

Requests were made on **2026-07-17**.

Search requests used Google, United States (`2840`), English, and
desktop/Windows where a device was required. Reusable endpoint and credential
guidance belongs in the central
[DataForSEO documentation](../../tools/dataforseo.md).

No credential was written to a repository file or this report. The configured
credential was read from the system credential store and passed only to
curl's Basic-auth handling. Every billed Live POST contained exactly **one
task object**.

## Final-pass cost summary

| Request | Endpoint | Returned | Cost (USD) |
| --- | --- | ---: | ---: |
| Authorization-format failure | Domain overview endpoint | Top-level `40100`; no task ID and no billed task | 0.000000 |
| Domain overview | `dataforseo_labs/google/domain_rank_overview/live` | 1 domain | 0.012120 |
| Ranked keywords | `dataforseo_labs/google/ranked_keywords/live` | 250 of 452 rows | 0.042000 |
| Relevant pages, initial | `dataforseo_labs/google/relevant_pages/live` | 21 of 21 rows; URL projection omitted | 0.014520 |
| Relevant pages, extraction recovery | `dataforseo_labs/google/relevant_pages/live` | 21 of 21 rows | 0.014520 |
| Backlink summary, initial | `backlinks/summary/live` | 1 result; metric projection omitted | 0.024036 |
| Backlink summary, extraction recovery | `backlinks/summary/live` | 1 result | 0.024036 |
| Backlinks, one/domain | `backlinks/backlinks/live` | 200 of 1,915 rows | 0.031200 |
| Content Analysis | `content_analysis/search/live` | 100 of 13,143 possible rows | 0.027600 |
| Four live organic SERPs | `serp/google/organic/live/advanced` | 4 result pages | 0.008000 |
| Ads advertiser lookup | `serp/google/ads_advertisers/live/advanced` | no search results | 0.002000 |
| Ads creative lookup | `serp/google/ads_search/live/advanced` | 25 creatives | 0.002000 |
| **Final-pass total** | **14 billed tasks** |  | **0.202032** |

An audit then found 11 earlier same-day Shortwave tasks in the shared temporary
workspace. Counting both passes gives **25 charged tasks and $0.363508
all-in**. No new paid request was made to reconstruct or verify the earlier
ledger. The audited all-in spend is below the user-confirmed **$2
per-competitor budget**.

## Earlier same-day pass found during audit

The earlier response files predate the final pass and substantially overlap
it. They are included because they targeted the same client and were charged
on the same research date.

| Request | Task ID | Task status | Returned | Cost |
| --- | --- | --- | --- | ---: |
| Domain overview | `07171854-2101-0388-0000-271cc0e43d22` | `20000 Ok.` | 1 domain | 0.012120 |
| Ranked keywords | `07171854-2101-0381-0000-8d3319981d71` | `20000 Ok.` | 250 of 452 rows | 0.042000 |
| Relevant pages | `07171854-2101-0385-0000-91f526fb2674` | `20000 Ok.` | 21 of 21 rows | 0.014520 |
| Backlink summary | `07171854-2101-0265-0000-7dde3553173c` | `20000 Ok.` | 1 summary | 0.024036 |
| Backlinks, one/domain | `07171855-2101-0269-0000-e3653c695a64` | `20000 Ok.` | 200 of 1,915 rows | 0.031200 |
| Content Analysis | `07171855-2101-0463-0000-d739c52f9702` | `20000 Ok.` | 100 of 13,143 possible rows | 0.027600 |
| SERP: `shortwave email client` | `07171856-2101-0139-0000-3ab6674e7c7f` | `20000 Ok.` | 1 result page | 0.002000 |
| SERP: `ai powered email client` | `07171856-2101-0139-0000-270d7daa1929` | `20000 Ok.` | 1 result page | 0.002000 |
| SERP: `shortwave vs superhuman` | `07171856-2101-0139-0000-979926bd5cd8` | `20000 Ok.` | 1 result page | 0.002000 |
| Ads advertiser lookup | `07171855-2101-0139-0000-b986c12a39d5` | `40102 No Search Results.` | No advertiser result | 0.002000 |
| Ads creative lookup | `07171855-2101-0139-0000-0392e064c23b` | `20000 Ok.` | 25 creatives | 0.002000 |
| **Earlier-pass total** |  |  | **11 charged tasks** | **0.161476** |

The final-pass and earlier-pass arithmetic is:

```text
$0.202032 final pass
+0.161476 earlier pass
----------
 $0.363508 all-in across 25 charged tasks
```

## Failures, duplicates, and audit disclosure

The first domain-overview attempt sent the correct one-object body but used an
authorization-header shell form that DataForSEO rejected at the top level with
`40100`. It returned no task ID and cost $0. The credential was then passed to
curl's Basic-auth handling; it was never printed or stored.

Relevant Pages was billed twice with the same valid body. The initial response
was successful, but the local projection requested `page` instead of the
documented `page_address`, leaving URLs out of the compact output. The second
call recovered the URLs.

Backlink Summary was also billed twice with the same valid body. The initial
projection assumed an `items` wrapper, while this endpoint returns the summary
directly in `result[0]`. The second call recovered the metrics.

Both recovery calls are retained in the final-pass cost and audit ledger rather
than hidden. There were no other malformed paid calls in that pass. The
separate earlier pass found during audit created additional overlap across the
domain, keyword, page, backlink, mention, AI-category SERP, and ad lookups; its
full cost is also retained above rather than omitted.

The Ads Advertisers task returned API task status `40102` (“No Search Results”)
inside a billed envelope. The creative search separately returned 25 results
for the domain. These are different searches and are not contradictory.

No further Shortwave paid request was made after the all-in spend was
reconciled.

## Exact request bodies

### Domain overview

Endpoint:
`dataforseo_labs/google/domain_rank_overview/live`

The unbilled authorization failure and the successful task used this body:

```json
[
  {
    "target": "shortwave.com",
    "location_code": 2840,
    "language_code": "en",
    "ignore_synonyms": true
  }
]
```

### Ranked keywords

Endpoint: `dataforseo_labs/google/ranked_keywords/live`

```json
[
  {
    "target": "shortwave.com",
    "location_code": 2840,
    "language_code": "en",
    "ignore_synonyms": true,
    "item_types": ["organic", "paid"],
    "limit": 250,
    "order_by": ["keyword_data.keyword_info.search_volume,desc"]
  }
]
```

### Relevant pages, initial and recovery calls

Endpoint: `dataforseo_labs/google/relevant_pages/live`

Each of the two calls used:

```json
[
  {
    "target": "shortwave.com",
    "location_code": 2840,
    "language_code": "en",
    "ignore_synonyms": true,
    "limit": 50,
    "order_by": ["metrics.organic.etv,desc"]
  }
]
```

### Backlink summary, initial and recovery calls

Endpoint: `backlinks/summary/live`

Each of the two calls used:

```json
[
  {
    "target": "shortwave.com",
    "include_subdomains": true,
    "exclude_internal_backlinks": true
  }
]
```

### Backlink detail

Endpoint: `backlinks/backlinks/live`

```json
[
  {
    "target": "shortwave.com",
    "include_subdomains": true,
    "exclude_internal_backlinks": true,
    "mode": "one_per_domain",
    "limit": 200,
    "order_by": ["rank,desc"]
  }
]
```

### Content Analysis

Endpoint: `content_analysis/search/live`

```json
[
  {
    "keyword": "Shortwave email",
    "search_mode": "as_is",
    "limit": 100
  }
]
```

### Live organic SERP: `shortwave email`

Endpoint: `serp/google/organic/live/advanced`

```json
[
  {
    "keyword": "shortwave email",
    "location_code": 2840,
    "language_code": "en",
    "device": "desktop",
    "os": "windows",
    "depth": 10
  }
]
```

### Live organic SERP: `ai powered email client`

Endpoint: `serp/google/organic/live/advanced`

```json
[
  {
    "keyword": "ai powered email client",
    "location_code": 2840,
    "language_code": "en",
    "device": "desktop",
    "os": "windows",
    "depth": 10
  }
]
```

### Live organic SERP: `inbox by gmail alternative`

Endpoint: `serp/google/organic/live/advanced`

```json
[
  {
    "keyword": "inbox by gmail alternative",
    "location_code": 2840,
    "language_code": "en",
    "device": "desktop",
    "os": "windows",
    "depth": 10
  }
]
```

### Live organic SERP: `email batching app`

Endpoint: `serp/google/organic/live/advanced`

```json
[
  {
    "keyword": "email batching app",
    "location_code": 2840,
    "language_code": "en",
    "device": "desktop",
    "os": "windows",
    "depth": 10
  }
]
```

### Google Ads advertiser lookup

Endpoint: `serp/google/ads_advertisers/live/advanced`

```json
[
  {
    "keyword": "shortwave email",
    "location_code": 2840
  }
]
```

### Google Ads creative lookup

Endpoint: `serp/google/ads_search/live/advanced`

```json
[
  {
    "target": "shortwave.com",
    "location_code": 2840,
    "platform": "all",
    "format": "all",
    "date_from": "2018-05-31",
    "date_to": "2026-07-17",
    "depth": 40
  }
]
```

## Earlier-pass parameter variants

The earlier Domain Overview, Ranked Keywords, Backlink Summary, Backlink
Detail, and Content Analysis tasks used the exact bodies documented above.
The remaining earlier bodies differed as follows.

### Earlier relevant pages

The earlier request omitted the final pass's ETV ordering:

```json
[
  {
    "target": "shortwave.com",
    "location_code": 2840,
    "language_code": "en",
    "ignore_synonyms": true,
    "limit": 50
  }
]
```

Endpoint: `dataforseo_labs/google/relevant_pages/live`

### Earlier live organic SERPs

Each earlier SERP was a separate one-object POST using this exact structure:

```json
[
  {
    "keyword": "QUERY",
    "location_code": 2840,
    "language_code": "en",
    "device": "desktop",
    "os": "windows",
    "depth": 10
  }
]
```

Endpoint: `serp/google/organic/live/advanced`

`QUERY` was exactly one of:

- `shortwave email client`;
- `ai powered email client`; or
- `shortwave vs superhuman`.

### Earlier Google Ads advertiser lookup

```json
[
  {
    "keyword": "shortwave email",
    "location_code": 2840,
    "device": "desktop",
    "os": "windows"
  }
]
```

Endpoint: `serp/google/ads_advertisers/live/advanced`

### Earlier Google Ads creative lookup

```json
[
  {
    "target": "shortwave.com",
    "location_code": 2840,
    "platform": "all",
    "format": "all",
    "date_from": "2018-05-31",
    "date_to": "2026-07-17",
    "depth": 40,
    "device": "desktop",
    "os": "windows"
  }
]
```

Endpoint: `serp/google/ads_search/live/advanced`

## Final-pass audit identifiers

| Request | Task ID | Task status | Task cost |
| --- | --- | --- | ---: |
| Authorization-format failure | No task ID | Top-level `40100` | 0.000000 |
| Domain overview | `07171937-2101-0388-0000-01287406008d` | `20000 Ok.` | 0.012120 |
| Ranked keywords | `07171938-2101-0381-0000-b42521548c60` | `20000 Ok.` | 0.042000 |
| Relevant pages, initial | `07171938-2101-0385-0000-ae2d290a8cf6` | `20000 Ok.` | 0.014520 |
| Relevant pages, recovery | `07171939-2101-0385-0000-5a2a5a7fde9f` | `20000 Ok.` | 0.014520 |
| Backlink summary, initial | `07171939-2101-0265-0000-941cc0253104` | `20000 Ok.` | 0.024036 |
| Backlink summary, recovery | `07171940-2101-0265-0000-96248ff01a83` | `20000 Ok.` | 0.024036 |
| Backlink detail | `07171940-2101-0269-0000-47d9f40a5892` | `20000 Ok.` | 0.031200 |
| Content Analysis | `07171941-2101-0463-0000-6c35b40a4d4c` | `20000 Ok.` | 0.027600 |
| SERP: `shortwave email` | `07171941-2101-0139-0000-a2a91836e7fc` | `20000 Ok.` | 0.002000 |
| SERP: `ai powered email client` | `07171942-2101-0139-0000-cae95ef7b4ed` | `20000 Ok.` | 0.002000 |
| SERP: `inbox by gmail alternative` | `07171942-2101-0139-0000-e68c6d484f09` | `20000 Ok.` | 0.002000 |
| SERP: `email batching app` | `07171942-2101-0139-0000-8841c6ea4ac7` | `20000 Ok.` | 0.002000 |
| Ads advertisers | `07171943-2101-0139-0000-ff03b140f5b9` | `40102 No Search Results.` | 0.002000 |
| Ads creatives | `07171943-2101-0139-0000-f2b8a4c80f62` | `20000 Ok.` | 0.002000 |

## Evidence limits

- Domain, keyword, page, and ETV metrics are modeled, not Shortwave analytics.
- A backlink or mention does not prove a visit, signup, or commercial
  relationship.
- Content Analysis includes stores, copied material, directories, and
  unofficial package pages; no client artifact from those results was
  obtained.
- An ad archive proves creatives existed, not spend, impressions, targeting,
  or performance.
- Live US desktop SERPs are point-in-time results and can vary.
- No API result exposes inbox connection, first value, return, payment,
  renewal, CAC, LTV, or profitability.
