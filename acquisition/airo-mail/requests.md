# Airo Mail request ledger

Research date: **2026-07-17**

DataForSEO used Google United States (`2840`), English, and desktop Windows
where a device was required. Reusable credential and endpoint guidance is in
[the central documentation](../../tools/dataforseo.md).

No credential is stored here. Every successful live POST contained exactly one
task object.

## Cost summary

| Request | Endpoint | Returned | Status | Cost |
| --- | --- | ---: | ---: | ---: |
| Domain overview | `dataforseo_labs/google/domain_rank_overview/live` | 1 domain | 20000 | $0.012120 |
| Ranked keywords | `dataforseo_labs/google/ranked_keywords/live` | all 2 rows | 20000 | $0.012240 |
| Relevant pages | `dataforseo_labs/google/relevant_pages/live` | all 2 rows | 20000 | $0.012240 |
| Backlink summary | `backlinks/summary/live` | 1 summary | 20000 | $0.024036 |
| Backlinks, one/domain | `backlinks/backlinks/live` | 1 of 1 row | 20000 | $0.024036 |
| Content search | `content_analysis/search/live` | 100 of 2,543 rows | 20000 | $0.027600 |
| Exact-brand SERP | `serp/google/organic/live/advanced` | 1 result page | 20000 | $0.002000 |
| Founder/category SERP | `serp/google/organic/live/advanced` | 1 result page | 20000 | $0.002000 |
| **Confirmed total** | **8 returned tasks** |  |  | **$0.116272** |

The audited returned-task total is **$0.116272**. One earlier category-SERP
transport attempt returned no body, ID, status, or cost; if it reached
DataForSEO and was billed at the normal $0.002 task price, total spend would be
**$0.118272**. Both figures are below the user-confirmed **$2 per-competitor
budget**. No paid ad archive call was made because no page, referral, or search
evidence created a specific paid-media hypothesis.

## Exact request bodies

### Domain overview

```json
[{"target":"airo.email","location_code":2840,"language_code":"en","ignore_synonyms":true}]
```

### Ranked keywords

```json
[{"target":"airo.email","location_code":2840,"language_code":"en","ignore_synonyms":true,"item_types":["organic","paid"],"limit":250,"order_by":["keyword_data.keyword_info.search_volume,desc"]}]
```

### Relevant pages

```json
[{"target":"airo.email","location_code":2840,"language_code":"en","ignore_synonyms":true,"limit":50,"order_by":["metrics.organic.etv,desc"]}]
```

### Backlink summary

```json
[{"target":"airo.email","include_subdomains":true,"exclude_internal_backlinks":true}]
```

### Backlinks, one per domain

```json
[{"target":"airo.email","include_subdomains":true,"exclude_internal_backlinks":true,"mode":"one_per_domain","limit":100,"order_by":["rank,desc"]}]
```

### Content Analysis

```json
[{"keyword":"Airo Mail","search_mode":"as_is","limit":100}]
```

### SERP: `airo mail`

```json
[{"keyword":"airo mail","location_code":2840,"language_code":"en","device":"desktop","os":"windows","depth":10}]
```

### SERP: `AI email client for solo founders`

```json
[{"keyword":"AI email client for solo founders","location_code":2840,"language_code":"en","device":"desktop","os":"windows","depth":10}]
```

## Audit identifiers

| Request | Task ID | Status | Cost |
| --- | --- | ---: | ---: |
| Domain overview | `07172055-2101-0388-0000-f1ea2cff010a` | 20000 | $0.012120 |
| Ranked keywords | `07172055-2101-0381-0000-f2e51736cdcb` | 20000 | $0.012240 |
| Relevant pages | `07172055-2101-0385-0000-3b5d3088c436` | 20000 | $0.012240 |
| Backlink summary | `07172055-2101-0265-0000-3674e8c0e182` | 20000 | $0.024036 |
| Backlinks | `07172055-2101-0269-0000-a520dbe6fc70` | 20000 | $0.024036 |
| Content Analysis | `07172055-2101-0463-0000-69ccd886477f` | 20000 | $0.027600 |
| Exact-brand SERP | `07172055-2101-0139-0000-6660aac4d3df` | 20000 | $0.002000 |
| Founder/category SERP | `07172056-2101-0139-0000-71f2a0c1c109` | 20000 | $0.002000 |

## Transport limitation

The first fixed batch ended before saving the final Airo category-SERP
response. It returned no body, task ID, status, or cost to reconcile. The same
one-object request was then sent once and returned the audited task above. The
eight-task total is exact for all returned tasks; the unreturned transport
attempt cannot be proven to have reached or been billed by DataForSEO. It is
therefore reported explicitly as a possible additional $0.002 rather than
silently assigned or omitted.

## Public metadata and webpage requests

Public pages and metadata inspected without entering the funnel included:

- `https://www.airo.email/`
- `https://www.airo.email/our_story`
- `https://www.airo.email/security`
- `https://www.airo.email/support`
- `https://www.airo.email/blog/best-email-apps-iphone`
- US App Store listing and Apple lookup API for app ID `6747727414`
- Google Play listing HTML for package `email.airo.rena`
- one disclosed Reddit conversation and the founder’s public LinkedIn profile
- Internet Archive CDX index for `airo.email/*`

Two archived Airo homepage captures were requested through Wayback. Both
returned the Wayback internal-error page rather than captured site content, so
only CDX timestamps and routes were used.

Initial public HTML and metadata responses were retained temporarily outside
the repository. All eight returned DataForSEO JSON responses are under
`/private/tmp` for this audit. Temporary files are not durable project evidence
and may disappear after cleanup; this ledger preserves every body, task ID,
status, cost, limit, and count used in the report.

## Inspection and evidence limits

- A rendered-browser session was attempted, but no browser was available.
- Current server-rendered initial HTML exposed the homepage message, CTAs,
  pricing, metadata, and tags; interaction state was not verified.
- Ranked Keywords and Relevant Pages returned their full two-row sets.
- Backlink detail returned its full one-row set.
- Content Analysis returned 100 of 2,543 matches. The generic name caused
  severe unrelated-brand and word-collision noise.
- Google Play displayed an install band, not unique activated users.
- Store, search, and backlink metadata do not expose paid attribution.

Deliberately not performed:

- app, package, installer, application, store artifact, or binary retrieval;
- artifact header/body request, mount, extraction, inspection, installation,
  launch, or execution;
- live-demo operation or CTA click;
- account or trial creation;
- Gmail, Google Workspace, Drive, Calendar, OAuth, or mailbox authorization;
- contact, newsletter, feedback, sales, or account form submission;
- pricing-toggle, checkout, subscription, or in-app purchase interaction; or
- authenticated web app, store app, or product inspection.
