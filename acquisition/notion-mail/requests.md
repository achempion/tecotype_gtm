# Notion Mail paid-data request ledger

Research date: 2026-07-17. Provider: DataForSEO. Market: Google US (`location_code: 2840`), English where supported.

Every live POST contained exactly one task object. No credentials, authorization headers, account data, mailbox data, client artifacts, or exports are recorded here. Raw responses were retained only in `/private/tmp` during analysis and were not committed; they can contain provider metadata, estimated search data, public URLs, and indexed page text.

## Summary

- Requests: 11
- Successful task responses: 9
- `No Search Results` task responses: 2
- Total cost: **$0.108836**
- Per-competitor budget: **$2.00**
- Remaining budget: **$1.891164**

`limit` and `depth` are request ceilings, not guarantees of exhaustive coverage. A successful status means the provider processed the request, not that its index is complete.

## Request 01 — exact-path ranked keywords

- Endpoint: `/v3/dataforseo_labs/google/ranked_keywords/live`
- Body:

```json
[{"target":"notion.com/product/mail","location_code":2840,"language_code":"en","ignore_synonyms":true,"item_types":["organic","paid"],"limit":250,"order_by":["keyword_data.keyword_info.search_volume,desc"]}]
```

- Task ID: `07172105-2101-0381-0000-b250d6d3eab3`
- Status: `20000` — `Ok.`
- Cost: `$0.012000`
- Requested limit: 250
- Returned: 0 items and null metrics. A separate live SERP ranked the page first for `notion mail`, so this is treated as an exact-target/index limitation.

## Request 02 — exact-URL backlink summary

- Endpoint: `/v3/backlinks/summary/live`
- Body:

```json
[{"target":"https://www.notion.com/product/mail","exclude_internal_backlinks":true}]
```

- Task ID: `07172105-2101-0265-0000-9947e97e4f34`
- Status: `20000` — `Ok.`
- Cost: `$0.024036`
- Response boundary: indexed backlink summary, not traffic or unique visitors.

## Request 03 — exact-URL backlink detail

- Endpoint: `/v3/backlinks/backlinks/live`
- Body:

```json
[{"target":"https://www.notion.com/product/mail","exclude_internal_backlinks":true,"mode":"one_per_domain","limit":200,"order_by":["rank,desc"]}]
```

- Task ID: `07172105-2101-0269-0000-4624514886ea`
- Status: `20000` — `Ok.`
- Cost: `$0.031200`
- Requested limit: 200
- Returned: 200 items from 618 candidates under the selected one-per-domain mode.

## Request 04 — phrase content analysis

- Endpoint: `/v3/content_analysis/search/live`
- Body:

```json
[{"keyword":"Notion Mail","search_mode":"as_is","limit":100}]
```

- Task ID: `07172105-2101-0463-0000-8c0bbe527747`
- Status: `20000` — `Ok.`
- Cost: `$0.027600`
- Requested limit: 100
- Returned: 100 rows; provider total count 582,942. Broad phrase matching produced substantial noise, so that total is not treated as article or mention count.

## Request 05 — branded live SERP

- Endpoint: `/v3/serp/google/organic/live/advanced`
- Body:

```json
[{"keyword":"notion mail","location_code":2840,"language_code":"en","device":"desktop","os":"windows","depth":10}]
```

- Task ID: `07172105-2101-0139-0000-89914dfb82be`
- Status: `20000` — `Ok.`
- Cost: `$0.002000`
- Requested depth: 10.

## Request 06 — shutdown live SERP

- Endpoint: `/v3/serp/google/organic/live/advanced`
- Body:

```json
[{"keyword":"notion mail shutdown","location_code":2840,"language_code":"en","device":"desktop","os":"windows","depth":10}]
```

- Task ID: `07172105-2101-0139-0000-1b6a3a9400b1`
- Status: `20000` — `Ok.`
- Cost: `$0.002000`
- Requested depth: 10.

## Request 07 — alternative live SERP

- Endpoint: `/v3/serp/google/organic/live/advanced`
- Body:

```json
[{"keyword":"notion mail alternative","location_code":2840,"language_code":"en","device":"desktop","os":"windows","depth":10}]
```

- Task ID: `07172106-2101-0139-0000-107c297c8a5c`
- Status: `20000` — `Ok.`
- Cost: `$0.002000`
- Requested depth: 10.

## Request 08 — migration live SERP

- Endpoint: `/v3/serp/google/organic/live/advanced`
- Body:

```json
[{"keyword":"notion mail migration","location_code":2840,"language_code":"en","device":"desktop","os":"windows","depth":10}]
```

- Task ID: `07172106-2101-0139-0000-8f2e51cecf6c`
- Status: `20000` — `Ok.`
- Cost: `$0.002000`
- Requested depth: 10.

## Request 09 — category live SERP

- Endpoint: `/v3/serp/google/organic/live/advanced`
- Body:

```json
[{"keyword":"AI email client for Gmail","location_code":2840,"language_code":"en","device":"desktop","os":"windows","depth":10}]
```

- Task ID: `07172106-2101-0139-0000-db221bd9421b`
- Status: `20000` — `Ok.`
- Cost: `$0.002000`
- Requested depth: 10; Notion Mail was absent from the observed top ten.

## Request 10 — advertiser lookup

- Endpoint: `/v3/serp/google/ads_advertisers/live/advanced`
- Body:

```json
[{"keyword":"notion mail","location_code":2840}]
```

- Task ID: `07172106-2101-0139-0000-7ee40d97bfad`
- Status: `40102` — `No Search Results.`
- Cost: `$0.002000`
- Response boundary: no result for this keyword-and-market lookup; not proof that Notion never advertised Mail.

## Request 11 — ad archive search

- Endpoint: `/v3/serp/google/ads_search/live/advanced`
- Body:

```json
[{"target":"notion.com/product/mail","location_code":2840,"platform":"all","format":"all","date_from":"2018-05-31","date_to":"2026-07-17","depth":40}]
```

- Task ID: `07172106-2101-0139-0000-b34e27aaed36`
- Status: `40102` — `No Search Results.`
- Cost: `$0.002000`
- Requested depth: 40
- Response boundary: no indexed creative for this exact target query; not proof of no advertising across other URLs, accounts, formats, platforms, or time-index coverage.

## Interpretation limits

DataForSEO provides indexed estimates and snapshots, not Notion's analytics. Rankings, links, content-index rows, and empty ad-archive results cannot establish impressions, spend, clicks, source-level activation, retention, plan conversion, shutdown causality, or revenue. No authenticated flow or client artifact was needed or used.
