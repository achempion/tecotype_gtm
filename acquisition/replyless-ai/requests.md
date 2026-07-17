# ReplylessAI request ledger

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
| Ranked keywords | `dataforseo_labs/google/ranked_keywords/live` | all 11 rows | 20000 | $0.013320 |
| Relevant pages | `dataforseo_labs/google/relevant_pages/live` | all 5 rows | 20000 | $0.012600 |
| Backlink summary | `backlinks/summary/live` | 1 summary | 20000 | $0.024036 |
| Backlinks, one/domain | `backlinks/backlinks/live` | 42 of 44 rows | 20000 | $0.025512 |
| Content search | `content_analysis/search/live` | all 29 rows | 20000 | $0.025044 |
| Exact-brand SERP | `serp/google/organic/live/advanced` | 1 result page | 20000 | $0.002000 |
| Provider/category SERP | `serp/google/organic/live/advanced` | 1 result page | 20000 | $0.002000 |
| **Total** | **8 tasks** |  |  | **$0.116632** |

The total is below the user-confirmed **$2 per-competitor budget**. No paid ad
archive call was made because no landing-page or referral evidence created a
specific paid-media hypothesis.

## Exact request bodies

### Domain overview

```json
[{"target":"replyless.ai","location_code":2840,"language_code":"en","ignore_synonyms":true}]
```

### Ranked keywords

```json
[{"target":"replyless.ai","location_code":2840,"language_code":"en","ignore_synonyms":true,"item_types":["organic","paid"],"limit":250,"order_by":["keyword_data.keyword_info.search_volume,desc"]}]
```

### Relevant pages

```json
[{"target":"replyless.ai","location_code":2840,"language_code":"en","ignore_synonyms":true,"limit":50,"order_by":["metrics.organic.etv,desc"]}]
```

### Backlink summary

```json
[{"target":"replyless.ai","include_subdomains":true,"exclude_internal_backlinks":true}]
```

### Backlinks, one per domain

```json
[{"target":"replyless.ai","include_subdomains":true,"exclude_internal_backlinks":true,"mode":"one_per_domain","limit":100,"order_by":["rank,desc"]}]
```

### Content Analysis

```json
[{"keyword":"ReplylessAI","search_mode":"as_is","limit":100}]
```

### SERP: `replyless ai email`

```json
[{"keyword":"replyless ai email","location_code":2840,"language_code":"en","device":"desktop","os":"windows","depth":10}]
```

### SERP: `AI email client for Gmail Outlook Zoho`

```json
[{"keyword":"AI email client for Gmail Outlook Zoho","location_code":2840,"language_code":"en","device":"desktop","os":"windows","depth":10}]
```

## Audit identifiers

| Request | Task ID | Status | Cost |
| --- | --- | ---: | ---: |
| Domain overview | `07172055-2101-0388-0000-e388ce6f5ee1` | 20000 | $0.012120 |
| Ranked keywords | `07172055-2101-0381-0000-8ab1391c5a4a` | 20000 | $0.013320 |
| Relevant pages | `07172055-2101-0385-0000-2c9b7bd22774` | 20000 | $0.012600 |
| Backlink summary | `07172055-2101-0265-0000-bc523e8ddb6e` | 20000 | $0.024036 |
| Backlinks | `07172055-2101-0269-0000-f2b508c3df9b` | 20000 | $0.025512 |
| Content Analysis | `07172055-2101-0463-0000-ee9277e902ee` | 20000 | $0.025044 |
| Exact-brand SERP | `07172055-2101-0139-0000-be6d1e96a398` | 20000 | $0.002000 |
| Provider/category SERP | `07172055-2101-0139-0000-7bd6ee9a9148` | 20000 | $0.002000 |

## Public-web requests

Public pages inspected without entering a funnel included:

- `https://www.replyless.ai/`
- `https://www.replyless.ai/pricing`
- `https://www.replyless.ai/features`
- `https://www.replyless.ai/privacy`
- `https://blog.replyless.ai/`
- Product Hunt, Indie Hackers, LinkedIn, TrustMRR, Toolify, and Capterra pages
- Internet Archive CDX index for `replyless.ai/*`

Initial public HTML was retained temporarily outside the repository for the
homepage, pricing, and features pages. All eight DataForSEO JSON responses were
retained under `/private/tmp` for this audit. Temporary files are not durable
project evidence and may disappear after the environment is cleaned; this
ledger preserves every body, task ID, status, cost, limit, and reported count.

## Inspection and evidence limits

- A rendered-browser session was attempted, but no browser was available.
- Replyless hides the initial SEO shell after JavaScript starts, so rendered
  hero copy, consent state, and CTA behavior were not verified.
- Ranked Keywords returned all 11 modeled rows; Relevant Pages all five.
- Backlink detail returned 42 of 44 one-per-domain rows.
- Content Analysis returned all 29 rows, including mirrors and regional
  duplicates.
- DataForSEO models visibility and indexes links; it does not expose visits or
  customer attribution.

Deliberately not performed:

- client, app, extension, installer, package, or artifact retrieval;
- artifact header/body request, mount, extraction, inspection, installation,
  launch, or execution;
- account or trial creation;
- Gmail, Outlook, Zoho, IMAP, or other mailbox authorization;
- contact, newsletter, feedback, or account form submission;
- CTA click, checkout, payment, or pricing-toggle interaction; or
- authenticated dashboard or product inspection.
