# Orchid DataForSEO request ledger

Requests were made on **2026-07-17**.

Search requests used Google, United States (`2840`), English, and
desktop/Windows for SERPs. Reusable endpoint and credential guidance is in
[the central documentation](../../tools/dataforseo.md).

No credential was written to the repository or emitted in command output.
Every billed Live POST contained exactly **one task object**. All 12 tasks
returned top-level and task-level status `20000 Ok.` There were no malformed,
failed, or duplicate paid calls in this pass.

## Cost summary

| # | Request | Returned | Cost (USD) |
| ---: | --- | ---: | ---: |
| 1 | `0.email` domain overview | 1 domain | 0.012120 |
| 2 | `0.email` ranked keywords | all 76 rows | 0.021120 |
| 3 | `0.email` relevant pages | all 6 pages | 0.012720 |
| 4 | `0.email` backlink summary | 1 summary | 0.024036 |
| 5 | `0.email` backlinks, one/domain | 100 of 373 rows | 0.027600 |
| 6 | `orchid.ai` domain overview | 1 domain | 0.012120 |
| 7 | `orchid.ai` ranked keywords | all 8 rows | 0.012960 |
| 8 | `orchid.ai` relevant pages | all 2 pages | 0.012240 |
| 9 | `orchid.ai` backlink summary | 1 summary | 0.024036 |
| 10 | `orchid.ai` backlinks, one/domain | 63 of 66 rows | 0.026268 |
| 11 | Live SERP: `zero email client` | 1 result page | 0.002000 |
| 12 | Live SERP: `orchid personal assistant` | 1 result page | 0.002000 |
|  | **Audited total** | **12 billed tasks** | **0.189220** |

The audited total is below the confirmed **$2 per-competitor budget**.

## Audit identifiers

| # | Task ID | Status | Cost |
| ---: | --- | --- | ---: |
| 1 | `07172056-2101-0388-0000-ac226d4df69f` | `20000 Ok.` | 0.012120 |
| 2 | `07172056-2101-0381-0000-431ef375e097` | `20000 Ok.` | 0.021120 |
| 3 | `07172056-2101-0385-0000-7d6ee64f2519` | `20000 Ok.` | 0.012720 |
| 4 | `07172056-2101-0265-0000-8a08b3b3611a` | `20000 Ok.` | 0.024036 |
| 5 | `07172056-2101-0269-0000-0ca9262d2124` | `20000 Ok.` | 0.027600 |
| 6 | `07172056-2101-0388-0000-0aff1cdc4f55` | `20000 Ok.` | 0.012120 |
| 7 | `07172056-2101-0381-0000-397aa6653317` | `20000 Ok.` | 0.012960 |
| 8 | `07172056-2101-0385-0000-88678140b717` | `20000 Ok.` | 0.012240 |
| 9 | `07172056-2101-0265-0000-4cb8b9c63b4c` | `20000 Ok.` | 0.024036 |
| 10 | `07172056-2101-0269-0000-97f743804f12` | `20000 Ok.` | 0.026268 |
| 11 | `07172056-2101-0139-0000-960e59236dd3` | `20000 Ok.` | 0.002000 |
| 12 | `07172057-2101-0139-0000-99dd3b289ea3` | `20000 Ok.` | 0.002000 |

## Exact request bodies

### 1. `0.email` domain overview

Endpoint: `dataforseo_labs/google/domain_rank_overview/live`

```json
[
  {
    "target": "0.email",
    "location_code": 2840,
    "language_code": "en",
    "ignore_synonyms": true
  }
]
```

### 2. `0.email` ranked keywords

Endpoint: `dataforseo_labs/google/ranked_keywords/live`

```json
[
  {
    "target": "0.email",
    "location_code": 2840,
    "language_code": "en",
    "ignore_synonyms": true,
    "item_types": ["organic", "paid"],
    "limit": 250,
    "order_by": ["keyword_data.keyword_info.search_volume,desc"]
  }
]
```

### 3. `0.email` relevant pages

Endpoint: `dataforseo_labs/google/relevant_pages/live`

```json
[
  {
    "target": "0.email",
    "location_code": 2840,
    "language_code": "en",
    "ignore_synonyms": true,
    "limit": 50,
    "order_by": ["metrics.organic.etv,desc"]
  }
]
```

### 4. `0.email` backlink summary

Endpoint: `backlinks/summary/live`

```json
[
  {
    "target": "0.email",
    "include_subdomains": true,
    "exclude_internal_backlinks": true
  }
]
```

### 5. `0.email` backlink detail

Endpoint: `backlinks/backlinks/live`

```json
[
  {
    "target": "0.email",
    "include_subdomains": true,
    "exclude_internal_backlinks": true,
    "mode": "one_per_domain",
    "limit": 100,
    "order_by": ["rank,desc"]
  }
]
```

### 6. `orchid.ai` domain overview

Endpoint: `dataforseo_labs/google/domain_rank_overview/live`

```json
[
  {
    "target": "orchid.ai",
    "location_code": 2840,
    "language_code": "en",
    "ignore_synonyms": true
  }
]
```

### 7. `orchid.ai` ranked keywords

Endpoint: `dataforseo_labs/google/ranked_keywords/live`

```json
[
  {
    "target": "orchid.ai",
    "location_code": 2840,
    "language_code": "en",
    "ignore_synonyms": true,
    "item_types": ["organic", "paid"],
    "limit": 250,
    "order_by": ["keyword_data.keyword_info.search_volume,desc"]
  }
]
```

### 8. `orchid.ai` relevant pages

Endpoint: `dataforseo_labs/google/relevant_pages/live`

```json
[
  {
    "target": "orchid.ai",
    "location_code": 2840,
    "language_code": "en",
    "ignore_synonyms": true,
    "limit": 50,
    "order_by": ["metrics.organic.etv,desc"]
  }
]
```

### 9. `orchid.ai` backlink summary

Endpoint: `backlinks/summary/live`

```json
[
  {
    "target": "orchid.ai",
    "include_subdomains": true,
    "exclude_internal_backlinks": true
  }
]
```

### 10. `orchid.ai` backlink detail

Endpoint: `backlinks/backlinks/live`

```json
[
  {
    "target": "orchid.ai",
    "include_subdomains": true,
    "exclude_internal_backlinks": true,
    "mode": "one_per_domain",
    "limit": 100,
    "order_by": ["rank,desc"]
  }
]
```

### 11. Live SERP: `zero email client`

Endpoint: `serp/google/organic/live/advanced`

```json
[
  {
    "keyword": "zero email client",
    "location_code": 2840,
    "language_code": "en",
    "device": "desktop",
    "os": "windows",
    "depth": 10
  }
]
```

### 12. Live SERP: `orchid personal assistant`

Endpoint: `serp/google/organic/live/advanced`

```json
[
  {
    "keyword": "orchid personal assistant",
    "location_code": 2840,
    "language_code": "en",
    "device": "desktop",
    "os": "windows",
    "depth": 10
  }
]
```

## Retained result extract

The responses support these report figures:

- `0.email`: 76 organic keywords, 2,355.274975 ETV, zero paid keywords;
- `orchid.ai`: 8 organic keywords, 94.810001 ETV, zero paid keywords;
- `0.email`: 1,421 backlinks and 481 referring domains;
- `orchid.ai`: 133 backlinks and 68 referring domains;
- `0.email` detail: 100 of 373 one-per-domain rows;
- `orchid.ai` detail: 63 of 66 one-per-domain rows; and
- both requested SERPs returned one result page.

Raw API responses were retained only in the session's transient private
temporary directory, not in the repository. That storage may be cleaned
automatically. This ledger preserves every billed request body, task ID,
status, cost, returned-row count, and the report-level result extract.

## Raw-response retention and limitations

Complete API responses were retained only in the shared temporary workspace
under `/private/tmp/wave3_orchid_*.json`. They were not added to the
repository and may disappear when temporary storage is cleaned. This ledger
preserves every request body, task ID, status, cost, returned limit, and
aggregate used in the dossier.

The raw responses show potential search and link surfaces, not visits or
attribution. The backlink indexes include domain history predating both
products, and the samples include directories, scraped pages, and spam.

## Public-web inspection record

Inspected without interaction:

- `0.email`, about, pricing, privacy, and terms pages;
- `orchid.ai`, blog, case study, privacy, terms, pricing response, sitemap,
  and public headers;
- GitHub repository, contributor, and release metadata;
- Hacker News item metadata;
- Product Hunt, YC, HN, and Reddit public pages; and
- public search-result extracts.

The in-app browser reported no available browser, so rendered DOM, dynamic
consent behavior, and interactive CTA state were not verified. Server HTML
and public search extraction were used instead.

Deliberately not performed:

- repository clone or source checkout;
- any app, package, binary, installer, or release-asset request;
- Zero or Orchid login;
- Google or mailbox authorization;
- SMS initiation;
- Enterprise Typeform;
- trial, checkout, payment, or account creation; and
- client-side execution or local inspection.
