# Extra paid-data request ledger

Research date: 2026-07-17. Provider: DataForSEO. Market: Google US (`location_code: 2840`), English where supported.

Every live POST contained exactly one task object. No credentials, authorization headers, or mailbox/client data are recorded here. Raw responses were retained only in `/private/tmp` during analysis and were not committed; they can contain provider metadata, estimated search data, public URLs, and public ad-preview URLs.

## Summary

- Requests: 11
- Successful task responses: 10
- `No Search Results` task responses: 1
- Total cost: **$0.122128**
- Per-competitor budget: **$2.00**
- Remaining budget: **$1.877872**

`limit` and `depth` below are request ceilings, not guarantees of complete market coverage. A successful status means the provider processed the request, not that its index is exhaustive.

## Request 01 — domain rank overview

- Endpoint: `/v3/dataforseo_labs/google/domain_rank_overview/live`
- Body:

```json
[{"target":"extra.email","location_code":2840,"language_code":"en","ignore_synonyms":true}]
```

- Task ID: `07172103-2101-0388-0000-ce773fa6439c`
- Status: `20000` — `Ok.`
- Cost: `$0.012120`
- Response boundary: domain-level ranking estimates; 3 organic keywords, estimated traffic value 53.556, 0 paid keywords.

## Request 02 — ranked keywords

- Endpoint: `/v3/dataforseo_labs/google/ranked_keywords/live`
- Body:

```json
[{"target":"extra.email","location_code":2840,"language_code":"en","ignore_synonyms":true,"item_types":["organic","paid"],"limit":250,"order_by":["keyword_data.keyword_info.search_volume,desc"]}]
```

- Task ID: `07172103-2101-0381-0000-effc86af6800`
- Status: `20000` — `Ok.`
- Cost: `$0.012360`
- Requested limit: 250
- Returned: 3 items.

## Request 03 — relevant pages

- Endpoint: `/v3/dataforseo_labs/google/relevant_pages/live`
- Body:

```json
[{"target":"extra.email","location_code":2840,"language_code":"en","ignore_synonyms":true,"limit":50,"order_by":["metrics.organic.etv,desc"]}]
```

- Task ID: `07172103-2101-0385-0000-45118a85b7bd`
- Status: `20000` — `Ok.`
- Cost: `$0.012120`
- Requested limit: 50
- Returned: 1 page, the homepage.

## Request 04 — backlink summary

- Endpoint: `/v3/backlinks/summary/live`
- Body:

```json
[{"target":"extra.email","include_subdomains":true,"exclude_internal_backlinks":true}]
```

- Task ID: `07172104-2101-0265-0000-90aa5469d943`
- Status: `20000` — `Ok.`
- Cost: `$0.024036`
- Response boundary: indexed backlink summary, including legacy-domain and low-quality noise.

## Request 05 — backlink detail

- Endpoint: `/v3/backlinks/backlinks/live`
- Body:

```json
[{"target":"extra.email","include_subdomains":true,"exclude_internal_backlinks":true,"mode":"one_per_domain","limit":200,"order_by":["rank,desc"]}]
```

- Task ID: `07172104-2101-0269-0000-9fe5247d29a7`
- Status: `20000` — `Ok.`
- Cost: `$0.027384`
- Requested limit: 200
- Returned: 94 items from 101 candidates under the selected one-per-domain mode.

## Request 06 — content analysis

- Endpoint: `/v3/content_analysis/search/live`
- Body:

```json
[{"keyword":"extra.email","search_mode":"as_is","limit":100}]
```

- Task ID: `07172104-2101-0463-0000-7a8c00554a83`
- Status: `20000` — `Ok.`
- Cost: `$0.024108`
- Requested limit: 100
- Returned: 3 items. Coverage missed known major articles and is not suitable for complete share-of-voice analysis.

## Request 07 — branded live SERP

- Endpoint: `/v3/serp/google/organic/live/advanced`
- Body:

```json
[{"keyword":"extra email app","location_code":2840,"language_code":"en","device":"desktop","os":"windows","depth":10}]
```

- Task ID: `07172104-2101-0139-0000-c3c730e14f11`
- Status: `20000` — `Ok.`
- Cost: `$0.002000`
- Requested depth: 10.

## Request 08 — life-inbox live SERP

- Endpoint: `/v3/serp/google/organic/live/advanced`
- Body:

```json
[{"keyword":"life inbox email app","location_code":2840,"language_code":"en","device":"desktop","os":"windows","depth":10}]
```

- Task ID: `07172104-2101-0139-0000-b9b570747cd5`
- Status: `20000` — `Ok.`
- Cost: `$0.002000`
- Requested depth: 10; Extra was absent from the observed top ten.

## Request 09 — category live SERP

- Endpoint: `/v3/serp/google/organic/live/advanced`
- Body:

```json
[{"keyword":"personal email assistant app","location_code":2840,"language_code":"en","device":"desktop","os":"windows","depth":10}]
```

- Task ID: `07172104-2101-0139-0000-ffa92da4d4ee`
- Status: `20000` — `Ok.`
- Cost: `$0.002000`
- Requested depth: 10; Extra was absent from the observed top ten.

## Request 10 — advertiser lookup

- Endpoint: `/v3/serp/google/ads_advertisers/live/advanced`
- Body:

```json
[{"keyword":"extra email","location_code":2840}]
```

- Task ID: `07172104-2101-0139-0000-9daafe7da23b`
- Status: `40102` — `No Search Results.`
- Cost: `$0.002000`
- Response boundary: no result for this keyword-and-market lookup; not proof that Extra never advertised.

## Request 11 — ad archive search

- Endpoint: `/v3/serp/google/ads_search/live/advanced`
- Body:

```json
[{"target":"extra.email","location_code":2840,"platform":"all","format":"all","date_from":"2018-05-31","date_to":"2026-07-17","depth":40}]
```

- Task ID: `07172104-2101-0139-0000-259a2f4872d4`
- Status: `20000` — `Ok.`
- Cost: `$0.002000`
- Requested depth: 40
- Returned: 2 creatives—one text and one image—from verified advertiser
  Samuel Hsiung. One public preview was inspected; the other creative's copy
  was not verified.

## Interpretation limits

DataForSEO provides indexed estimates and archive observations, not Extra's analytics. Keyword estimates, backlinks, result positions, and ad creatives cannot establish impressions, clicks, spend, incremental lift, activation, retention, or payment. No client artifact or authenticated funnel was needed or used.
