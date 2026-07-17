# MonoMail DataForSEO request ledger

Requests were made on **2026-07-17**.

Search requests used Google, United States (`2840`), English, and
desktop/Windows for SERPs. Reusable endpoint and credential guidance is in
[the central documentation](../../tools/dataforseo.md).

No credential was written to the repository or emitted in command output.
Every billed Live POST contained exactly **one task object**. All seven tasks
returned top-level and task-level status `20000 Ok.` There were no malformed,
failed, or duplicate paid calls in this pass.

## Cost summary

| # | Request | Returned | Cost (USD) |
| ---: | --- | ---: | ---: |
| 1 | Domain overview | 0 items | 0.012000 |
| 2 | Ranked keywords | 0 rows | 0.012000 |
| 3 | Relevant pages | 0 rows | 0.012000 |
| 4 | Backlink summary | 1 summary | 0.024036 |
| 5 | Backlinks, one/domain | all 3 rows | 0.024108 |
| 6 | Live SERP: `monomail android email client` | 1 result page | 0.002000 |
| 7 | Live SERP: `minimal open source android email client` | 1 result page | 0.002000 |
|  | **Audited total** | **7 billed tasks** | **0.088144** |

The audited total is below the confirmed **$2 per-competitor budget**.

## Audit identifiers

| # | Task ID | Status | Cost |
| ---: | --- | --- | ---: |
| 1 | `07172057-2101-0388-0000-dd14bf365ad1` | `20000 Ok.` | 0.012000 |
| 2 | `07172057-2101-0381-0000-4d5d510bc2fc` | `20000 Ok.` | 0.012000 |
| 3 | `07172057-2101-0385-0000-2dcf870e8aa4` | `20000 Ok.` | 0.012000 |
| 4 | `07172057-2101-0265-0000-48693bca3485` | `20000 Ok.` | 0.024036 |
| 5 | `07172057-2101-0269-0000-833b9a5a6d6c` | `20000 Ok.` | 0.024108 |
| 6 | `07172057-2101-0139-0000-894853484b15` | `20000 Ok.` | 0.002000 |
| 7 | `07172057-2101-0139-0000-1be33b8fa407` | `20000 Ok.` | 0.002000 |

## Exact request bodies

### 1. Domain overview

Endpoint: `dataforseo_labs/google/domain_rank_overview/live`

```json
[
  {
    "target": "monomail.millosaurs.me",
    "location_code": 2840,
    "language_code": "en",
    "ignore_synonyms": true
  }
]
```

### 2. Ranked keywords

Endpoint: `dataforseo_labs/google/ranked_keywords/live`

```json
[
  {
    "target": "monomail.millosaurs.me",
    "location_code": 2840,
    "language_code": "en",
    "ignore_synonyms": true,
    "item_types": ["organic", "paid"],
    "limit": 250,
    "order_by": ["keyword_data.keyword_info.search_volume,desc"]
  }
]
```

### 3. Relevant pages

Endpoint: `dataforseo_labs/google/relevant_pages/live`

```json
[
  {
    "target": "monomail.millosaurs.me",
    "location_code": 2840,
    "language_code": "en",
    "ignore_synonyms": true,
    "limit": 50,
    "order_by": ["metrics.organic.etv,desc"]
  }
]
```

### 4. Backlink summary

Endpoint: `backlinks/summary/live`

```json
[
  {
    "target": "monomail.millosaurs.me",
    "include_subdomains": true,
    "exclude_internal_backlinks": true
  }
]
```

### 5. Backlink detail

Endpoint: `backlinks/backlinks/live`

```json
[
  {
    "target": "monomail.millosaurs.me",
    "include_subdomains": true,
    "exclude_internal_backlinks": true,
    "mode": "one_per_domain",
    "limit": 100,
    "order_by": ["rank,desc"]
  }
]
```

### 6. Live SERP: `monomail android email client`

Endpoint: `serp/google/organic/live/advanced`

```json
[
  {
    "keyword": "monomail android email client",
    "location_code": 2840,
    "language_code": "en",
    "device": "desktop",
    "os": "windows",
    "depth": 10
  }
]
```

### 7. Live SERP: `minimal open source android email client`

Endpoint: `serp/google/organic/live/advanced`

```json
[
  {
    "keyword": "minimal open source android email client",
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

- zero domain-overview items;
- zero ranked-keyword rows;
- zero relevant-page rows;
- 4 backlinks from 3 referring domains;
- all 3 one-per-domain backlink rows;
- one brand-and-category SERP; and
- one unbranded category SERP.

Raw API responses were retained only in the session's transient private
temporary directory, not in the repository. That storage may be cleaned
automatically. This ledger preserves every billed request body, task ID,
status, cost, returned-row count, and the report-level result extract.
