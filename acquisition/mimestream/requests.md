# DataForSEO request ledger

Requests were made on **2026-07-17**.

Search requests used Google, United States (`2840`), English, and desktop/Windows where a device was required. Reusable endpoint and credential guidance belongs in the central [DataForSEO documentation](../../tools/dataforseo.md).

No credential was written to a repository file, command output, or this report. The credential was read from the configured system credential store. Request bodies below are complete; they contain no secret and therefore require no field-level redaction.

## Cost summary

| Request | Endpoint | Returned | Cost (USD) |
| --- | --- | ---: | ---: |
| Domain overview | `dataforseo_labs/google/domain_rank_overview/live` | 1 domain | 0.012120 |
| Ranked keywords | `dataforseo_labs/google/ranked_keywords/live` | 217 rows | 0.038040 |
| Relevant pages | `dataforseo_labs/google/relevant_pages/live` | 18 rows | 0.014160 |
| Backlink summary | `backlinks/summary/live` | 1 summary | 0.024036 |
| Backlinks, one/domain | `backlinks/backlinks/live` | 200 of 963 available rows | 0.031200 |
| Exact-domain content search | `content_analysis/search/live` | 17 rows | 0.024612 |
| Four live organic SERPs | `serp/google/organic/live/advanced` | 4 result pages | 0.008000 |
| Ads advertiser lookup | `serp/google/ads_advertisers/live/advanced` | no search results | 0.002000 |
| Ads creative lookup | `serp/google/ads_search/live/advanced` | no search results | 0.002000 |
| **Total** | 12 billed tasks |  | **0.156168** |

The total is below the **$0.25** research cap. There were no duplicate or malformed paid calls.

The two advertising tasks returned API status `40102` (“No Search Results”) inside successfully billed task envelopes. That is recorded as no result for the requested coverage, not as proof that Mimestream never advertised.

## Exact request bodies

### Domain overview

```json
[
  {
    "target": "mimestream.com",
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
    "target": "mimestream.com",
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
    "target": "mimestream.com",
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
    "target": "mimestream.com",
    "include_subdomains": true,
    "exclude_internal_backlinks": true
  }
]
```

### Backlink detail

```json
[
  {
    "target": "mimestream.com",
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
    "keyword": "mimestream.com",
    "search_mode": "as_is",
    "limit": 100
  }
]
```

### Live organic SERP: `mimestream`

```json
[
  {
    "keyword": "mimestream",
    "location_code": 2840,
    "language_code": "en",
    "device": "desktop",
    "os": "windows",
    "depth": 10
  }
]
```

### Live organic SERP: `gmail app for mac`

```json
[
  {
    "keyword": "gmail app for mac",
    "location_code": 2840,
    "language_code": "en",
    "device": "desktop",
    "os": "windows",
    "depth": 10
  }
]
```

### Live organic SERP: `best gmail client for mac`

```json
[
  {
    "keyword": "best gmail client for mac",
    "location_code": 2840,
    "language_code": "en",
    "device": "desktop",
    "os": "windows",
    "depth": 10
  }
]
```

### Live organic SERP: `gmail client macos`

```json
[
  {
    "keyword": "gmail client macos",
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
    "keyword": "mimestream",
    "location_code": 2840
  }
]
```

### Google Ads creative lookup

```json
[
  {
    "target": "mimestream.com",
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

| Request | Task ID | Task cost |
| --- | --- | ---: |
| Domain overview | `07171653-2101-0388-0000-1ac524e418c2` | 0.012120 |
| Ranked keywords | `07171653-2101-0381-0000-8cf0aa54d739` | 0.038040 |
| Relevant pages | `07171653-2101-0385-0000-316d75524879` | 0.014160 |
| Backlink summary | `07171653-2101-0265-0000-aeb53e23010f` | 0.024036 |
| Backlink detail | `07171653-2101-0269-0000-d67d64c01061` | 0.031200 |
| Content Analysis | `07171653-2101-0463-0000-9f5900b06132` | 0.024612 |
| SERP: `mimestream` | `07171654-2101-0139-0000-e7710bd6758f` | 0.002000 |
| SERP: `gmail app for mac` | `07171654-2101-0139-0000-6d28364e17e5` | 0.002000 |
| SERP: `best gmail client for mac` | `07171655-2101-0139-0000-9deb7bef6e72` | 0.002000 |
| SERP: `gmail client macos` | `07171655-2101-0139-0000-b27c614f8ef8` | 0.002000 |
| Ads advertisers | `07171655-2101-0139-0000-ed634b9b4d82` | 0.002000 |
| Ads creatives | `07171655-2101-0139-0000-41137f9c4c23` | 0.002000 |

## Output and extraction record

Raw response envelopes were used from temporary local files and were **not retained in the repository**. The report retains:

- exact request body;
- endpoint;
- task ID;
- returned-row limit;
- task-reported cost;
- extracted aggregate used in the analysis.

This is sufficient to identify the provider tasks but not to independently re-extract every row from repository artifacts. A future repeat should retain redacted raw envelopes in a dedicated evidence location if repository policy permits.

Notable extraction boundaries:

- Ranked-keyword request returned all 217 reported rows because its limit was 250.
- Relevant-pages request returned all 18 reported rows because its limit was 50.
- Backlink detail returned the first 200 of 963 available one-per-domain rows, ordered by provider rank.
- Content Analysis returned all 17 reported rows, but its coverage missed known press and community pages.
- Backlink summary is an aggregate index snapshot, not verified referral traffic.

## Public-web and funnel inspection record

The in-app browser runtime had no available browser session during this research. After the documented availability check failed, the public funnel was inspected through:

- current public page responses and scripts;
- public search results;
- unauthenticated account-page GET requests;
- Wayback captures;
- direct installer metadata and read-only static bundle inspection.

That installer inspection happened before the user clarified a
no-client-download boundary. The disk image was never launched or installed,
was removed from temporary storage on 2026-07-17, and was not downloaded
again.

The following actions were deliberately not performed:

- newsletter submission;
- account creation;
- Cloudflare Turnstile completion;
- Google authorization;
- live app launch;
- email verification;
- checkout or purchase.

This limits the funnel report to public and static evidence. It does not validate interactive onboarding, sync, activation, or payment completion.

## Reliability rules

- Search volume, ETV, difficulty, and rank are provider estimates.
- The Labs rank for `gmail app for mac` was 9 while the same-day live top-10 capture did not contain Mimestream; both observations are preserved as method/timing variance.
- A current ranking cannot reconstruct beta-era acquisition.
- Literal-brand ETV classification is directional and misses spelling variants.
- A backlink is not a referral visit.
- A press link or community vote is not activation.
- Link indexes contain piracy and spam and have incomplete coverage.
- No captured ad is not evidence of no historical advertising.
- Archived pages show offer and message changes, not why they changed or how they performed.
- Public first-party counts have no source, active-use, or retention definition.
- No internal source analytics, activation, retention, payment, cost, or revenue data was available.
