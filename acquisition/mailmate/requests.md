# DataForSEO request ledger

Requests were made on **2026-07-17**.

Search requests used Google, United States (`2840`), English, and
desktop/Windows where a device was required. Reusable endpoint and credential
guidance is in [the central documentation](../../tools/dataforseo.md).

No credential was written to the repository or emitted in command output.
All successful MailMate POSTs contained exactly one task object. Two zero-cost
validation failures are documented rather than omitted.

## Cost summary

| Request | Endpoint | Returned | Cost (USD) |
| --- | --- | ---: | ---: |
| Domain overview | `dataforseo_labs/google/domain_rank_overview/live` | 1 domain | 0.012120 |
| Ranked keywords | `dataforseo_labs/google/ranked_keywords/live` | all 17 rows | 0.014040 |
| Relevant pages | `dataforseo_labs/google/relevant_pages/live` | all 7 pages | 0.012840 |
| Backlink summary | `backlinks/summary/live` | 1 summary | 0.024036 |
| Backlinks, one/domain | `backlinks/backlinks/live` | 100 of 623 rows | 0.027600 |
| Content search | `content_analysis/search/live` | 50 of 438 rows | 0.025800 |
| Two live organic SERPs | `serp/google/organic/live/advanced` | 2 result pages | 0.004000 |
| Ads advertiser lookup | `serp/google/ads_advertisers/live/advanced` | no search results | 0.002000 |
| Ads creative lookup | `serp/google/ads_search/live/advanced` | no search results | 0.002000 |
| **Total** | 10 billed tasks |  | **0.124436** |

The **$0.124436** total is below the confirmed **$2 per-competitor budget** and
is included in the Wave 2 aggregate research spend. Advertising tasks with no
results were still billed. They are not proof that advertising never occurred.

## Zero-cost validation failures

1. The initial domain-overview POST contained HEY and MailMate objects.
   DataForSEO processed HEY and rejected MailMate with status `40000`, “You
   can set only one task at a time,” at cost $0. MailMate was then sent alone.
2. The first creative-archive body used a `date_from` before the endpoint's
   supported boundary. It returned status `40501`, “Invalid Field:
   'date_from',” at cost $0. The request was corrected to `2018-05-31`.

## Exact request bodies

### Rejected domain-overview object

It was the second object in this mistaken initial POST:

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

### Corrected domain overview

```json
[
  {
    "target": "freron.com",
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
    "target": "freron.com",
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
    "target": "freron.com",
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
    "target": "freron.com",
    "include_subdomains": true,
    "exclude_internal_backlinks": true
  }
]
```

### Backlink detail

```json
[
  {
    "target": "freron.com",
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
    "keyword": "mailmate email client",
    "search_mode": "as_is",
    "limit": 50
  }
]
```

### Live organic SERP: `mailmate email client`

```json
[
  {
    "keyword": "mailmate email client",
    "location_code": 2840,
    "language_code": "en",
    "device": "desktop",
    "os": "windows",
    "depth": 10
  }
]
```

### Live organic SERP: `keyboard email client mac`

```json
[
  {
    "keyword": "keyboard email client mac",
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
    "keyword": "mailmate email client",
    "location_code": 2840
  }
]
```

### Invalid Google Ads creative lookup

```json
[
  {
    "target": "freron.com",
    "location_code": 2840,
    "platform": "all",
    "format": "all",
    "date_from": "2010-01-26",
    "date_to": "2026-07-17",
    "depth": 40
  }
]
```

### Corrected Google Ads creative lookup

```json
[
  {
    "target": "freron.com",
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
| Rejected overview object | `07171856-2101-0388-0000-eade9574d385` | 40000 | 0 |
| Domain overview | `07171856-2101-0388-0000-4c51bf839c0e` | 20000 | 0.012120 |
| Ranked keywords | `07171908-2101-0381-0000-083c9cb953f3` | 20000 | 0.014040 |
| Relevant pages | `07171909-2101-0385-0000-5434a0fd7a03` | 20000 | 0.012840 |
| Backlink summary | `07171909-2101-0265-0000-961f578181c9` | 20000 | 0.024036 |
| Backlink detail | `07171910-2101-0269-0000-2ba78faf93e9` | 20000 | 0.027600 |
| Content Analysis | `07171911-2101-0463-0000-0489387727b1` | 20000 | 0.025800 |
| SERP: `mailmate email client` | `07171912-2101-0139-0000-516ff6f6da7f` | 20000 | 0.002000 |
| SERP: `keyboard email client mac` | `07171912-2101-0139-0000-22136c1dbc3e` | 20000 | 0.002000 |
| Ads advertisers | `07171913-2101-0139-0000-d80977e977c3` | 40102 | 0.002000 |
| Invalid ads creative | `07171914-2101-0139-0000-6ac3ea46bdc2` | 40501 | 0 |
| Ads creatives | `07171914-2101-0139-0000-9f1b4dd62dc7` | 40102 | 0.002000 |

## Output and extraction record

Responses were parsed in memory and were not retained as repository artifacts.
This ledger preserves every request body, task ID, status, cost, returned
limit, and aggregate used in the analysis.

Limits:

- Ranked Keywords returned all 17 reported rows.
- Relevant Pages returned all seven reported pages.
- Backlink detail returned 100 of 623 one-per-domain rows ordered by provider
  rank.
- Content Analysis returned 50 of 438 results and included old, duplicated,
  scraped, and unsafe download-related pages.
- Search and backlink metrics do not expose visits or customer attribution.

## Public-web inspection record

The homepage, pricing, support, privacy, EULA, download options, blog posts,
and release notes were inspected as public webpages. The visible download
destination was not fetched.

Deliberately not performed:

- client, beta, stable-release, disk-image, or update-payload download;
- artifact header/body fetch;
- mount, extraction, static inspection, installation, launch, or execution;
- IMAP/SMTP account configuration;
- trial use;
- license creation;
- subscription or checkout; or
- contact, feedback, mailing-list, or payment form submission.
