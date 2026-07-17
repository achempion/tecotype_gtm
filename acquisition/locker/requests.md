# Locker request ledger

Requests were made on **2026-07-17**. Search requests used Google US-English
and desktop Windows where applicable.

Reusable endpoint and credential guidance live in the central
[DataForSEO documentation](../../tools/dataforseo.md). This file records exact
redacted bodies, costs, task IDs, public browser and HTTP observations, GitHub
API results, and limitations.

No resolved credential is present below.

## DataForSEO requests

| Category | Endpoint or request | Returned data | Cost |
| --- | --- | ---: | ---: |
| Search | `dataforseo_labs/google/domain_rank_overview/live` | 0 items | $0.012000 |
| Search | `dataforseo_labs/google/ranked_keywords/live` | 0 items | $0.012000 |
| Search | `dataforseo_labs/google/relevant_pages/live` | 0 items | $0.012000 |
| Backlinks | `backlinks/summary/live` | 1 summary | $0.024036 |
| Backlinks | `backlinks/backlinks/live`, one per domain | 13 rows | $0.024468 |
| Mentions | `content_analysis/search/live`, exact domain | 1 irrelevant row | $0.024036 |
| Advertising | `serp/google/ads_advertisers/live/advanced` | No Search Results | $0.002000 |
| Advertising | `serp/google/ads_search/live/advanced` | No Search Results | $0.002000 |
| SERP | `inbox locker email client` | 1 result page | $0.002000 |
| SERP | `local AI email client Mac` | 1 result page | $0.002000 |
| SERP | `private AI email client Mac` | 1 result page | $0.002000 |
| **Total** | | | **$0.118540** |

Nine tasks returned `status_code: 20000`. Both Advertising tasks returned
`status_code: 40102`, `No Search Results`; their recorded $0.002000 costs are
included in the total.

There were no duplicate or malformed paid requests.

## Headline endpoint results

### Labs

All three Labs tasks completed successfully. Each returned zero items with
`total_count: null`. No modeled ETV or ranking metrics were available.

### Backlinks

The summary reported:

| Metric | Result |
| --- | ---: |
| Backlinks | 20 |
| Referring domains | 13 |
| Referring main domains | 13 |
| Referring pages | 19 |
| Broken backlinks | 0 |
| Broken pages | 0 |
| Backlink spam score | 35 |
| First seen | 2025-11-16 07:56:03 UTC |

The detail request returned 13 one-per-domain rows:

- 10 to `inbox.locker`.
- 3 to the separate `drop.inbox.locker` product.
- Two root-domain rows used explicit paid-backlink/PBN anchors and had spam
  scores 70 and 75.
- Several root-domain rows predated the current June 2026 email product.

The detail response reported `total_count: 15` while returning 13 rows. The
classification covers only the 13 returned rows and does not infer what
accounts for that response-level difference.

Detailed rows and their interpretation are in [referrals.md](./referrals.md).

### Content Analysis

The exact-domain request returned one old Portuguese-language page on
`yasteq.com`. Its content invited notifications from an entity called
“Inbox.locker” and was fetched in June 2025. It is not evidence about the
current Mac client.

### Advertising

Both Google Ads Transparency-derived calls returned `No Search Results`.

- Advertiser search: keyword `inbox locker`, United States.
- Creative search: target `inbox.locker`, United States, all supported
  platforms and formats, 2018-05-31 through 2026-07-17.

The result does not disprove historical ads under another identity, other
networks, or other markets.

### Live SERPs

For `inbox locker email client`:

- Homepage at absolute position 6.
- Founder Reddit post at absolute position 7.

For `local AI email client Mac` and `private AI email client Mac`:

- No `inbox.locker` result in the returned top-ten page.

Exact visible results are in [traffic.md](./traffic.md).

## Exact DataForSEO request bodies

### Domain Rank Overview

```json
[{
  "target": "inbox.locker",
  "location_code": 2840,
  "language_code": "en",
  "ignore_synonyms": true
}]
```

### Ranked Keywords

```json
[{
  "target": "inbox.locker",
  "location_code": 2840,
  "language_code": "en",
  "ignore_synonyms": true,
  "item_types": ["organic", "paid"],
  "limit": 250,
  "order_by": ["keyword_data.keyword_info.search_volume,desc"]
}]
```

### Relevant Pages

```json
[{
  "target": "inbox.locker",
  "location_code": 2840,
  "language_code": "en",
  "ignore_synonyms": true,
  "limit": 50
}]
```

### Backlink Summary

```json
[{
  "target": "inbox.locker",
  "include_subdomains": true,
  "exclude_internal_backlinks": true
}]
```

### Backlinks, one per domain

```json
[{
  "target": "inbox.locker",
  "include_subdomains": true,
  "exclude_internal_backlinks": true,
  "mode": "one_per_domain",
  "limit": 200,
  "order_by": ["rank,desc"]
}]
```

### Content Analysis

```json
[{
  "keyword": "inbox.locker",
  "search_mode": "as_is",
  "limit": 100
}]
```

### Google Ads Advertisers

```json
[{
  "keyword": "inbox locker",
  "location_code": 2840
}]
```

### Google Ads Search

```json
[{
  "target": "inbox.locker",
  "location_code": 2840,
  "platform": "all",
  "format": "all",
  "date_from": "2018-05-31",
  "date_to": "2026-07-17",
  "depth": 40
}]
```

### Organic SERP: `inbox locker email client`

```json
[{
  "keyword": "inbox locker email client",
  "location_code": 2840,
  "language_code": "en",
  "device": "desktop",
  "os": "windows",
  "depth": 10
}]
```

### Organic SERP: `local AI email client Mac`

```json
[{
  "keyword": "local AI email client Mac",
  "location_code": 2840,
  "language_code": "en",
  "device": "desktop",
  "os": "windows",
  "depth": 10
}]
```

### Organic SERP: `private AI email client Mac`

```json
[{
  "keyword": "private AI email client Mac",
  "location_code": 2840,
  "language_code": "en",
  "device": "desktop",
  "os": "windows",
  "depth": 10
}]
```

## DataForSEO audit identifiers

| Request | Task ID |
| --- | --- |
| Domain Rank Overview | `07171652-2101-0388-0000-2813111f1a57` |
| Ranked Keywords | `07171652-2101-0381-0000-34b12b88db25` |
| Relevant Pages | `07171652-2101-0385-0000-a99a3b6b7471` |
| Backlink Summary | `07171652-2101-0265-0000-8ea246cda58a` |
| Backlinks, one per domain | `07171652-2101-0269-0000-0a4467515bf7` |
| Content Analysis | `07171652-2101-0463-0000-4de001606746` |
| Ads advertiser search | `07171652-2101-0139-0000-66e6dee0abc5` |
| Ads creative search | `07171652-2101-0139-0000-6eb99b258e99` |
| SERP: exact brand | `07171653-2101-0139-0000-831beabfe204` |
| SERP: local AI | `07171653-2101-0139-0000-d96e7203b899` |
| SERP: private AI | `07171653-2101-0139-0000-67ea6103e6d6` |

## GitHub API observations

Public unauthenticated requests were made to:

```text
GET https://api.github.com/repos/newtophilly/locker-releases
GET https://api.github.com/repos/newtophilly/locker-releases/releases?per_page=100
```

Repository result:

| Field | Result |
| --- | --- |
| Created | 2026-06-23T16:37:06Z |
| Description | `Locker for Mac — signed, notarized downloads` |
| Stars / forks / open issues | 0 / 0 / 0 |
| Declared license | None |
| Archived / disabled | False / false |

The repository description and v0.1.0/v0.2.0 release wording are
publisher-authored signing/notarization claims. No disk image was fetched, so
code signing and notarization were not independently verified.

Release assets at capture:

| Tag | Asset | Bytes | Downloads | Published |
| --- | --- | ---: | ---: | --- |
| v0.1.0 | `Locker.dmg` | 113,072,932 | 6 | 2026-06-23T16:37:29Z |
| v0.2.0 | `Locker.dmg` | 113,376,118 | 4 | 2026-06-23T21:15:05Z |
| v0.3.0 | `Locker.dmg` | 158,996,673 | 17 | 2026-06-24T14:03:39Z |

GitHub counters are dynamic. Downloads are requests rather than unique users,
installs, activations, or retained users.

## Browser and public HTTP observations

| Surface | Capture | Result |
| --- | --- | --- |
| Homepage | Rendered desktop browser, 892 × 1033 CSS pixels | Current message, direct download, $39.99 offer, five keys shown as claimed, 10 of 10 paid spots shown left |
| Homepage markup and headers | Direct GET | Next.js on Vercel; metadata and first-party chunks; no recognizable client analytics tag |
| Checkout endpoint | Browser navigation only | Redirected to Polar for `Locker — Lifetime (Mac)`, $39.99 one-time charge |
| Checkout | Read-only inspection | Email, payment, name, address, tax, and discount fields; no submission |
| Privacy | Rendered public page | Provider, update, license, and optional cloud-AI network boundaries |
| Terms | Rendered public page | License tiers, payment, as-is terms, and update duration |
| Refunds | Rendered public page | Final-sale policy and try-before-buy framing |
| What's New | Rendered public page | v0.1.0–v0.3.0 released; v0.4.0 in testing |
| `/welcome` | Direct public GET | Polar email → copy key → Settings → License → Activate |
| `robots.txt` | Direct public GET | Site allowed; `/api/`, `/admin`, `/welcome`, `/design` disallowed |
| `sitemap.xml` | Direct public GET | Five public URLs |
| Reddit thread | Logged-out public view/search | One founder post, one interested comment, maker reply |
| Maker portfolio | Public search/open | No Locker or exact-domain reference found |

No:

- App installation.
- Disk-image download or execution.
- License claim.
- Purchase.
- Mailbox authorization.
- Account credential entry.
- Email submission.
- Checkout submission.

was performed.

## Wayback observations

The CDX query was:

```text
https://web.archive.org/cdx/search/cdx?url=inbox.locker/*&output=json&filter=statuscode:200&filter=mimetype:text/html&fl=timestamp,original,digest,statuscode&collapse=digest&from=2025&to=2026
```

It returned one successful homepage capture:

```text
20250716124225  http://inbox.locker/
```

The archived response redirected to `/lander`. No archived `/lander` page was
returned by a follow-up exact-path CDX query.

## Audit limitations

- Competitor analytics and payment data are private.
- Search and backlink data are third-party snapshots.
- Search indexing lag exposed an earlier title and page state.
- Wayback coverage is sparse.
- GitHub download counts can include repeats and internal testing.
- Code signing and notarization were not independently verified.
- The checkout was not submitted.
- The app was not run.
- The homepage and changelog disagree about several feature states.
- A negative public search does not prove a channel never existed.
