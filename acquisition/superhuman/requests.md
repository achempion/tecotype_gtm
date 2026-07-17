# Superhuman Mail DataForSEO request ledger

Requests were made on **2026-07-17**.

Search requests used Google, United States (`2840`), English, and
desktop/Windows where a device was required. Reusable endpoint and credential
guidance belongs in the central
[DataForSEO documentation](../../tools/dataforseo.md).

No credential was written to a repository file or this report. The configured
credential was read from the system credential store and used only in the
authorization header. Every Live POST contained exactly **one task object**.

## Final-pass cost summary

| Request | Endpoint | Returned | Cost (USD) |
| --- | --- | ---: | ---: |
| Domain overview, initial | `dataforseo_labs/google/domain_rank_overview/live` | 1 domain | 0.012120 |
| Domain overview, extraction recovery | `dataforseo_labs/google/domain_rank_overview/live` | 1 domain | 0.012120 |
| Ranked keywords | `dataforseo_labs/google/ranked_keywords/live` | 250 of 8,470 rows | 0.042000 |
| Relevant pages | `dataforseo_labs/google/relevant_pages/live` | 50 of 996 rows | 0.018000 |
| Backlink summary | `backlinks/summary/live` | 1 summary | 0.024036 |
| Backlinks, one/domain | `backlinks/backlinks/live` | 200 of 8,028 rows | 0.031200 |
| Content Analysis | `content_analysis/search/live` | 100 of 18,994 possible rows | 0.027600 |
| Four live organic SERPs | `serp/google/organic/live/advanced` | 4 result pages | 0.008000 |
| Ads advertiser lookup | `serp/google/ads_advertisers/live/advanced` | no search results | 0.002000 |
| Ads creative lookup | `serp/google/ads_search/live/advanced` | 40 creatives | 0.002000 |
| **Final-pass total** | **13 billed tasks** |  | **0.179076** |

The final-pass total is disclosed separately from the earlier same-day tasks
below.

The domain overview was called twice in the final pass with the same valid
body. The first
response was successfully billed, but the local extraction projection selected
the wrong field and returned `null` for the metrics. A second call recovered
the metrics. This intentional duplicate is retained in the ledger rather than
hidden.

The Ads Advertisers task returned API status `40102` (“No Search Results”)
inside a billed task envelope. The creative search separately returned 40
results for verified advertiser Superhuman Platform Inc. These results are not
contradictory: the first endpoint searched advertisers by the phrase
`superhuman mail`, while the second searched the transparency archive by
domain.

## Earlier same-day responses found during cross-audit

Twelve earlier Superhuman DataForSEO response files were present in the shared
temporary workspace. They predate the documented final pass. Most repeat the
same domain, keyword, page, backlink, mention, and advertising questions; three
use different live SERP queries, and one unsuccessful advertising query
targeted the Mail page rather than the root domain.

They are disclosed because they were charged against the same client research
on the same date:

| Request | Task ID | Task status | Returned | Cost |
| --- | --- | --- | ---: | ---: |
| Domain overview | `07171854-2101-0388-0000-124a631b4866` | `20000 Ok.` | 1 domain | 0.012120 |
| Ranked keywords | `07171854-2101-0381-0000-7fdfd4763b8f` | `20000 Ok.` | 250 of 8,470 rows | 0.042000 |
| Relevant pages | `07171854-2101-0385-0000-a93d589eddb7` | `20000 Ok.` | 50 of 996 rows | 0.018000 |
| Backlink summary | `07171854-2101-0265-0000-942e3b8fe343` | `20000 Ok.` | 1 summary | 0.024036 |
| Backlinks, one/domain | `07171854-2101-0269-0000-36a925d65f0a` | `20000 Ok.` | 200 of 8,028 rows | 0.031200 |
| Content Analysis, `superhuman mail` | `07171854-2101-0463-0000-d4f6087ea64f` | `20000 Ok.` | 100 of 18,994 rows | 0.027600 |
| SERP, `superhuman email` | `07171856-2101-0139-0000-ef0a244b53e6` | `20000 Ok.` | Successful | 0.002000 |
| SERP, `best email app for productivity` | `07171856-2101-0139-0000-68afe304d69f` | `20000 Ok.` | Successful | 0.002000 |
| SERP, `email app for sales teams` | `07171856-2101-0139-0000-39b85885121c` | `20000 Ok.` | Successful | 0.002000 |
| Ads advertiser lookup, `superhuman mail` | `07171854-2101-0139-0000-f27322be75ec` | `40102 No Search Results.` | 0 rows | 0.002000 |
| Ads creative lookup, Mail-page target | `07171854-2101-0139-0000-149f59d994de` | `40102 No Search Results.` | 0 rows | 0.002000 |
| Ads creative lookup, root domain | `07171856-2101-0139-0000-2b9c53460618` | `20000 Ok.` | 40 creatives | 0.002000 |
| **Earlier-response total** | | | **12 billed tasks** | **0.166956** |

The earlier Labs, backlink, and content bodies match the corresponding final
bodies except that the earlier Relevant Pages body did not include
`order_by`, and its Content Analysis keyword was lowercase
`superhuman mail`. The earlier advertiser lookup included desktop/Windows.
The earlier root-domain creative lookup included desktop/Windows and otherwise
used the same domain, date, platform, format, and depth. The unsuccessful
Mail-page creative lookup used target `superhuman.com/products/mail` with the
same archive parameters. Each earlier POST also contained one task object.

The audited all-in arithmetic is:

```text
Documented final pass   $0.179076   13 tasks
Earlier same-day pass   $0.166956   12 tasks
Audited all-in total    $0.346032   25 tasks
```

No new paid request was made during the cross-audit. The final narrative relies
on the later pass and keeps the full **$0.346032** spend visible rather than
silently excluding earlier tasks. The audited all-in spend is below the
confirmed **$2 per-competitor budget**.

## Exact request bodies

### Domain overview, initial and recovery calls

Endpoint:
`dataforseo_labs/google/domain_rank_overview/live`

Each of the two calls used this one-object task array:

```json
[
  {
    "target": "superhuman.com",
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
    "target": "superhuman.com",
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

Endpoint: `dataforseo_labs/google/relevant_pages/live`

```json
[
  {
    "target": "superhuman.com",
    "location_code": 2840,
    "language_code": "en",
    "ignore_synonyms": true,
    "limit": 50,
    "order_by": ["metrics.organic.etv,desc"]
  }
]
```

### Backlink summary

Endpoint: `backlinks/summary/live`

```json
[
  {
    "target": "superhuman.com",
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
    "target": "superhuman.com",
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
    "keyword": "Superhuman Mail",
    "search_mode": "as_is",
    "limit": 100
  }
]
```

### Live organic SERP: `superhuman mail`

Endpoint: `serp/google/organic/live/advanced`

```json
[
  {
    "keyword": "superhuman mail",
    "location_code": 2840,
    "language_code": "en",
    "device": "desktop",
    "os": "windows",
    "depth": 10
  }
]
```

### Live organic SERP: `ai email client`

Endpoint: `serp/google/organic/live/advanced`

```json
[
  {
    "keyword": "ai email client",
    "location_code": 2840,
    "language_code": "en",
    "device": "desktop",
    "os": "windows",
    "depth": 10
  }
]
```

### Live organic SERP: `fastest email client`

Endpoint: `serp/google/organic/live/advanced`

```json
[
  {
    "keyword": "fastest email client",
    "location_code": 2840,
    "language_code": "en",
    "device": "desktop",
    "os": "windows",
    "depth": 10
  }
]
```

### Live organic SERP: `keyboard email client`

Endpoint: `serp/google/organic/live/advanced`

```json
[
  {
    "keyword": "keyboard email client",
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
    "keyword": "superhuman mail",
    "location_code": 2840
  }
]
```

### Google Ads creative lookup

Endpoint: `serp/google/ads_search/live/advanced`

```json
[
  {
    "target": "superhuman.com",
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

| Request | Task ID | Task status | Task cost |
| --- | --- | --- | ---: |
| Domain overview, initial | `07171913-2101-0388-0000-0fdcfd9bfa07` | `20000 Ok.` | 0.012120 |
| Domain overview, recovery | `07171913-2101-0388-0000-d49ea1e1fd5e` | `20000 Ok.` | 0.012120 |
| Ranked keywords | `07171914-2101-0381-0000-431c9a31e289` | `20000 Ok.` | 0.042000 |
| Relevant pages | `07171914-2101-0385-0000-f16ee83bda10` | `20000 Ok.` | 0.018000 |
| Backlink summary | `07171914-2101-0265-0000-280dea167e91` | `20000 Ok.` | 0.024036 |
| Backlink detail | `07171915-2101-0269-0000-2c105ae88ab3` | `20000 Ok.` | 0.031200 |
| Content Analysis | `07171915-2101-0463-0000-e41125d08d9f` | `20000 Ok.` | 0.027600 |
| SERP: `superhuman mail` | `07171915-2101-0139-0000-68fdf53de7fe` | `20000 Ok.` | 0.002000 |
| SERP: `ai email client` | `07171915-2101-0139-0000-3036ce2da14c` | `20000 Ok.` | 0.002000 |
| SERP: `fastest email client` | `07171918-2101-0139-0000-e389d0f7ba67` | `20000 Ok.` | 0.002000 |
| SERP: `keyboard email client` | `07171919-2101-0139-0000-df66e9f02661` | `20000 Ok.` | 0.002000 |
| Ads advertisers | `07171919-2101-0139-0000-7a9601d342d1` | `40102 No Search Results.` | 0.002000 |
| Ads creatives | `07171919-2101-0139-0000-c3c083953e08` | `20000 Ok.` | 0.002000 |

## Extracted results used

- Domain overview: 8,467 organic keywords, 56,158.66378023662
  organic ETV, $219,295.6663571592 modeled traffic value; three paid
  keywords, 7.274999916553497 paid ETV, $135.65421003103256 modeled
  paid traffic value.
- Ranked keywords: 8,470 total available; 250 returned; sample ETV
  36,680.90732192993.
- Relevant pages: 996 total available; 50 returned. Homepage ETV
  19,103.771966; Mail landing ETV 833.0767 across 33 keywords.
- Backlink summary: 175,717 backlinks and 8,909 referring domains.
- Backlink detail: 8,028 available one-per-domain rows; 200 returned.
- Content Analysis: 18,994 possible items; 100 returned.
- Ads creatives: 40 returned, comprising 36 video and four text archive
  results for verified advertiser Superhuman Platform Inc.

Provider decimals are retained here for auditability. Narrative files round
them for readability.

## Output and extraction record

Raw response envelopes were inspected in command output and were **not
retained in the repository**. The report retains:

- the exact request body;
- endpoint;
- task ID, status, and cost;
- returned-row limit or result count; and
- extracted aggregates used in the analysis.

Important limits:

- DataForSEO traffic is modeled, not first-party analytics.
- The current domain is suite-wide, so search, backlink, mention, and
  advertising totals cannot be assigned to Mail without page-level evidence.
- Ranked-keyword and relevant-page requests returned only the requested top
  samples.
- Backlinks are index observations, not referral clicks.
- Content Analysis includes noisy and duplicated material.
- Ads archive results do not expose spend or conversion and are not necessarily
  Mail creatives.
- One-time SERPs can change and do not represent every geography or device.

## Public-web and funnel inspection record

The first-pass agent runtime had no available browser session. A later
independent root audit rendered the live US-English Mail page and verified its
visible headline, section sequence, repeated `Get Started` controls, Pricing
route, footer Download route, and script hosts. Public inspection also used:

- current public HTML and metadata;
- linked public page scripts;
- public search extracts;
- unauthenticated page GET responses; and
- first-party and independent public articles.

No Superhuman client, browser extension, app package, or installer was
downloaded, opened, installed, mounted, executed, or statically inspected.

The following actions were deliberately not performed:

- entering a signup field;
- choosing Google or Microsoft OAuth;
- authorizing a mailbox;
- creating an account;
- submitting a startup, partner, newsletter, or referral form;
- starting a trial;
- opening checkout;
- entering payment details;
- obtaining a desktop, mobile, or browser client; or
- testing activation, sending, retention, cancellation, or renewal.

Consequently, responsive and animated variants, consent or regional variants,
actual provider eligibility, downloaded client behavior, first sync,
onboarding completion, activation, payment, and retention remain unobserved.
