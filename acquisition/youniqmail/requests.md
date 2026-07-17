# YouniqMail request ledger

Requests were made on **2026-07-17**. Search requests used Google US-English
and desktop Windows where applicable.

Reusable endpoint and credential guidance belong in the central
[DataForSEO documentation](../../tools/dataforseo.md). This file records exact
redacted request bodies, returned counts, costs, task identifiers, public HTTP
observations, and research limits.

## DataForSEO requests

| Category | Endpoint or request | Returned data | Cost |
| --- | --- | ---: | ---: |
| Search | `dataforseo_labs/google/domain_rank_overview/live` | 1 domain item | $0.012120 |
| Search | `dataforseo_labs/google/ranked_keywords/live` | 250 items of 395 | $0.042000 |
| Search | `dataforseo_labs/google/relevant_pages/live` | 19 pages | $0.014280 |
| Backlinks | `backlinks/summary/live` | 1 summary | $0.024036 |
| Backlinks | `backlinks/backlinks/live`, one per domain | 21 rows; `total_count: 24` | $0.024756 |
| Mentions | `content_analysis/search/live`, exact domain | 0 matches | $0.024036 |
| Mentions | `content_analysis/search/live`, exact brand plus category | 1 match | $0.024036 |
| Advertising | `serp/google/ads_advertisers/live/advanced` | 0 advertisers | $0.002000 |
| Advertising | `serp/google/ads_search/live/advanced` | 0 creatives | $0.002000 |
| SERP | `youniqmail email client` live check | 1 result page / 11 items | $0.002000 |
| SERP | `local first email client` live check | 1 result page / 11 items | $0.002000 |
| SERP | `privacy first email client` live check | 1 result page / 12 items | $0.002000 |
| **Total** | | | **$0.175264** |

The total is below the **$0.25** competitor cap.

There were no duplicate or malformed paid requests. The two Google Ads calls
returned task status `40102`, `No Search Results`, with the listed costs and
were not retried. All other paid tasks returned `20000`, `Ok`; all twelve task
IDs, including the two no-result statuses, appear below.

The Backlinks detail `total_count` of 24 differs from the 21 returned
one-per-domain rows and the summary's 21 referring domains. This ledger
preserves the API values rather than forcing them to agree.

## Credential handling

- The credential was read from the macOS Keychain service
  `dataforseo-base64`.
- It was used only in the in-memory Authorization header.
- The header and resolved credential were not printed or written to the
  dossier.
- All request bodies below omit authorization.

## Headline endpoint results

### Domain and keyword snapshot

The domain overview returned:

| Metric | Result |
| --- | ---: |
| Organic keywords | 395 |
| Organic ETV | 1,127.937285 |
| Estimated paid-traffic cost | $2,720.124044 |
| Organic positions 4–10 | 4 |
| Organic positions 11–20 | 56 |
| Organic positions 21–30 | 90 |
| Paid keywords / ETV | 0 / 0 |

The 250 returned keyword rows were ordered by search volume. The relevant-page
result contained 15 blog articles and four public tools. The two largest pages
were:

| Page | Keywords | ETV |
| --- | ---: | ---: |
| `what-is-cc-in-emails` | 84 | 524.675007 |
| `what-is-bcc-in-emails` | 93 | 466.173997 |

Combined ETV was 990.849004, 87.8% of the domain estimate.

### Backlinks

The backlink summary reported:

| Metric | Result |
| --- | ---: |
| Target rank | 37 |
| Backlinks | 37 |
| Referring domains | 21 |
| Referring main domains | 21 |
| Referring pages | 34 |
| Nofollow referring domains | 12 |
| Nofollow referring pages | 23 |
| Backlink spam score | 25 |
| First seen | 2025-08-02 20:46:14 UTC |

The 21 one-per-domain rows included:

- 8 dofollow and 13 nofollow rows.
- 9 relevant or contextually plausible sources.
- 12 generic reports, URL-share pages, low-context directories, or unrelated
  link pages.

Relevant rows and their first-seen dates:

| Domain | Source path or role | First seen |
| --- | --- | --- |
| `apprater.net` | YouniqMail listing with beta UTM | 2026-07-10 |
| `saashub.com` | Tatem alternatives | 2026-07-16 |
| `startupbuffer.com` | YouniqMail startup listing | 2026-05-04 |
| `getmailbird.com` | Editorial link to local-storage article | 2026-03-02 |
| `techproductivity.co` | Issue 360 | 2026-01-28 |
| `um.marketing` | Link to send-time article | 2026-05-01 |
| `patriciabarboza.co` | Link to send-time article | 2026-06-11 |
| `localfirstnews.com` | March 12 edition | 2026-03-18 |
| `startuptile.com` | September 22 listing | 2025-09-28 |

### Content Analysis

The exact-domain request for `youniqmail.com` returned no row.

The exact brand-plus-category request returned one
[AppRater listing](https://apprater.net/a/youniqmail-the-email-client-you-control/),
published July 7 and first fetched July 10.

The known Reddit, LinkedIn, BetaList, Local-First News, and feedback pages were
absent from Content Analysis. The endpoint result is therefore incomplete,
not evidence that those pages do not exist.

### Advertising

The advertiser request checked `youniqmail` in the United States and returned
no advertiser.

The creative request checked `youniqmail.com` across all supported platforms
and formats from 2018-05-31 through 2026-07-17 and returned no creative.

The domain overview also returned no paid ranking keyword.

These checks do not cover every ad identity, country, network, or private
campaign. Publicly configured Reddit, X, and LinkedIn pixels do not establish
media spend.

### Live SERPs

| Query | YouniqMail result |
| --- | --- |
| `youniqmail email client` | Homepage organic group rank 1 / absolute rank 2; LinkedIn #2; r/SideProject #3; X #4; AppRater #5 |
| `local first email client` | Founder r/emailprivacy post organic #3 / absolute #5; YouniqMail article organic #6 / absolute #8 |
| `privacy first email client` | Founder r/emailprivacy post organic #1 / absolute #2; no YouniqMail-domain organic result |

No paid item was present in the returned SERP items.

Detailed interpretation is in [traffic.md](./traffic.md).

## Main parameters

| Request group | Important parameters |
| --- | --- |
| Labs domain calls | `target: youniqmail.com`, `location_code: 2840`, `language_code: en`, `ignore_synonyms: true` |
| Ranked keywords | Organic and paid items, limit 250, search volume descending |
| Relevant pages | Limit 50 |
| Backlink summary/detail | Include subdomains and exclude internal links |
| Backlink detail | One result per domain, limit 200, rank descending |
| Content Analysis | Exact domain or exact brand-plus-category wording, `search_mode: as_is`, limit 100 |
| Ads Advertisers | Brand keyword, United States |
| Ads Search | Target domain, United States, all platforms and formats, full supported date range, depth 40 |
| Organic SERPs | Google US-English, desktop Windows, live advanced result, depth 10 |

Backlink and Content Analysis endpoints are not market- or device-specific.
The Ads Transparency endpoints used the United States location but do not
provide the same English-language and desktop controls as organic SERP.

## Exact request bodies

The authorization header is omitted. No resolved credential appears below.

### Domain Rank Overview

```json
[{
  "target": "youniqmail.com",
  "location_code": 2840,
  "language_code": "en",
  "ignore_synonyms": true
}]
```

### Ranked Keywords

```json
[{
  "target": "youniqmail.com",
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
  "target": "youniqmail.com",
  "location_code": 2840,
  "language_code": "en",
  "ignore_synonyms": true,
  "limit": 50
}]
```

### Backlinks Summary

```json
[{
  "target": "youniqmail.com",
  "include_subdomains": true,
  "exclude_internal_backlinks": true
}]
```

### Backlinks, one per domain

```json
[{
  "target": "youniqmail.com",
  "include_subdomains": true,
  "exclude_internal_backlinks": true,
  "mode": "one_per_domain",
  "limit": 200,
  "order_by": ["rank,desc"]
}]
```

### Content Analysis, exact domain

```json
[{
  "keyword": "youniqmail.com",
  "search_mode": "as_is",
  "limit": 100
}]
```

### Content Analysis, brand plus category

```json
[{
  "keyword": "\"YouniqMail\" email client",
  "search_mode": "as_is",
  "limit": 100
}]
```

### Google Ads Advertisers

```json
[{
  "keyword": "youniqmail",
  "location_code": 2840
}]
```

### Google Ads Search

```json
[{
  "target": "youniqmail.com",
  "location_code": 2840,
  "platform": "all",
  "format": "all",
  "date_from": "2018-05-31",
  "date_to": "2026-07-17",
  "depth": 40
}]
```

### Organic SERP: `youniqmail email client`

```json
[{
  "keyword": "youniqmail email client",
  "location_code": 2840,
  "language_code": "en",
  "device": "desktop",
  "os": "windows",
  "depth": 10
}]
```

### Organic SERP: `local first email client`

```json
[{
  "keyword": "local first email client",
  "location_code": 2840,
  "language_code": "en",
  "device": "desktop",
  "os": "windows",
  "depth": 10
}]
```

### Organic SERP: `privacy first email client`

```json
[{
  "keyword": "privacy first email client",
  "location_code": 2840,
  "language_code": "en",
  "device": "desktop",
  "os": "windows",
  "depth": 10
}]
```

## Audit identifiers

| Request | Task ID |
| --- | --- |
| Domain Rank Overview | `07171732-2101-0388-0000-2f676ba77c6b` |
| Ranked Keywords | `07171732-2101-0381-0000-00f6d2064030` |
| Relevant Pages | `07171732-2101-0385-0000-7b65ff245cfa` |
| Backlink Summary | `07171732-2101-0265-0000-ecd17eb392de` |
| Backlinks, one per domain | `07171732-2101-0269-0000-a50ba4c65591` |
| Content Analysis, exact domain | `07171732-2101-0463-0000-c52c23181e03` |
| Content Analysis, brand plus category | `07171732-2101-0463-0000-d80d2d5151fa` |
| Ads advertiser search | `07171732-2101-0139-0000-708e2c81c59f` |
| Ads creative search | `07171732-2101-0139-0000-752ffe0bf60d` |
| Live SERP: `youniqmail email client` | `07171733-2101-0139-0000-837824674dfc` |
| Live SERP: `local first email client` | `07171733-2101-0139-0000-1950dcc467b7` |
| Live SERP: `privacy first email client` | `07171733-2101-0139-0000-edadacdc5275` |

## Direct public request and observation ledger

| Surface | Public request or capture | Result |
| --- | --- | --- |
| [Homepage](https://youniqmail.com/) | Rendered logged-out visit at 1280 × 720 plus direct HTML GET | Blocking consent modal; beta v0.9.0; six direct artifact links; two Brevo forms; metadata and first-party click handler |
| Borlabs public config | First-party config script referenced by the homepage | GA4, Reddit, X, and LinkedIn optional services; all Off before consent |
| Homepage response headers | Public GET/HEAD metadata | Apache, security headers, current response metadata |
| Six artifact URLs | Header-only inspection; no artifact body requested | Status 200, lengths, modification dates, and available response headers |
| [Robots](https://youniqmail.com/robots.txt) | Public GET | Allows public site; disallows WordPress admin |
| [Sitemap](https://youniqmail.com/sitemap_index.xml) | Public GET | Post and page sitemap indexes |
| WordPress posts API | `wp-json/wp/v2/posts?per_page=100` | 28 posts and publication metadata |
| WordPress pages API | `wp-json/wp/v2/pages?per_page=100` | 17 public pages and publication metadata |
| [Feedback forum](https://feedback.youniqmail.com/) | Public Flarum discussion endpoints, limit 50 plus final offset | 53 discussions; 36 maker-created and 17 non-maker |
| [v0.9.0 update](https://feedback.youniqmail.com/d/53-beta-update-v090) | Public discussion endpoint | Created 2026-07-13; full first-party changelog |
| Wayback CDX | `youniqmail.com/*`, successful HTML, digest-collapsed | 193 rows in the returned index |
| Wayback homepage snapshots | 2025-08-18, 2025-10-10, 2026-03-14 | Waitlist, expanded privacy/features, then gated beta |
| Reddit profile and threads | Public logged-out pages and search | 33 submissions; scores/comments/removals and individual user statements |
| Third-party surfaces | Public BetaList, LinkedIn, Local-First News, AppRater, Startup Buffer, Startuptile, SaaSHub, and article pages | Placement and copy verification; no private analytics |

The feedback and Wayback API requests are public read-only requests. No
feedback, reply, account, consent, or form state was created.

## Artifact boundary

The research recorded artifact destinations from the homepage DOM and inspected
public response headers only.

It did **not**:

- Follow an artifact link in the rendered browser.
- Fetch an artifact body.
- Download or install a client.
- Execute a package.
- Inspect the package contents.
- Connect a mailbox.

Artifact sizes and response headers therefore describe distribution metadata,
not software behavior.

## Limitations

- DataForSEO is modeled and indexed, not first-party analytics.
- The US-English desktop market does not represent every geography or device.
- Ranked keywords were limited to 250 and ordered by search volume.
- A live SERP is a one-date sample.
- Backlink indexes include low-quality pages and can lag.
- Content Analysis missed several known pages.
- Reddit scores, comments, and relative dates can change.
- A forum issue suggests use but not continued use.
- Button click code proves measurement capability, not event volume.
- Header-only artifact inspection does not prove a completed download.
- No public evidence connects source, visit, download, install, connection,
  activation, retention, or payment for one person.
