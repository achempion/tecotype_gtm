# DataForSEO request ledger

Requests were made on **2026-07-17**. Search requests used Google US-English and desktop where applicable.

Reusable endpoint and operating guidance belong in the central [DataForSEO documentation](../../tools/dataforseo.md). This file records the Tatem calls, provenance, and audit limitations.

## Requests

| Category | Endpoint or request | Returned data |
| --- | --- | ---: |
| Search | `dataforseo_labs/google/domain_rank_overview/live` | 1 domain |
| Search | `dataforseo_labs/google/ranked_keywords/live` | 8 keywords |
| Search | `dataforseo_labs/google/relevant_pages/live` | 2 pages |
| Search | 5 × `serp/google/organic/live/advanced` | 5 top-10 SERPs |
| Backlinks | `backlinks/summary/live`, initial call | Response not retained by local extraction |
| Backlinks | `backlinks/backlinks/live`, one per domain | 100 of 113 available rows |
| Backlinks | `backlinks/backlinks/live`, tracked-target filter | 79 rows |
| Backlinks | `backlinks/domain_pages/live` | 93 pages |
| Backlinks | `backlinks/summary/live`, corrected extraction | 1 summary |
| Backlinks | `backlinks/history/live` | 54 monthly points |
| Mentions | `content_analysis/search/live` | 50 of 1,018 matches |
| Advertising | `serp/google/ads_advertisers/live/advanced` | 13 ambiguous advertisers |
| Advertising | `serp/google/ads_search/live/advanced` | 0 creatives |
| Trends | `keywords_data/dataforseo_trends/explore/live` | 130 weekly points |
| Opportunities | `dataforseo_labs/google/keyword_overview/live`, initial | 7 of 15 phrases; local output truncated |
| Opportunities | `dataforseo_labs/google/keyword_overview/live`, compact retry | 7 of 15 phrases |

One malformed `backlinks/domain_pages/live` request returned no data and is omitted.

## Main parameters

| Request group | Important parameters |
| --- | --- |
| Labs domain calls | `target: tatem.com`, `location_code: 2840`, `language_code: en`, `ignore_synonyms: true` |
| Ranked keywords | Organic and paid items, limit 100 |
| Backlink detail | Live links, exclude internal, one result per domain, limit 100 |
| Tracked backlinks | Target URL contains `utm`, `ref`, or `referrerId`, limit 100 |
| Backlink history | 2022-01-01 through 2026-07-17 |
| Content Analysis | Exact `"tatem"` plus `email`, limit 50 |
| Ads | Advertiser keyword `tatem`; creative target `tatem.com`, all platforms; no explicit historical range retained |
| Trends | US web search, 2024-01-01 through 2026-07-17, five terms |
| Keyword Overview | 15 candidate phrases, US-English |

## Audit identifiers

| Request | Task ID |
| --- | --- |
| Backlinks, one per domain | `07171417-2101-0269-0000-46c06a197f80` |
| Content Analysis | `07171417-2101-0463-0000-d4452947d74f` |
| Tracked backlinks | `07171418-2101-0269-0000-923c466b17bc` |
| Domain pages | `07171418-2101-0270-0000-df747912cdcd` |
| Corrected backlink summary | `07171418-2101-0265-0000-5f97e97165d7` |
| Backlink history | `07171419-2101-0266-0000-12d0b6d4bc46` |
| Ads advertiser search | `07171419-2101-0139-0000-5c7f88e54131` |
| Ads creative search | `07171419-2101-0139-0000-a762d16ae303` |
| Trends | `07171419-2101-0570-0000-c1f3eb45350e` |
| Live SERP: `tatem` | `07171420-2101-0139-0000-c2b5c32cb573` |
| Live SERP: `tatem email` | `07171420-2101-0139-0000-d66be1d65424` |
| Live SERP: keyboard query | `07171420-2101-0139-0000-2d37498b342f` |
| Live SERP: fast query | `07171420-2101-0139-0000-fc2fa3e0e852` |
| Live SERP: Gmail query | `07171420-2101-0139-0000-b3e05f7e1773` |
| Keyword Overview, first | `07171420-2101-0607-0000-8f58545d0f16` |
| Keyword Overview, retry | `07171421-2101-0607-0000-80bc370feb36` |

## Audit limitation

No raw API response files were retained in the repository:

- One response was lost during local extraction.
- One output was truncated and repeated.
- Several core calls have no task ID recorded here.
- The summary values cannot be independently replayed from repository artifacts alone.

The current report therefore uses these calls as a directional 2026 snapshot and keeps conclusions narrow. Based on the documented endpoint pricing, the listed successful calls are estimated at **$0.2358–$0.2598**, plus any charge for the malformed request. No new paid calls were made for the rewrite because that estimated spend was already near the research budget and historical public pages corrected the highest-impact errors.

If these calls are repeated, retain:

1. The redacted request body.
2. The complete response envelope and raw results.
3. Task ID, timestamp, and task cost.
4. The extraction used in the report.
5. Product-era classification for every referral or mention used.

## Reliability rules

- Search ETV, volume, CPC, difficulty, and intent are estimates.
- A current ranking does not reconstruct 2023–2025 acquisition.
- Backlink totals span different Tatem products.
- A backlink or parameterized URL is not a click or signup.
- The 50 returned Content Analysis rows were mostly irrelevant ambiguity; the relevance of all 1,018 reported matches was not validated.
- No Google ad result does not prove no historical advertising.
- Trend scores are relative indices.
- No competitor analytics, source-level conversion, activation, retention, payment, or revenue data was available.
