# Canary Mail DataForSEO request ledger

Requests were made on **2026-07-17**.

Search requests used Google, United States (`2840`), English, and desktop/Windows where a device was required. Reusable endpoint and credential guidance belongs in the central [DataForSEO documentation](../../tools/dataforseo.md).

No credential was written to a repository file, command output, or this report. Each POST contained exactly one task object. No malformed or duplicated paid call was identified in the documented pass.

## Cost summary

| # | Request | Endpoint | Returned / task status | Cost (USD) |
| ---: | --- | --- | --- | ---: |
| 1 | Domain overview | `dataforseo_labs/google/domain_rank_overview/live` | 1 result; `20000 Ok` | 0.012120 |
| 2 | Ranked keywords | `dataforseo_labs/google/ranked_keywords/live` | 250 of 3,115 keywords; `20000 Ok` | 0.042000 |
| 3 | Relevant pages | `dataforseo_labs/google/relevant_pages/live` | 50 of 217 pages; `20000 Ok` | 0.018000 |
| 4 | Backlink summary | `backlinks/summary/live` | 1 summary; `20000 Ok` | 0.024036 |
| 5 | Backlinks, one/domain | `backlinks/backlinks/live` | 200 of 1,927 rows; `20000 Ok` | 0.031200 |
| 6 | Exact-domain content search | `content_analysis/search/live` | 100 of 262 items; `20000 Ok` | 0.027600 |
| 7 | Live organic SERP: `canary mail` | `serp/google/organic/live/advanced` | result page; `20000 Ok` | 0.002000 |
| 8 | Live organic SERP: `best email client for mac` | `serp/google/organic/live/advanced` | result page; `20000 Ok` | 0.002000 |
| 9 | Live organic SERP: `private email client` | `serp/google/organic/live/advanced` | result page; `20000 Ok` | 0.002000 |
| 10 | Live organic SERP: `ai email client` | `serp/google/organic/live/advanced` | result page; `20000 Ok` | 0.002000 |
| 11 | Ads advertiser lookup | `serp/google/ads_advertisers/live/advanced` | `40102 No Search Results` | 0.002000 |
| 12 | Ads creative lookup | `serp/google/ads_search/live/advanced` | `40102 No Search Results` | 0.002000 |
|  | **Audited all-in total** | **12 billed tasks** |  | **0.166956** |

The audited all-in **$0.166956** spend is below the confirmed **$2
per-competitor budget**.

A same-day reconciliation of the workspace and `/private/tmp` found no earlier
Canary DataForSEO response artifact or task ID beyond the 12 tasks listed
below, and the research coordinator confirmed that no earlier Canary paid pass
was known. No API request was made for this reconciliation. On the evidence
available, **12 billed tasks and $0.166956 are Canary's complete documented
spend**.

The two advertising requests returned API status `40102` (“No Search Results”) inside successfully billed task envelopes. That means no item was returned for the requested archive coverage. It is not proof that Canary has never advertised.

## Task IDs

| # | DataForSEO task ID |
| ---: | --- |
| 1 | `07171912-2101-0388-0000-1cf25cc1dda4` |
| 2 | `07171913-2101-0381-0000-7f31219e84f1` |
| 3 | `07171913-2101-0385-0000-8c226091f1f5` |
| 4 | `07171913-2101-0265-0000-7ca8379af414` |
| 5 | `07171913-2101-0269-0000-939ab10f7d26` |
| 6 | `07171914-2101-0463-0000-5926f3e46c73` |
| 7 | `07171914-2101-0139-0000-7a0e6b361bf1` |
| 8 | `07171914-2101-0139-0000-2771ed850cc1` |
| 9 | `07171915-2101-0139-0000-536e16117ef9` |
| 10 | `07171915-2101-0139-0000-86ed830fddac` |
| 11 | `07171915-2101-0139-0000-d860b537830b` |
| 12 | `07171916-2101-0139-0000-8665cdaa611f` |

## Exact request bodies

### 1. Domain overview

```json
[
  {
    "target": "canarymail.io",
    "location_code": 2840,
    "language_code": "en",
    "ignore_synonyms": true
  }
]
```

The task completed with one result. A local projection mistakenly selected a non-existent `metrics` path and the raw live response was not retained. The paid task was deliberately not repeated. Consequently, this report does not use domain-overview metrics; the aggregate search figures come from the retained ranked-keywords response.

### 2. Ranked keywords

```json
[
  {
    "target": "canarymail.io",
    "location_code": 2840,
    "language_code": "en",
    "ignore_synonyms": true,
    "item_types": ["organic", "paid"],
    "limit": 250,
    "order_by": ["keyword_data.keyword_info.search_volume,desc"]
  }
]
```

Retained aggregate results:

| Metric | Result |
| --- | ---: |
| Organic keyword count | 3,115 |
| Organic ETV | 22,414.684556 |
| Estimated organic paid-traffic cost | $63,422.020770 |
| Paid keyword count | 0 |
| Paid ETV | 0 |
| Marked new | 1,191 |
| Marked up | 674 |
| Marked down | 1,102 |

Position counts:

| Position group | Count |
| --- | ---: |
| 1 | 19 |
| 2–3 | 131 |
| 4–10 | 634 |
| 11–20 | 747 |
| 21–30 | 592 |
| 31–40 | 435 |
| 41–50 | 275 |
| 51–60 | 133 |
| 61–70 | 73 |
| 71–80 | 41 |
| 81–90 | 26 |
| 91–100 | 9 |

Representative retained rows:

| Keyword | Volume | Rank | ETV | URL |
| --- | ---: | --- | ---: | --- |
| `free email services` | 2,240,000 | group 76 / absolute 86 | 4,704.00 | `/blog/best-free-business-email` |
| `what does bcc mean in email` | 22,200 | group 6 / absolute 10 | 750.36 | `/blog/what-does-bcc-mean-in-email` |
| `create yahoo email` | 12,100 | group 6 | 408.98 | `/blog/create-a-yahoo-mail-account` |
| `ai powered email client` | 1,000 | group 4 / absolute 5 | 65.90 | homepage |
| `best email application for mac` | 1,000 | group 13 / absolute 18 | 5.90 | Mac email-client article |
| `email apps for windows` | 1,000 | group 11 / absolute 16 | 9.10 | homepage |

The call ordered rows by search volume and retained only 250 of 3,115 keywords. The aggregate metrics cover the task result, while the row examples are not a complete keyword export.

### 3. Relevant pages

```json
[
  {
    "target": "canarymail.io",
    "location_code": 2840,
    "language_code": "en",
    "ignore_synonyms": true,
    "limit": 50,
    "order_by": ["metrics.organic.etv,desc"]
  }
]
```

Leading retained pages:

| URL | Organic ETV | Organic keywords |
| --- | ---: | ---: |
| `/blog/best-free-business-email` | 4,835.622961 | 41 |
| `/blog/what-does-bcc-mean-in-email` | 2,717.694 | 131 |
| `/blog/email-cc-meaning` | 1,991.089 | 147 |
| `/blog/create-a-yahoo-mail-account` | 1,710.612 | 158 |
| `/blog/change-outlook-password` | 1,322.100 | 54 |
| `/blog/can-you-unsend-an-email` | 1,131.001 | 47 |
| homepage | 1,090.996003 | 186 |
| `/blog/email-read-receipts` | 695.711 | 30 |
| `/blog/how-to-find-archived-emails-gmail` | 566.664 | 99 |

Calculated against total organic ETV:

- homepage: 4.867%;
- leading page: 21.573%;
- top six listed blog pages: 61.157%;
- top six blog pages plus homepage: 66.024%.

Small rounding differences in displayed rows do not materially affect those shares.

### 4. Backlink summary

```json
[
  {
    "target": "canarymail.io",
    "include_subdomains": true,
    "exclude_internal_backlinks": true
  }
]
```

Retained summary:

| Metric | Result |
| --- | ---: |
| Backlinks | 16,224 |
| Referring pages | 14,703 |
| Referring domains | 2,283 |
| Referring main domains | 1,852 |
| Rank | 292 |
| Spam score | 18 |
| Broken backlinks | 109 |

The backlink total is not treated as a referral count. Large TLD concentrations and the detail sample showed substantial directory, syndication, and low-quality noise.

### 5. Backlink detail

```json
[
  {
    "target": "canarymail.io",
    "include_subdomains": true,
    "exclude_internal_backlinks": true,
    "mode": "one_per_domain",
    "limit": 200,
    "order_by": ["rank,desc"]
  }
]
```

The task returned 200 of 1,927 available one-per-domain rows. Credible examples included Product Hunt, TechRadar, The Sweet Setup, Mailtrap, Comparitech, Heise, and StartupNation. Many other rows were generic software/AI directories, syndicated content, or low-quality sites.

The Product Hunt target included:

`https://canarymail.io/?utm_source=producthunt&utm_medium=referral&utm_campaign=producthunt_launch&ref=producthunt`

This proves that the link was tagged for attribution, not that it generated traffic or conversion.

### 6. Content Analysis

```json
[
  {
    "keyword": "canarymail.io",
    "search_mode": "as_is",
    "limit": 100
  }
]
```

The task returned 100 of 262 items. Results were dominated by Canary’s own pages and multilingual pages, making the task weak for independent-mention discovery. It was useful as corroboration of a broad owned-content system.

### 7. Live organic SERP: `canary mail`

```json
[
  {
    "keyword": "canary mail",
    "location_code": 2840,
    "language_code": "en",
    "device": "desktop",
    "os": "windows",
    "depth": 10
  }
]
```

Observed: Canary homepage organic group rank 1. The sampled result page also included Mac App Store, Google Play, YouTube, iOS App Store, Setapp’s comparison, and Wikipedia surfaces.

### 8. Live organic SERP: `best email client for mac`

```json
[
  {
    "keyword": "best email client for mac",
    "location_code": 2840,
    "language_code": "en",
    "device": "desktop",
    "os": "windows",
    "depth": 10
  }
]
```

Observed: Canary was absent from the sampled top ten organic groups.

### 9. Live organic SERP: `private email client`

```json
[
  {
    "keyword": "private email client",
    "location_code": 2840,
    "language_code": "en",
    "device": "desktop",
    "os": "windows",
    "depth": 10
  }
]
```

Observed: Canary was absent from the sampled top ten. The result set leaned toward private-email providers and discussion, showing query ambiguity as well as weak Canary capture.

### 10. Live organic SERP: `ai email client`

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

Observed: Canary appeared at organic group rank 6 / absolute rank 7. Shortwave and GitHub’s Inbox Zero were among the higher results.

### 11. Google Ads advertiser lookup

```json
[
  {
    "keyword": "canary mail",
    "location_code": 2840
  }
]
```

Task status: `40102 No Search Results`.

### 12. Google Ads creative lookup

```json
[
  {
    "target": "canarymail.io",
    "location_code": 2840,
    "platform": "all",
    "format": "all",
    "date_from": "2018-05-31",
    "date_to": "2026-07-17",
    "depth": 40
  }
]
```

Task status: `40102 No Search Results`.

## Non-DataForSEO inspection record

Only public web and metadata surfaces were used:

- Canary homepage, pricing, downloads index, about, FAQ, privacy, audit summary, release notes, and blog pages;
- public Apple metadata and App Store pages;
- public Google Play page;
- the public Microsoft Store URL as linked by Canary;
- Product Hunt, TechRadar, Times of India, Setapp, public Reddit, and other indexed articles/guides.

The public `/downloads` index was opened only as a webpage. No download button or installer/store install action was followed.

A parallel audit pass successfully rendered the public Canary homepage in the
in-app browser. It verified the visible hero and section hierarchy, repeated
Download links, the Pricing link, the Dove cross-product link, a US-English
state with no visible cookie-choice control, and the presence of Google,
HubSpot, Ahrefs, Webflow, and Canary-hosted script elements in the rendered
DOM. No CTA, link, form, download route, or store route was used. This was a
public-page visual and DOM inspection, not a complete network capture; it does
not establish that every script transmitted data or verify geolocated,
responsive, personalized, conditional, or post-click states.

A separate rendering attempt in this workstream found no local browser runtime.
That failed attempt created no interaction and does not negate the successful
parallel render. Public initial HTML, response headers, public metadata APIs,
and text-accessible pages supplied the rest of the web evidence. JavaScript-only
Microsoft Store detail remains unverified.

No Canary client, installer, extension, package, or binary was downloaded, fetched, mounted, opened, inspected, or executed. No account, mailbox authorization, trial, form, store action, or checkout was started.

## Reproducibility and interpretation rules

- Treat ETV, search volume, paid-traffic value, backlink rank, and spam score as provider models.
- Preserve the market, language, date, device, order, and row limit with every result.
- Do not turn “No Search Results” into “never advertised.”
- Do not equate indexed backlinks with referral sessions.
- Do not infer activation from downloads or store ratings.
- Do not infer current features or pricing from historical reviews.
- Do not repeat the domain-overview call solely to recover a projection mistake; the limitation is documented instead.
- Verify all public-platform and Tecotype release claims again immediately before publication.
