# DataForSEO request ledger

Requests were made on **2026-07-17**.

Search requests used Google, United States (`2840`), English, and
desktop/Windows where a device was required. Reusable endpoint and credential
guidance is in [the central documentation](../../tools/dataforseo.md).

No credential was written to the repository or emitted in command output.
Every subsequent live POST contained exactly one task object. The first domain
overview POST mistakenly contained two objects; DataForSEO processed HEY and
rejected the second MailMate object at zero cost. Both task results are
retained below.

## Cost summary

| Request | Endpoint | Returned | Cost (USD) |
| --- | --- | ---: | ---: |
| Domain overview | `dataforseo_labs/google/domain_rank_overview/live` | 1 domain | 0.012120 |
| Ranked keywords | `dataforseo_labs/google/ranked_keywords/live` | 250 of 4,375 rows | 0.042000 |
| Relevant pages | `dataforseo_labs/google/relevant_pages/live` | 50 of 1,097 rows | 0.018000 |
| Backlink summary | `backlinks/summary/live` | 1 summary | 0.024036 |
| Backlinks, one/domain | `backlinks/backlinks/live` | 100 of 8,674 rows | 0.027600 |
| Exact-domain content search | `content_analysis/search/live` | 50 of 2,878 rows | 0.025800 |
| Two live organic SERPs | `serp/google/organic/live/advanced` | 2 result pages | 0.004000 |
| Ads advertiser lookup | `serp/google/ads_advertisers/live/advanced` | no search results | 0.002000 |
| Ads creative lookup | `serp/google/ads_search/live/advanced` | no search results | 0.002000 |
| **Total** | 10 billed tasks |  | **0.157556** |

The **$0.157556** total is below the confirmed **$2 per-competitor budget** and
is included in the Wave 2 aggregate research spend. Both advertising tasks
returned task status `40102` inside billed task envelopes. That is no result
for the requested coverage, not proof of historical absence.

## Exact request bodies

### Domain overview

This initial POST mistakenly included two task objects:

```json
[
  {
    "target": "hey.com",
    "location_code": 2840,
    "language_code": "en",
    "ignore_synonyms": true
  },
  {
    "target": "freron.com",
    "location_code": 2840,
    "language_code": "en",
    "ignore_synonyms": true
  }
]
```

HEY succeeded. The second task was rejected with status `40000`, “You can set
only one task at a time,” and cost $0. Its identifier is recorded in the
MailMate ledger.

### Ranked keywords

```json
[
  {
    "target": "hey.com",
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
    "target": "hey.com",
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
    "target": "hey.com",
    "include_subdomains": true,
    "exclude_internal_backlinks": true
  }
]
```

### Backlink detail

```json
[
  {
    "target": "hey.com",
    "include_subdomains": true,
    "exclude_internal_backlinks": true,
    "mode": "one_per_domain",
    "limit": 100,
    "order_by": ["rank,desc"]
  }
]
```

### Content Analysis

```json
[
  {
    "keyword": "hey.com",
    "search_mode": "as_is",
    "limit": 50
  }
]
```

### Live organic SERP: `hey email service`

```json
[
  {
    "keyword": "hey email service",
    "location_code": 2840,
    "language_code": "en",
    "device": "desktop",
    "os": "windows",
    "depth": 10
  }
]
```

### Live organic SERP: `gmail alternative email service`

```json
[
  {
    "keyword": "gmail alternative email service",
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
    "keyword": "hey email service",
    "location_code": 2840
  }
]
```

### Google Ads creative lookup

```json
[
  {
    "target": "hey.com",
    "location_code": 2840,
    "platform": "all",
    "format": "all",
    "date_from": "2019-01-01",
    "date_to": "2026-07-17",
    "depth": 40
  }
]
```

## Audit identifiers

| Request | Task ID | Status | Task cost |
| --- | --- | ---: | ---: |
| Domain overview | `07171856-2101-0388-0000-37a9fa3995f1` | 20000 | 0.012120 |
| Ranked keywords | `07171856-2101-0381-0000-7cce8669f458` | 20000 | 0.042000 |
| Relevant pages | `07171909-2101-0385-0000-a03c93352aa8` | 20000 | 0.018000 |
| Backlink summary | `07171909-2101-0265-0000-d09127868efb` | 20000 | 0.024036 |
| Backlink detail | `07171909-2101-0269-0000-3c849202c6b7` | 20000 | 0.027600 |
| Content Analysis | `07171911-2101-0463-0000-0035cf3cd7fe` | 20000 | 0.025800 |
| SERP: `hey email service` | `07171911-2101-0139-0000-54ba273858b5` | 20000 | 0.002000 |
| SERP: `gmail alternative email service` | `07171911-2101-0139-0000-8e971b4ce83f` | 20000 | 0.002000 |
| Ads advertisers | `07171912-2101-0139-0000-71d9d9a1e651` | 40102 | 0.002000 |
| Ads creatives | `07171913-2101-0139-0000-20dcdeb79a58` | 40102 | 0.002000 |

## Output and extraction record

Responses were parsed in memory and were not retained as repository artifacts.
This report retains the complete request body, task ID, status, cost, returned
limit, and every aggregate used in the analysis.

Important limits:

- Ranked Keywords returned the first 250 of 4,375 rows, ordered by search
  volume.
- Relevant Pages returned the first 50 of 1,097 pages, ordered by organic ETV.
- Backlink detail returned 100 of 8,674 one-per-domain rows, ordered by
  provider rank.
- Content Analysis returned 50 of 2,878 rows and mixed useful coverage with
  duplication, unrelated address mentions, and low-value pages.
- Backlink and search estimates combine `www.hey.com` with HEY World.

## Public-web inspection record

The homepage, pricing, FAQ, HEY Way, How It Works, migration guide, Apple
archive, and unauthenticated signup page were inspected as public pages. Public
website scripts were read to identify measurement behavior.

Deliberately not performed:

- client or installer download;
- app-artifact fetch or static inspection;
- app installation, mount, launch, or execution;
- account creation;
- signup continuation;
- email-address reservation;
- Gmail or another mailbox authorization;
- trial start;
- newsletter submission; or
- checkout.
