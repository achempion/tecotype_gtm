# Request ledger

Requests were made on **2026-07-17**. Search requests used Google US-English
and desktop where applicable.

Reusable endpoint and operating guidance belong in the central [DataForSEO
documentation](../../tools/dataforseo.md). This file records Quartz-specific
calls, direct HTTP observations, costs, and audit limitations.

## DataForSEO requests

| Category | Endpoint or request | Returned data | Cost |
| --- | --- | ---: | ---: |
| Search | `dataforseo_labs/google/domain_rank_overview/live` | 1 domain | $0.012120 |
| Search | `dataforseo_labs/google/ranked_keywords/live` | 3 keywords | $0.012360 |
| Search | Duplicate ranked-keyword call after local formatter failure | 3 keywords; first response not retained | $0.012360 |
| Search | `dataforseo_labs/google/relevant_pages/live` | 1 page | $0.012120 |
| Backlinks | `backlinks/summary/live` | 1 summary | $0.024036 |
| Backlinks | `backlinks/backlinks/live`, one per domain | 24 of 25 available rows | $0.024864 |
| Mentions | `content_analysis/search/live`, exact domain | 0 matches | $0.024036 |
| Mentions | Duplicate exact-domain call after empty-result formatter failure | 0 matches; first response not retained | $0.024036 |
| SERP | Branded `quartz mail` live check | 1 result page | $0.002000 |
| SERP | `quartz email client` live check | 1 result page | $0.002000 |
| SERP | `local AI email client` live check | 1 result page | $0.002000 |
| SERP | `private AI email client` live check | Internal search-engine error | $0.002000 |
| SERP | Initial multi-task live attempt beginning with `quartz mail` | First task charged; local response not retained | $0.002000 |
| **Total** | | | **$0.155932** |

Three additional tasks in one corrected live-SERP request were rejected with
“You can set only one task at a time” and cost $0.

## Main parameters

| Request group | Important parameters |
| --- | --- |
| Labs domain calls | `target: quartzmail.ai`, `location_code: 2840`, `language_code: en`, `ignore_synonyms: true` |
| Ranked keywords | Organic and paid items, limit 250 |
| Backlink summary/detail | Include subdomains, exclude internal links |
| Backlink detail | Live links, one result per domain, limit 200, rank descending |
| Content Analysis | Exact `"quartzmail.ai"`, `search_mode: as_is`, limit 100 |
| SERPs | Google US-English, desktop Windows, live advanced result |

## Audit identifiers

| Request | Task ID |
| --- | --- |
| Domain Rank Overview | `07171546-2101-0388-0000-063c81a60978` |
| Ranked Keywords, retained retry | `07171547-2101-0381-0000-48e056fd1303` |
| Relevant Pages | `07171547-2101-0385-0000-fe28542137b7` |
| Backlink Summary | `07171547-2101-0265-0000-a561ac7e6771` |
| Backlinks, one per domain | `07171547-2101-0269-0000-733cb27a90fe` |
| Content Analysis, retained retry | `07171548-2101-0463-0000-c067f4fd89dc` |
| Live SERP: `quartz mail` | `07171548-2101-0139-0000-c83fb8b4499b` |
| Live SERP: `quartz email client` | `07171549-2101-0139-0000-b2cf10edfa7a` |
| Rejected live SERP: local AI, batched | `07171549-2101-0139-0000-91b19e2d10f4` |
| Rejected live SERP: private AI, batched | `07171549-2101-0139-0000-ddcc7eb87023` |
| Rejected live SERP: Mac/local AI, batched | `07171549-2101-0139-0000-6ae1e8135077` |
| Live SERP: `local AI email client` | `07171549-2101-0139-0000-5ae8fe9eb9bd` |
| Live SERP: `private AI email client`, server error | `07171549-2101-0139-0000-5f2cd0dac419` |

The initial ranked-keyword call, initial Content Analysis call, and first
multi-task SERP response beginning with `quartz mail` were lost during local
output formatting and have no retained task ID. Their known costs are included
above.

## Direct public HTTP and browser observations

| Surface | Request or capture | Result |
| --- | --- | --- |
| Current homepage | Rendered browser capture | Current copy, CTA, metadata, scripts, links, and demo |
| `/download` | HEAD request | 307 to versioned v0.1.88 Apple Silicon DMG |
| Versioned DMG | HEAD request | 15,628,612 bytes; last modified June 27 |
| Update manifest | Public JSON | v0.1.88; published June 27 |
| App bundle | DMG mounted read-only; bundle inspected | arm64 app metadata, identifier, minimum macOS, signing, notarization, and static model reference; app not launched |
| Robots and sitemap | Public GET | `/ingest/` disallowed; four indexable sitemap URLs |
| Wayback CDX | Public index request | Distinct May 23 and June 17 landing-page captures |
| Archived pages | Rendered browser capture | Private waitlist and public launch funnels |
| Privacy, terms, contact | Rendered browser capture | Legal owner, free offer, telemetry, and local-processing boundary |
| Product Hunt | Current public page | Launch result, discussion, reviews, and release notes |
| Google Ads Transparency Center | Narrow brand/domain search | No relevant result found; not proof of no historical or other-network advertising |
| Referenced model repository API | Public JSON | Referenced GGUF size of 4,977,171,584 bytes |

No email address, OAuth credential, waitlist submission, app execution, or
payment action was used. Post-install onboarding was therefore not manually
walked. The DataForSEO Basic token was read from the configured macOS Keychain
item and was not printed or written to the repository.

## Audit limitations

- Complete raw DataForSEO response files were not retained in the repository.
- Two duplicate paid requests were needed after local formatting failures.
- One live multi-task SERP response beginning with `quartz mail` was not
  retained; the corrected API accepts only one live task at a time.
- Product Hunt counters are dynamic, and cached views returned slightly
  different point/follower values. The report uses the current overview capture
  of 278 points and 401 followers.
- Content Analysis returned no exact-domain rows even though the backlink index
  and manual research found many pages. Index coverage differs by endpoint.
- Installer and public-bucket artifacts prove release availability, not
  downloads or users.

## Reliability rules

- Search ETV, volume, rank history, and traffic are third-party estimates.
- An exact branded ranking does not establish category discovery.
- A backlink or parameterized URL does not prove a visit or attribution.
- Product Hunt points and followers do not prove a Quartz download.
- A first-party statement about hundreds of daily users has no published
  denominator, cohort, retention definition, or source.
- “Not found” community or advertising evidence is not proof of absence.
- Installed analytics and event names prove measurement capability, not event
  quality or a working source-to-activation report.
- No public evidence exposes Quartz's actual waitlist, download, OAuth,
  onboarding, activation, retention, payment, or revenue rates.
