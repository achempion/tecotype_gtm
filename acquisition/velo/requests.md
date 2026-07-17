# Request and cost ledger

Requests were made on **2026-07-17**.

DataForSEO search requests used Google, United States (`2840`), English, and desktop/Windows where a device was required. Credential setup and reusable endpoint guidance belongs in the central [DataForSEO documentation](../../tools/dataforseo.md).

No credential was written to a repository file, request body, command output, or this report. The authorization credential was resolved from the configured system credential store and supplied only as:

```text
Authorization: Basic [REDACTED]
```

The request bodies below are otherwise exact and complete. No body field contained a secret, so no body field is redacted.

## Cost summary

| # | Request | Task ID | Task status | Returned | Cost (USD) |
| ---: | --- | --- | --- | ---: | ---: |
| 1 | Domain overview | `07171734-2101-0388-0000-18907c9ef1a7` | `20000` | 1 domain | 0.012120 |
| 2 | Ranked keywords | `07171734-2101-0381-0000-01a40cc26a84` | `20000` | 2 rows | 0.012240 |
| 3 | Relevant pages | `07171734-2101-0385-0000-49c768457e9d` | `20000` | 1 row | 0.012120 |
| 4 | Domain backlink summary | `07171734-2101-0265-0000-80d586d64379` | `20000` | 1 summary | 0.024036 |
| 5 | Domain backlinks, one/domain | `07171734-2101-0269-0000-4d69b87aa34c` | `20000` | 8 rows | 0.024288 |
| 6 | Exact-domain content search | `07171734-2101-0463-0000-22f093486e8a` | `20000` | 0 rows | 0.024036 |
| 7 | Brand live SERP | `07171734-2101-0139-0000-97ef0dff6c30` | `20000` | 1 result page | 0.002000 |
| 8 | Open-source category live SERP | `07171735-2101-0139-0000-717ff806f21a` | `20000` | 1 result page | 0.002000 |
| 9 | Keyboard category live SERP | `07171735-2101-0139-0000-ea8ef4390157` | `20000` | 1 result page | 0.002000 |
| 10 | Ads advertiser lookup | `07171735-2101-0139-0000-7e67798ba958` | `40102` No Search Results | 0 results | 0.002000 |
| 11 | Ads creative lookup | `07171735-2101-0139-0000-99d2f4145001` | `40102` No Search Results | 0 results | 0.002000 |
| 12 | Repository-URL backlink summary | `07171737-2101-0265-0000-5c1d213e44b7` | `20000` | 1 summary | 0.024036 |
| 13 | Repository-URL backlinks, one/domain | `07171737-2101-0269-0000-8387d21b2468` | `20000` | 11 rows | 0.024396 |
|  | **Total** | **13 billed tasks** |  |  | **0.167272** |

The exact total is below the **$0.25** cap by **$0.082728**.

There were:

- **0 duplicate paid calls**;
- **0 malformed paid calls**;
- **2 billed no-result task statuses**, both recorded above;
- **0 tasks omitted from this ledger**.

The two `40102` task statuses occurred inside billed task envelopes. They mean no result was returned for the requested coverage; they do not establish that Velo never advertised.

The exact-domain content search returned zero rows even though known Reddit, Hacker News, LinkedIn, YouTube, and publication pages exist. This is a direct coverage limitation.

## Exact request bodies

### 1. Domain overview

Endpoint:

`/v3/dataforseo_labs/google/domain_rank_overview/live`

```json
[{"target":"velomail.app","location_code":2840,"language_code":"en","ignore_synonyms":true}]
```

### 2. Ranked keywords

Endpoint:

`/v3/dataforseo_labs/google/ranked_keywords/live`

```json
[{"target":"velomail.app","location_code":2840,"language_code":"en","ignore_synonyms":true,"item_types":["organic","paid"],"limit":250,"order_by":["keyword_data.keyword_info.search_volume,desc"]}]
```

### 3. Relevant pages

Endpoint:

`/v3/dataforseo_labs/google/relevant_pages/live`

```json
[{"target":"velomail.app","location_code":2840,"language_code":"en","ignore_synonyms":true,"limit":50,"order_by":["metrics.organic.etv,desc"]}]
```

### 4. Domain backlink summary

Endpoint:

`/v3/backlinks/summary/live`

```json
[{"target":"velomail.app","include_subdomains":true,"exclude_internal_backlinks":true}]
```

### 5. Domain backlinks, one/domain

Endpoint:

`/v3/backlinks/backlinks/live`

```json
[{"target":"velomail.app","include_subdomains":true,"exclude_internal_backlinks":true,"mode":"one_per_domain","limit":200,"order_by":["rank,desc"]}]
```

### 6. Exact-domain content search

Endpoint:

`/v3/content_analysis/search/live`

```json
[{"keyword":"velomail.app","search_mode":"as_is","limit":100}]
```

### 7. Brand live SERP

Endpoint:

`/v3/serp/google/organic/live/advanced`

```json
[{"keyword":"velo mail email client","location_code":2840,"language_code":"en","device":"desktop","os":"windows","depth":10}]
```

### 8. Open-source category live SERP

Endpoint:

`/v3/serp/google/organic/live/advanced`

```json
[{"keyword":"open source desktop email client","location_code":2840,"language_code":"en","device":"desktop","os":"windows","depth":10}]
```

### 9. Keyboard category live SERP

Endpoint:

`/v3/serp/google/organic/live/advanced`

```json
[{"keyword":"keyboard first email client","location_code":2840,"language_code":"en","device":"desktop","os":"windows","depth":10}]
```

### 10. Ads advertiser lookup

Endpoint:

`/v3/serp/google/ads_advertisers/live/advanced`

```json
[{"keyword":"velo mail","location_code":2840}]
```

### 11. Ads creative lookup

Endpoint:

`/v3/serp/google/ads_search/live/advanced`

```json
[{"target":"velomail.app","location_code":2840,"platform":"all","format":"all","date_from":"2018-05-31","date_to":"2026-07-17","depth":40}]
```

### 12. Repository-URL backlink summary

Endpoint:

`/v3/backlinks/summary/live`

```json
[{"target":"https://github.com/avihaymenahem/velo","exclude_internal_backlinks":true}]
```

### 13. Repository-URL backlinks, one/domain

Endpoint:

`/v3/backlinks/backlinks/live`

```json
[{"target":"https://github.com/avihaymenahem/velo","exclude_internal_backlinks":true,"mode":"one_per_domain","limit":200,"order_by":["rank,desc"]}]
```

## Public-web and metadata requests

The no-cost evidence pass used only public, non-account surfaces:

- `https://velomail.app/`;
- `https://velomail.app/robots.txt`;
- `https://velomail.app/sitemap.xml`;
- current first-party JavaScript/CSS/image assets referenced by the page;
- public GitHub repository metadata, file tree, languages, contributors, commits, releases, release assets, workflow definitions, and workflow job metadata;
- raw public README, SECURITY, architecture, keyboard, package, Tauri manifest, and workflow files;
- GitHub release and repository pages;
- Wayback CDX and the two available archived homepage captures;
- public Reddit JSON/pages and Hacker News item data;
- public search extracts for LinkedIn, YouTube, publications, packages, and community pages;
- a metadata-only request to the configured updater URL.

The updater request followed the public redirect:

```text
https://github.com/avihaymenahem/velo/releases/latest/download/latest.json
→ https://github.com/avihaymenahem/velo/releases/download/velo-v0.4.21/latest.json
→ HTTP 404
```

No update artifact or Velo application binary was downloaded.

A request for timestamped public stargazer history returned GitHub’s **“Requires authentication”** response. No GitHub account, token, or alternative authenticated path was used. Current star count was retained; historical daily star growth is unknown.

## Research boundaries

### Performed

- rendered the public homepage at a desktop viewport;
- inspected public HTML, metadata, source, manifests, and workflows;
- read public release and community records;
- requested public search/backlink estimates;
- checked response status for the configured update manifest.

### Not performed

- download, install, mount, or launch Velo;
- create a Velo, GitHub, Google, AI-provider, or other account;
- configure Google Cloud credentials;
- start OAuth or connect Gmail/IMAP/SMTP;
- submit a form or send email;
- start a trial;
- purchase or donate;
- inspect private analytics;
- treat source-present behavior as runtime-validated.

## Interpretation limits

- DataForSEO values are third-party snapshots, not analytics.
- Search ranks are date-, market-, and device-specific.
- Backlink indexes omit known public links and include mirrors/spam.
- GitHub counters are dynamic and do not identify unique people.
- Community votes, comments, reactions, views, stars, forks, and asset requests are attention signals.
- Public comments can reveal friction but are not representative research.
- Source and workflows establish implementation/configuration evidence, not end-user success.
