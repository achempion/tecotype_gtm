# DataForSEO request ledger

Requests were made on **2026-07-17**.

Search requests used Google, United States (`2840`), English, and
desktop/Windows where a device was required. Reusable endpoint, credential,
and budget guidance is in
[the central documentation](../../tools/dataforseo.md).

No credential was written to the repository or emitted in command output.
Every successful POST contained exactly one task object.

## Cost summary

| Request | Endpoint | Returned | Cost (USD) |
| --- | --- | ---: | ---: |
| Domain overview | `dataforseo_labs/google/domain_rank_overview/live` | 1 domain | 0.012120 |
| Ranked keywords | `dataforseo_labs/google/ranked_keywords/live` | all 13 rows | 0.013560 |
| Relevant pages | `dataforseo_labs/google/relevant_pages/live` | all 4 pages | 0.012480 |
| Backlink summary | `backlinks/summary/live` | 1 summary | 0.024036 |
| Backlinks, one/domain | `backlinks/backlinks/live` | 200 of 1,094 rows | 0.031200 |
| Content search | `content_analysis/search/live` | 100 of 161,691 rows | 0.027600 |
| Four live organic SERPs | `serp/google/organic/live/advanced` | 4 result pages | 0.008000 |
| Ads advertiser lookup | `serp/google/ads_advertisers/live/advanced` | no search results | 0.002000 |
| Ads creative lookup | `serp/google/ads_search/live/advanced` | no search results | 0.002000 |
| **Total** | **12 billed tasks** |  | **0.132996** |

The **$0.132996** total is below the confirmed **$2 per-competitor budget**.
The per-competitor budget is the governing limit; the Wave 3 aggregate is not a
combined cap.

Advertising tasks with no returned result were still billed. They establish
only that those specific archive requests returned no result.

## Exact request bodies

### Domain overview

```json
[
  {
    "target": "newtonhq.com",
    "location_code": 2840,
    "language_code": "en",
    "ignore_synonyms": true
  }
]
```

### Ranked keywords

```json
[
  {
    "target": "newtonhq.com",
    "location_code": 2840,
    "language_code": "en",
    "ignore_synonyms": true,
    "item_types": ["organic", "paid"],
    "limit": 250,
    "order_by": ["keyword_data.keyword_info.search_volume,desc"]
  }
]
```

### Relevant pages

```json
[
  {
    "target": "newtonhq.com",
    "location_code": 2840,
    "language_code": "en",
    "ignore_synonyms": true,
    "limit": 50,
    "order_by": ["metrics.organic.etv,desc"]
  }
]
```

### Backlink summary

```json
[
  {
    "target": "newtonhq.com",
    "include_subdomains": true,
    "exclude_internal_backlinks": true
  }
]
```

### Backlink detail

```json
[
  {
    "target": "newtonhq.com",
    "include_subdomains": true,
    "exclude_internal_backlinks": true,
    "mode": "one_per_domain",
    "limit": 200,
    "order_by": ["rank,desc"]
  }
]
```

### Content Analysis

```json
[
  {
    "keyword": "Newton Mail",
    "search_mode": "as_is",
    "limit": 100
  }
]
```

### Live organic SERP: `newton mail`

```json
[
  {
    "keyword": "newton mail",
    "location_code": 2840,
    "language_code": "en",
    "device": "desktop",
    "os": "windows",
    "depth": 10
  }
]
```

### Live organic SERP: `newton mail alternative`

```json
[
  {
    "keyword": "newton mail alternative",
    "location_code": 2840,
    "language_code": "en",
    "device": "desktop",
    "os": "windows",
    "depth": 10
  }
]
```

### Live organic SERP: `best email client for professionals`

```json
[
  {
    "keyword": "best email client for professionals",
    "location_code": 2840,
    "language_code": "en",
    "device": "desktop",
    "os": "windows",
    "depth": 10
  }
]
```

### Live organic SERP: `calm email client`

```json
[
  {
    "keyword": "calm email client",
    "location_code": 2840,
    "language_code": "en",
    "device": "desktop",
    "os": "windows",
    "depth": 10
  }
]
```

### Google Ads advertiser lookup

```json
[
  {
    "keyword": "newton mail",
    "location_code": 2840
  }
]
```

### Google Ads creative lookup

```json
[
  {
    "target": "newtonhq.com",
    "location_code": 2840,
    "platform": "all",
    "format": "all",
    "date_from": "2018-05-31",
    "date_to": "2026-07-17",
    "depth": 40
  }
]
```

## Audit identifiers

| Request | Task ID | Status | Task cost |
| --- | --- | ---: | ---: |
| Domain overview | `07172052-2101-0388-0000-b74dcd2d1a78` | 20000 | 0.012120 |
| Ranked keywords | `07172053-2101-0381-0000-4195a442e7d5` | 20000 | 0.013560 |
| Relevant pages | `07172053-2101-0385-0000-d4748074b066` | 20000 | 0.012480 |
| Backlink summary | `07172054-2101-0265-0000-3ea585ecba02` | 20000 | 0.024036 |
| Backlink detail | `07172054-2101-0269-0000-ff9d592717f7` | 20000 | 0.031200 |
| Content Analysis | `07172054-2101-0463-0000-941b69c79f71` | 20000 | 0.027600 |
| SERP: `newton mail` | `07172055-2101-0139-0000-5a4a6c23ee7d` | 20000 | 0.002000 |
| SERP: `newton mail alternative` | `07172055-2101-0139-0000-5b4b159719eb` | 20000 | 0.002000 |
| SERP: `best email client for professionals` | `07172056-2101-0139-0000-4b99451f53c2` | 20000 | 0.002000 |
| SERP: `calm email client` | `07172056-2101-0139-0000-3161f0106533` | 20000 | 0.002000 |
| Ads advertisers | `07172057-2101-0139-0000-8a7094b2c649` | 40102 | 0.002000 |
| Ads creatives | `07172057-2101-0139-0000-d9d32767c0e5` | 40102 | 0.002000 |

## Extracted results

### Domain and keywords

- 13 organic keywords and 132.40000120922923 ETV;
- no paid keywords or paid ETV;
- three position-one rows, two rows at 21–30, three at 31–40, two at
  41–50, one at 51–60, one at 71–80, and one at 91–100;
- five new, five improved, and two declined rows; and
- `newton email`, `newton mail`, and `cloudmagic newton` supplied 130.72
  ETV.

### Relevant pages

- homepage: four keywords and 130.8250012174 ETV;
- snooze article: four keywords and 0.7979999855 ETV;
- account subdomain: four keywords and 0.4830000065 ETV; and
- Mac page: one keyword and 0.294 ETV.

### Backlinks

- rank 247;
- 3,485 backlinks;
- 2,938 referring pages;
- 1,123 referring domains;
- 1,050 referring main domains;
- 1,973 broken backlinks;
- four broken pages; and
- 741 nofollow referring pages.

The 200-row detail sample included relevant press and community sources,
historical shutdown/return coverage, integrations, Product Hunt, directories,
scrapers, software databases, unsafe download-related pages, and spam. Only
sources whose public context was independently inspectable were used as
evidence.

### Content Analysis

The endpoint reported 161,691 possible `Newton Mail` results and returned the
first 100 under the requested ordering. The sample mixed credible shutdown
coverage with duplication, multilingual copies, generic pages, directories,
and suspicious 2026 “trending” content.

The reported total is not a press count, audience count, demand measure, or
traffic estimate. No conclusion in the dossier relies on that total as
adoption evidence.

### Live SERPs

- `newton mail`: official homepage first, followed by store, reference,
  integration, video, community, editorial, and social results;
- `newton mail alternative`: competitor and community pages; no Newton-owned
  page in the checked top results;
- `best email client for professionals`: editorial and competitor pages; no
  Newton-owned page in the checked top ten; and
- `calm email client`: mostly Calm-brand and general email results; no
  Newton-owned page in the checked top ten.

## Output and extraction record

Responses were parsed in memory and were not retained as repository artifacts.
This ledger preserves every request body, task ID, task status, cost, returned
limit, and aggregate used in the dossier.

Limits:

- keyword and ETV values are modeled US-English estimates;
- ranked keywords returned all 13 reported rows;
- relevant pages returned all four reported rows;
- backlink detail returned 200 of 1,094 one-per-domain rows ordered by
  provider rank;
- content search returned 100 of 161,691 reported results;
- live SERPs are point-in-time result pages and may vary by location or
  personalization;
- a backlink or mention does not establish a visit; and
- none of the endpoints exposes Newton activation, payment, retention, or
  renewal.

## Public-web and artifact-boundary record

Inspected as public webpages or metadata:

- homepage and rendered DOM;
- official 2019, 2020, and 2026 announcements;
- public pricing, privacy, terms, and about surfaces;
- Apple App Store and Google Play listings;
- Product Hunt page;
- independent press, reviews, community discussions, integrations, and
  alternative pages; and
- the public UserJot changelog destination, which returned a missing-page
  state.

Deliberately not performed:

- following a direct client, installer, disk-image, executable, archive,
  release-asset, or update-payload route;
- downloading, fetching, opening, mounting, installing, executing, or
  inspecting any Newton client or artifact;
- checking out or cloning source;
- using an app-store install control;
- submitting the request-access form;
- creating an account or authenticating a mailbox;
- entering a trial, checkout, subscription, or payment flow; or
- using private analytics or authenticated customer data.
