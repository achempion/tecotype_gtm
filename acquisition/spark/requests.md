# Spark Mail DataForSEO request ledger

Requests were made on **2026-07-17**.

Search requests used Google, United States (`2840`), English, and
desktop/Windows where a device was required. Reusable endpoint and credential
guidance belongs in the central
[DataForSEO documentation](../../tools/dataforseo.md).

No credential was written to a repository file, command output, or this
report. Each POST contained exactly one task object. There were no malformed,
retried, or duplicated paid calls.

## Cost summary

| # | Request | Endpoint | Returned / task status | Cost (USD) |
| ---: | --- | --- | --- | ---: |
| 1 | Domain overview | `dataforseo_labs/google/domain_rank_overview/live` | 1 result; `20000 Ok` | 0.012120 |
| 2 | Ranked keywords | `dataforseo_labs/google/ranked_keywords/live` | 250 of 5,509 keywords; `20000 Ok` | 0.042000 |
| 3 | Relevant pages | `dataforseo_labs/google/relevant_pages/live` | 50 of 302 pages; `20000 Ok` | 0.018000 |
| 4 | Backlink summary | `backlinks/summary/live` | 1 summary; `20000 Ok` | 0.024036 |
| 5 | Backlinks, one/domain | `backlinks/backlinks/live` | 200 of 4,921 rows; `20000 Ok` | 0.031200 |
| 6 | Exact-domain content search | `content_analysis/search/live` | 100 of 579 items; `20000 Ok` | 0.027600 |
| 7 | Live organic SERP: `spark mail` | `serp/google/organic/live/advanced` | result page; `20000 Ok` | 0.002000 |
| 8 | Live organic SERP: `best email client` | `serp/google/organic/live/advanced` | result page; `20000 Ok` | 0.002000 |
| 9 | Live organic SERP: `email client for mac` | `serp/google/organic/live/advanced` | result page; `20000 Ok` | 0.002000 |
| 10 | Live organic SERP: `ai email assistant` | `serp/google/organic/live/advanced` | result page; `20000 Ok` | 0.002000 |
| 11 | Google Ads advertiser lookup | `serp/google/ads_advertisers/live/advanced` | Spark advertiser result; `20000 Ok` | 0.002000 |
| 12 | Google Ads creative lookup | `serp/google/ads_search/live/advanced` | 10 creatives; `20000 Ok` | 0.002000 |
|  | **Total** | **12 billed tasks** |  | **0.166956** |

The **$0.166956** total is below the confirmed **$2 per-competitor budget** and
is included in the Wave 2 aggregate research spend.

The Labs snapshot returned zero paid keywords while the separate Google Ads
archive returned current creatives. These endpoints measure different things:
the first is a modeled domain ranking snapshot; the second is a public
advertiser/creative archive.

## Task IDs

| # | DataForSEO task ID |
| ---: | --- |
| 1 | `07171933-2101-0388-0000-63bf92d65c13` |
| 2 | `07171933-2101-0381-0000-f4fb15341c53` |
| 3 | `07171933-2101-0385-0000-294b551cb485` |
| 4 | `07171934-2101-0265-0000-9d5e32919479` |
| 5 | `07171934-2101-0269-0000-695eaadd5ec3` |
| 6 | `07171934-2101-0463-0000-da11307e430e` |
| 7 | `07171935-2101-0139-0000-1264d8b95e50` |
| 8 | `07171935-2101-0139-0000-ebb22d01e37b` |
| 9 | `07171935-2101-0139-0000-2e8b4bc7662f` |
| 10 | `07171935-2101-0139-0000-850b99fd5b37` |
| 11 | `07171935-2101-0139-0000-f58a7e57d2bf` |
| 12 | `07171935-2101-0139-0000-d905faed19e9` |

## Exact request bodies

### 1. Domain overview

```json
[
  {
    "target": "sparkmailapp.com",
    "location_code": 2840,
    "language_code": "en",
    "ignore_synonyms": true
  }
]
```

Retained result:

| Metric | Result |
| --- | ---: |
| Organic keyword count | 5,509 |
| Organic ETV | 131,962.8024505 |
| Estimated organic paid-traffic cost | $338,059.5083 |
| Paid keyword count | 0 |
| Paid ETV | 0 |
| Marked new | 2,341 |
| Marked up | 1,331 |
| Marked down | 1,528 |

Position counts:

| Position group | Count |
| --- | ---: |
| 1 | 158 |
| 2–3 | 306 |
| 4–10 | 1,070 |
| 11–20 | 1,229 |
| 21–30 | 875 |
| 31–40 | 555 |
| 41–50 | 449 |
| 51–60 | 309 |
| 61–70 | 232 |
| 71–80 | 183 |
| 81–90 | 98 |
| 91–100 | 45 |

### 2. Ranked keywords

```json
[
  {
    "target": "sparkmailapp.com",
    "location_code": 2840,
    "language_code": "en",
    "ignore_synonyms": true,
    "item_types": ["organic", "paid"],
    "limit": 250,
    "order_by": ["keyword_data.keyword_info.search_volume,desc"]
  }
]
```

The aggregate metrics matched the domain overview. Representative retained
rows were:

| Keyword | Search volume | Rank | ETV | URL |
| --- | ---: | --- | ---: | --- |
| `spark` | 246,000 | group 6 / absolute 8 | 8,314.80 | homepage |
| `what does cc mean in email` | 40,500 | group 1 / absolute 3 | 12,312.00 | `/blog/email-cc-bcc-meaning` |
| `what does bcc mean in email` | 22,200 | group 3 / absolute 5 | 2,160.06 | `/blog/email-cc-bcc-meaning` |
| `email format` | 18,100 | group 4 / absolute 8 | 1,192.79 | `/formal-email-template` |

`spark` is ambiguous. The sample also contained multiple close CC/BCC variants
and generic Gmail-login rows at lower ranks. The request returned 250 of 5,509
keywords, ordered by volume, and is not a complete export.

### 3. Relevant pages

```json
[
  {
    "target": "sparkmailapp.com",
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
| `/blog/email-cc-bcc-meaning` | 93,409.113 | 508 |
| homepage | 12,814.205 | 536 |
| `/formal-email-template` | 10,103.621 | 309 |
| `/how-to-end-an-email-template` | 1,985.306 | 695 |
| `/how-to-email-professor-template` | 1,661.226 | 174 |
| `/professional-email-template` | 865.795 | 257 |
| `/guides/what-does-re-in-email-mean` | 840.263 | 47 |
| Spanish CC/BCC page | 771.599 | 24 |
| Archive-email guide | 724.251 | 37 |
| Outbox guide | 656.269 | 43 |

Calculated shares against total organic ETV:

- leading CC/BCC page: 70.784%;
- homepage: 9.710%;
- top three pages: 88.151%;
- top six pages: 91.571%.

Displayed rows are rounded, so recalculating from the display can produce
small differences.

### 4. Backlink summary

```json
[
  {
    "target": "sparkmailapp.com",
    "include_subdomains": true,
    "exclude_internal_backlinks": true
  }
]
```

Retained summary:

| Metric | Result |
| --- | ---: |
| Backlinks | 32,350 |
| Referring pages | 25,273 |
| Referring domains | 5,338 |
| Referring main domains | 4,737 |
| Rank | 370 |
| Spam score | 13 |
| Broken backlinks | 161 |

The backlink total is not a referral count. The TLD distribution and detail
sample showed substantial directory, shared-link, scraped, AI-generated, and
suspicious-domain noise.

### 5. Backlink detail

```json
[
  {
    "target": "sparkmailapp.com",
    "include_subdomains": true,
    "exclude_internal_backlinks": true,
    "mode": "one_per_domain",
    "limit": 200,
    "order_by": ["rank,desc"]
  }
]
```

The task returned 200 of 4,921 available one-per-domain rows. Credible examples
included:

- Readdle's portfolio;
- Product Hunt;
- C-Command's SpamSieve documentation;
- Mac4Ever;
- Lifehack;
- mail-provider setup/help pages.

Many other rows were software/AI directories, suspicious pages, or links to
Spark public shared-email URLs from unrelated domains.

A current Product Hunt target contained `?ref=producthunt`. This supports
attribution intent, not sessions or conversion.

### 6. Content Analysis

```json
[
  {
    "keyword": "sparkmailapp.com",
    "search_mode": "as_is",
    "limit": 100
  }
]
```

The task returned 100 of 579 items. The result mixed store pages,
localizations, MacRumors comments, mirrors, and low-quality reviews. It helped
locate specific public pages but was not used as an earned-media count.

### 7. Live organic SERP: `spark mail`

```json
[
  {
    "keyword": "spark mail",
    "location_code": 2840,
    "language_code": "en",
    "device": "desktop",
    "os": "windows",
    "depth": 10
  }
]
```

Observed:

- Spark homepage: organic group rank 1;
- iOS App Store: group 2;
- Google Play: group 3 / absolute 4;
- Reddit: group 4;
- YouTube review: group 5;
- Spark Desktop Mac App Store: group 6;
- Trustpilot: group 7.

### 8. Live organic SERP: `best email client`

```json
[
  {
    "keyword": "best email client",
    "location_code": 2840,
    "language_code": "en",
    "device": "desktop",
    "os": "windows",
    "depth": 10
  }
]
```

Observed: Spark was absent from the sampled top ten organic groups.

### 9. Live organic SERP: `email client for mac`

```json
[
  {
    "keyword": "email client for mac",
    "location_code": 2840,
    "language_code": "en",
    "device": "desktop",
    "os": "windows",
    "depth": 10
  }
]
```

Observed: Spark was absent from the sampled top ten organic groups.

### 10. Live organic SERP: `ai email assistant`

```json
[
  {
    "keyword": "ai email assistant",
    "location_code": 2840,
    "language_code": "en",
    "device": "desktop",
    "os": "windows",
    "depth": 10
  }
]
```

Observed: Spark was absent from the sampled top ten organic groups.

### 11. Google Ads advertiser lookup

```json
[
  {
    "keyword": "Spark Mail",
    "location_code": 2840
  }
]
```

Observed:

- advertiser domain: `sparkmailapp.com`;
- verified advertiser: Readdle Technologies Limited;
- advertiser ID: `AR04060914874270613505`.

This identifies a public advertiser record. It does not disclose spend,
targeting, delivery, clicks, or conversion.

### 12. Google Ads creative lookup

```json
[
  {
    "target": "sparkmailapp.com",
    "location_code": 2840,
    "platform": "all",
    "format": "all",
    "date_from": "2018-05-31",
    "date_to": "2026-07-17",
    "depth": 40
  }
]
```

The task returned 10 text, image, and video creatives for the verified
advertiser. Representative records:

| Creative ID | Format | First shown | Last shown |
| --- | --- | --- | --- |
| `CR04004910777063440385` | Text | 2026-03-16 | 2026-07-17 |
| `CR01901587020728238081` | Image | 2026-06-16 | 2026-07-17 |
| `CR18079509741242941441` | Video | 2026-05-26 | 2026-07-16 |

Several other text records remained present through 2026-07-16. An older text
record ran from 2025-07-28 through 2025-09-16.

The response was used to establish format and date presence only. Creative
message text was not extracted, and no claim is made about audience, delivery,
spend, impressions, clicks, installs, CAC, or conversion.

## Non-DataForSEO inspection record

Only public web, metadata, and rendered public-page surfaces were used:

- Spark homepage, pricing, about, privacy, help, AI Assistant, migration,
  case-study, team, and historical blog pages;
- public Apple metadata and App Store listings;
- public Google Play and Microsoft Store-related pages;
- Product Hunt, Setapp, Readdle, MacStories, TechCrunch, MacRumors, TechRadar,
  Trustpilot, and selected public Reddit discussions;
- public initial HTML and response headers;
- a rendered public homepage used to verify visible copy, links, scripts, and
  the cookie-choice dialog.

The Free download and Stripe checkout destinations were read only from public
link attributes. `/download` and checkout were not opened. The cookie dialog
was not interacted with.

No Spark client, installer, package, extension, or binary was downloaded,
fetched, mounted, installed, opened, inspected, or executed. No account,
mailbox authorization, trial, demo, form, store action, or purchase was
started.

## Reproducibility and interpretation rules

- Treat ETV, search volume, paid-traffic value, backlink rank, and spam score
  as provider models.
- Preserve the market, language, date, device, order, and limit with each
  result.
- Do not equate generic email search visibility with qualified client demand.
- Do not equate indexed backlinks with referral sessions or partners.
- Do not infer active or unique users from cumulative downloads or ratings.
- Do not infer ad delivery or effectiveness from archive records.
- Do not treat current plan rows labeled SOON as shipped product.
- Do not infer current data handling from historical AI announcements.
- Verify all public-platform and Tecotype release claims again immediately
  before publication.
