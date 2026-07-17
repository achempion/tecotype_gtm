# Request ledger

Requests were made on **2026-07-17**. Search requests used Google US-English
and desktop Windows where applicable.

Reusable endpoint and operating guidance belong in the central [DataForSEO
documentation](../../tools/dataforseo.md). This file records Carbon Mail calls,
exact redacted request bodies, direct public observations, costs, and audit
limitations.

## DataForSEO requests

| Category | Endpoint or request | Returned data | Cost |
| --- | --- | ---: | ---: |
| Search | `dataforseo_labs/google/domain_rank_overview/live` | 0 items | $0.012000 |
| Search | `dataforseo_labs/google/ranked_keywords/live` | 0 organic or paid keywords | $0.012000 |
| Search | `dataforseo_labs/google/relevant_pages/live` | 0 pages | $0.012000 |
| Backlinks | `backlinks/summary/live` | 1 summary | $0.024036 |
| Backlinks | `backlinks/backlinks/live`, one per domain | 1 row | $0.024036 |
| Mentions | `content_analysis/search/live`, exact domain | 0 matches | $0.024036 |
| Mentions | `content_analysis/search/live`, exact brand plus category | 3 irrelevant matches | $0.024108 |
| Advertising | `serp/google/ads_advertisers/live/advanced` | 0 advertisers | $0.002000 |
| Advertising | `serp/google/ads_search/live/advanced` | 0 creatives | $0.002000 |
| SERP | `carbon mail email client` live check | 1 result page | $0.002000 |
| SERP | `on-device AI email client` live check | 1 result page | $0.002000 |
| SERP | `privacy-first email client` live check | 1 result page | $0.002000 |
| **Total** | | | **$0.142216** |

There were no duplicate or malformed paid requests in this ledger.

## Headline endpoint results

The backlink summary reported:

| Metric | Result |
| --- | ---: |
| Target rank | 56 |
| Backlinks | 4 |
| Referring domains | 1 |
| Referring main domains | 1 |
| Referring pages | 4 |
| Nofollow referring domains | 0 |
| Nofollow referring pages | 0 |
| Backlink spam score | 3 |
| First seen | 2026-02-09 |

The one-per-domain result was the live
[Find AI Tools Brazil listing](https://findaitools.com.br/produtividade/carbon-mail/):

| Field | Result |
| --- | --- |
| Source domain | `findaitools.com.br` |
| Target | `https://www.carbonmail.app/` |
| Anchor | `Visite o site` |
| Dofollow | Yes |
| Domain rank | 138 |
| Page rank | 0 |
| Backlink rank | 113 |
| First seen | 2026-02-09 |
| Last seen by the index | 2026-06-07 |

The exact-domain Content Analysis request returned no rows. The exact
`"Carbon Mail" email` request returned three unrelated pages: a Spanish page
about a coal business and two 2010 Blogspot theme pages. Neither request found
the known public Reddit posts.

Both Google Ads Transparency-derived calls returned `No Search Results`. The
advertiser call checked `carbon mail` in the United States. The creative call
checked `carbonmail.app` across all supported platforms and formats from
2018-05-31 through 2026-07-17.

The organic SERP results are reported in [traffic.md](./traffic.md).

## Main parameters

| Request group | Important parameters |
| --- | --- |
| Labs domain calls | `target: carbonmail.app`, `location_code: 2840`, `language_code: en`, `ignore_synonyms: true` |
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
provide the same English-language and desktop controls as the organic SERP
endpoint.

## Exact request bodies

The authorization header is omitted. No resolved credential appears below.

### Domain Rank Overview

```json
[{
  "target": "carbonmail.app",
  "location_code": 2840,
  "language_code": "en",
  "ignore_synonyms": true
}]
```

### Ranked Keywords

```json
[{
  "target": "carbonmail.app",
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
  "target": "carbonmail.app",
  "location_code": 2840,
  "language_code": "en",
  "ignore_synonyms": true,
  "limit": 50
}]
```

### Backlinks Summary

```json
[{
  "target": "carbonmail.app",
  "include_subdomains": true,
  "exclude_internal_backlinks": true
}]
```

### Backlinks, one per domain

```json
[{
  "target": "carbonmail.app",
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
  "keyword": "carbonmail.app",
  "search_mode": "as_is",
  "limit": 100
}]
```

### Content Analysis, brand plus category

```json
[{
  "keyword": "\"Carbon Mail\" email",
  "search_mode": "as_is",
  "limit": 100
}]
```

### Google Ads Advertisers

```json
[{
  "keyword": "carbon mail",
  "location_code": 2840
}]
```

### Google Ads Search

```json
[{
  "target": "carbonmail.app",
  "location_code": 2840,
  "platform": "all",
  "format": "all",
  "date_from": "2018-05-31",
  "date_to": "2026-07-17",
  "depth": 40
}]
```

### Organic SERP: `carbon mail email client`

```json
[{
  "keyword": "carbon mail email client",
  "location_code": 2840,
  "language_code": "en",
  "device": "desktop",
  "os": "windows",
  "depth": 10
}]
```

### Organic SERP: `on-device AI email client`

```json
[{
  "keyword": "on-device AI email client",
  "location_code": 2840,
  "language_code": "en",
  "device": "desktop",
  "os": "windows",
  "depth": 10
}]
```

### Organic SERP: `privacy-first email client`

```json
[{
  "keyword": "privacy-first email client",
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
| Domain Rank Overview | `07171619-2101-0388-0000-a07206972a87` |
| Ranked Keywords | `07171619-2101-0381-0000-0ba461486bdc` |
| Relevant Pages | `07171619-2101-0385-0000-146f0cf3fd70` |
| Backlink Summary | `07171619-2101-0265-0000-23275707a54f` |
| Backlinks, one per domain | `07171620-2101-0269-0000-2e93ebf1a175` |
| Content Analysis, exact domain | `07171620-2101-0463-0000-949cc6c77116` |
| Content Analysis, brand plus category | `07171620-2101-0463-0000-f3addc0bb67c` |
| Ads advertiser search | `07171620-2101-0139-0000-dc3190436828` |
| Ads creative search | `07171621-2101-0139-0000-d4d97f365d41` |
| Live SERP: `carbon mail email client` | `07171621-2101-0139-0000-62dfecbc1fb5` |
| Live SERP: `on-device AI email client` | `07171622-2101-0139-0000-36621a30d9b8` |
| Live SERP: `privacy-first email client` | `07171622-2101-0139-0000-df5686e58d6b` |

## Direct public HTTP and search observations

| Surface | Request or capture | Result |
| --- | --- | --- |
| [Current homepage](https://www.carbonmail.app/) | Rendered logged-out browser visit at 1280 × 720 plus direct HTTP GET | Current copy, metadata, feature claims, free-tier pledge, and `/login` CTAs; no rendered product screenshot, video, testimonial, customer logo, form, or consent interface |
| Homepage public links and scripts | Rendered visit and returned markup | Internal links to `/login` and `/privacy`; Next.js assets and Vercel Web Analytics; no visible external social link or observed Google Analytics, Google Tag Manager, Meta, LinkedIn, Reddit, PostHog, Hotjar, FullStory, Microsoft Clarity, HubSpot, Intercom, Optimizely, or VWO signature |
| [Login](https://www.carbonmail.app/login) | Rendered logged-out browser visit | Gmail-only connection page; says Carbon accesses only metadata for labeling and does not store content on its servers |
| Carbon “Security Check” | Clicked `Connect Your Gmail` on `/login` | Modal says Google will show “This app isn't verified,” requires acknowledgement, instructs `Advanced` → `Go to Carbon Mail (unsafe)`, and says CASA Tier 2 review is underway; stopped before continuing to Google |
| Public client JavaScript | Static inspection of scripts loaded by `/login` | Supabase Google OAuth requests `gmail.readonly`, `gmail.send`, and `gmail.modify`, offline access, and explicit consent; code also queries a hosted `user_tokens` table for an `access_token` |
| HTTP responses | Direct requests to `/`, `/login`, and `/privacy` | Homepage and login returned 200; privacy returned 404; homepage response showed Next.js/Vercel headers and no `Set-Cookie` header |
| [Privacy route](https://www.carbonmail.app/privacy) | Footer link and direct request | Returned 404 on the capture date |
| [Robots file](https://www.carbonmail.app/robots.txt) | Direct HTTP GET | Allows the public site and blocks product, account, authentication, API, and Next.js paths |
| [Sitemap](https://www.carbonmail.app/sitemap.xml) | Direct HTTP GET | Contains only the homepage, with `lastmod` `2026-01-27T20:47:59.343Z` |
| [February 2 archive](https://web.archive.org/web/20260202053315/https://www.carbonmail.app/) | Wayback CDX check and archived page | Only one distinct successful homepage digest was returned; the archive already has direct `/login` CTAs, the current-style message, and the free-tier pledge |
| [Find AI Tools listing](https://findaitools.com.br/produtividade/carbon-mail/) | Direct HTTP GET | Live Portuguese directory entry published 2026-02-03 with a direct `Visite o site` link |
| [Founder post in r/NoCodeSaaS](https://www.reddit.com/r/NoCodeSaaS/comments/1qoph6j/building_email_client_with_ondevice_ai_looking/) | Current public page | Beta positioning, `$0` spend statement, retention difficulty, and direct domain link |
| [Founder post in r/microsaas](https://www.reddit.com/r/microsaas/comments/1qo5zer/building_email_client_with_ondevice_ai_looking/) | Current public page | States “Reddit + X so far” and discusses a possible extension or pivot |
| Indexed-source checks | Exact domain/brand searches across public web results | Several Reddit copies found; no indexed Product Hunt, X, LinkedIn, or Hacker News result in the checked queries |
| Google Ads Transparency web-index check | Exact domain and brand site searches | No indexed result; not an authoritative archive search or proof of absence |

No email address, Google interstitial, Gmail authorization, account connection,
authenticated app execution, or payment action was used. The DataForSEO Basic
token was read from the configured macOS Keychain item and was not printed or
written to the repository.

## Audit limitations

- Complete raw DataForSEO responses were held only in temporary local files and
  were not retained in the repository.
- The Labs zero-item responses used `total_count: null`; they should not be
  rewritten as a definitive historical count of zero.
- Labs returned no ranked items even though the live branded SERP found the
  homepage. The endpoints have different update cycles and coverage.
- Live SERP ranks are a single-location, single-language, single-device
  observation and can change.
- The backlink detail call used one result per domain, so it exposes one
  representative source row rather than all four indexed referring pages.
- A manually verified live backlink proves publication, not referral clicks.
- Content Analysis missed known Reddit pages. Its zero exact-domain result is
  an index-coverage result, not evidence that no mentions exist.
- The brand Content Analysis query was vulnerable to name ambiguity and
  returned only unrelated rows.
- No Google Ads result does not prove that Carbon Mail never advertised.
  Another advertiser identity, country, domain, date, or network could produce
  different evidence.
- Public search-index checks do not fully cover social networks or private
  communities.

## Reliability rules

- Search rankings and visibility data are third-party observations, not Carbon
  Mail analytics.
- An exact branded ranking does not establish non-brand category discovery.
- A Reddit rank, vote, post, or backlink does not prove a visit or signup.
- A signup or Gmail connection would not by itself prove activation or
  retention.
- A founder statement about `$0` spend or next-day return is useful first-party
  evidence but has no published denominator, cohort, or analytics definition.
- No public evidence exposes Carbon Mail's actual acquisition, connection,
  activation, retention, payment, or revenue rates.
