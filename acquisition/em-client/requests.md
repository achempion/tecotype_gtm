# eM Client request and evidence ledger

Requests and observations were made on **2026-07-17**.

Search requests used Google United States, English, desktop Windows where
applicable. Reusable credential and endpoint guidance lives in
[DataForSEO documentation](../../tools/dataforseo.md). No credential is
included here.

Every live API POST contained **exactly one task object**. No task was batched.
The eM Client ledger is separate from every other client.

## DataForSEO cost ledger

| # | Category | Endpoint or query | Task ID | Status | Result | Cost |
| ---: | --- | --- | --- | ---: | --- | ---: |
| 1 | Search | Domain Rank Overview | `07171940-2101-0388-0000-28360c6e67d6` | 20000 | 5,500 organic keywords; 1 domain row | $0.012120 |
| 2 | Search | Ranked Keywords, limit 250 | `07171940-2101-0381-0000-8f34f03cf0da` | 20000 | 250 of 5,500 rows | $0.042000 |
| 3 | Search | Relevant Pages, limit 50 | `07171940-2101-0385-0000-a706e1f75f5d` | 20000 | 50 of 1,232 rows | $0.018000 |
| 4 | Backlinks | Summary | `07171940-2101-0265-0000-ed9ecaee9c3d` | 20000 | 1 summary row | $0.024036 |
| 5 | Backlinks | One per domain, limit 200 | `07171940-2101-0269-0000-ba5b03d3a026` | 20000 | 200 of 5,291 rows in endpoint result | $0.031200 |
| 6 | Mentions | `eM Client email client`, limit 100 | `07171940-2101-0463-0000-1076e7e14dd7` | 20000 | 100 of 96,130 potential rows | $0.027600 |
| 7 | SERP | `em client` | `07171941-2101-0139-0000-bfc5031d607c` | 20000 | Homepage absolute 1 | $0.002000 |
| 8 | SERP | `best email client for windows` | `07171941-2101-0139-0000-9e0371a80e67` | 20000 | No eM Client-owned result in returned top ten | $0.002000 |
| 9 | SERP | `outlook alternative windows` | `07171941-2101-0139-0000-a8441a282781` | 20000 | No owned result; independent eM Client review absolute 10 | $0.002000 |
| 10 | SERP | `email client for multiple accounts` | `07171941-2101-0139-0000-687357607903` | 20000 | No eM Client-owned result in returned top ten | $0.002000 |
| 11 | SERP | `email client for mac` | `07171941-2101-0139-0000-6b5212757d64` | 20000 | No eM Client-owned result in returned top ten | $0.002000 |
| 12 | Advertising | Advertiser lookup, `eM Client email client` | `07171941-2101-0139-0000-026744ecc1e7` | 40102 | No Search Results | $0.002000 |
| 13 | Advertising | Domain creative search, depth 40 | `07171942-2101-0139-0000-eba12ca0f762` | 20000 | 4 verified text creatives | $0.002000 |
| **Total** | | | | | **13 charged tasks** | **$0.168956** |

The audited **$0.168956** total is below the confirmed **$2 per-competitor
budget**.

Arithmetic:

```text
Labs             $0.072120
Backlinks        $0.055236
Content Analysis $0.027600
Five live SERPs  $0.010000
Two ad checks    $0.004000
Total            $0.168956
```

The advertiser lookup's `40102` is a charged task status meaning the narrow
keyword search returned no result. It is not proof that eM Client never
advertised. The domain creative query independently found verified advertiser
`eM Client s.r.o.` and four creatives.

No other same-day eM Client DataForSEO response was present in the inspected
temporary workspace before this pass.

## Exact DataForSEO request bodies

Each body below was sent as a one-element JSON array.

### Domain Rank Overview

```json
[{
  "target": "emclient.com",
  "location_code": 2840,
  "language_code": "en",
  "ignore_synonyms": true
}]
```

Endpoint: `dataforseo_labs/google/domain_rank_overview/live`

### Ranked Keywords

```json
[{
  "target": "emclient.com",
  "location_code": 2840,
  "language_code": "en",
  "ignore_synonyms": true,
  "item_types": ["organic", "paid"],
  "limit": 250,
  "order_by": ["keyword_data.keyword_info.search_volume,desc"]
}]
```

Endpoint: `dataforseo_labs/google/ranked_keywords/live`

### Relevant Pages

```json
[{
  "target": "emclient.com",
  "location_code": 2840,
  "language_code": "en",
  "ignore_synonyms": true,
  "limit": 50,
  "order_by": ["metrics.organic.etv,desc"]
}]
```

Endpoint: `dataforseo_labs/google/relevant_pages/live`

### Backlink Summary

```json
[{
  "target": "emclient.com",
  "include_subdomains": true,
  "exclude_internal_backlinks": true
}]
```

Endpoint: `backlinks/summary/live`

### Backlinks, one per domain

```json
[{
  "target": "emclient.com",
  "include_subdomains": true,
  "exclude_internal_backlinks": true,
  "mode": "one_per_domain",
  "limit": 200,
  "order_by": ["rank,desc"]
}]
```

Endpoint: `backlinks/backlinks/live`

### Content Analysis

```json
[{
  "keyword": "eM Client email client",
  "search_mode": "as_is",
  "limit": 100
}]
```

Endpoint: `content_analysis/search/live`

### Live organic SERPs

Each query was sent in its own one-object request:

```json
[{
  "keyword": "QUERY",
  "location_code": 2840,
  "language_code": "en",
  "device": "desktop",
  "os": "windows",
  "depth": 10
}]
```

Endpoint: `serp/google/organic/live/advanced`

`QUERY` was exactly one of:

- `em client`
- `best email client for windows`
- `outlook alternative windows`
- `email client for multiple accounts`
- `email client for mac`

### Google Ads advertiser lookup

```json
[{
  "keyword": "eM Client email client",
  "location_code": 2840,
  "device": "desktop",
  "os": "windows"
}]
```

Endpoint: `serp/google/ads_advertisers/live/advanced`

### Google Ads creative search

```json
[{
  "target": "emclient.com",
  "location_code": 2840,
  "platform": "all",
  "format": "all",
  "date_from": "2018-05-31",
  "date_to": "2026-07-17",
  "depth": 40,
  "device": "desktop",
  "os": "windows"
}]
```

Endpoint: `serp/google/ads_search/live/advanced`

## Headline endpoint results

### Labs

- 5,500 modeled organic ranking keywords.
- Organic ETV of 166,309.0115.
- Zero paid ranking keywords in the current Labs snapshot.
- 1,232 relevant pages.
- The ten leading pages were provider-help/navigation pages and contributed
  approximately 77.9% of domain ETV.
- The homepage contributed approximately 2.6%.

Full interpretation is in [traffic.md](./traffic.md).

### Backlinks and mentions

- 27,637 backlinks.
- 5,929 referring domains and 5,134 referring main domains.
- 24,212 referring pages.
- 11,127 nofollow referring pages, approximately 46.0%.
- 46 broken backlinks and 742 broken pages.
- 200 one-per-domain sample rows.
- 100 Content Analysis rows returned from 96,130 potential results.
- Sample quality mixed partners, providers, editorial coverage, syndication,
  owned forum threads, directories, coupon/download pages, and piracy.

Full qualification is in [referrals.md](./referrals.md).

### Live SERPs

- `em client`: homepage absolute 1.
- `best email client for windows`: no eM Client-owned returned top-ten result.
- `outlook alternative windows`: no owned returned top-ten result; independent
  TechHQ eM Client review absolute 10.
- `email client for multiple accounts`: no eM Client-owned returned top-ten
  result.
- `email client for mac`: no eM Client-owned returned top-ten result.

### Advertising

- Narrow advertiser-keyword lookup: no result.
- Domain archive lookup: verified advertiser ID
  `AR12287815946826940417`.
- Four text creatives.
- Earliest observed first-shown date: 2021-11-29.
- Three creatives were last shown on 2026-07-17.
- Representative creative ID `CR01848008093984620545`, first shown
  2026-05-26 and last shown on the research date.

The archive does not expose targeting, spend, impressions, clicks, landing
conversion, activation, CAC, or revenue.

## Public web source ledger

| Surface | Direct source | Observation |
| --- | --- | --- |
| Homepage | [emclient.com](https://www.emclient.com/) | Rendered message hierarchy, CTAs, social proof, platform sections, scripts, cookie control |
| Pricing | [Pricing](https://www.emclient.com/pricing) | Free, subscription, one-time, Personal/Business, trial, guarantee, feature matrix |
| Licensing | [Licensing](https://www.emclient.com/licensing) | Activation, offline state, usage/device rules, expiration, major-version rights |
| Free license | [Free license](https://www.emclient.com/free-license) | Registration fields and consent; form not submitted |
| Lifetime Upgrades | [Lifetime Upgrades](https://www.emclient.com/lifetime-upgrades) | Optional future-major entitlement and starting price |
| Privacy | [Privacy policy](https://www.emclient.com/privacy-policy) | Web, license, profiling, affiliate, analytics, AI, and mobile-push statements |
| Partner program | [Partners](https://www.emclient.com/partner-program) | 30%–45% margins, tiers, credits, enablement, finder, leads |
| Release history | [Windows history](https://www.emclient.com/release-history?os=win) | Long-running versions and current Windows release |
| Blog | [Blog](https://www.emclient.com/blog) | Current publishing, releases, previews, help |
| Robots and sitemap | [`robots.txt`](https://www.emclient.com/robots.txt), [`sitemap.xml`](http://www.emclient.com/sitemap.xml) | Crawl directives and 1,005-URL inventory |
| Version 8 | [Launch](https://www.emclient.com/blog/new-em-client-8-is-finally-here-388), [FAQ](https://www.emclient.com/blog/things-you-ask-about-em-client-8-396) | Major release and upgrade/offline explanation |
| Mobile beta | [Beta invitation](https://www.emclient.com/blog/come-test-the-beta-version-of-em-client-for-ios-and-android-566) | Public beta date and route |
| Mobile launch | [Official forum announcement](https://forum.emclient.com/t/em-client-for-ios-and-android-is-officially-here/96045) | Full iOS/Android launch |
| Version 10 | [Launch](https://www.emclient.com/blog/em-client-10-has-been-released-687) | Major release and licensing transition |
| Postbox announcement | [Postbox](https://www.postbox-inc.com/blog/entry/postbox-acquired-by-em-client) | Acquisition, shutdown, discounts, support dates |
| Acquisition release | [Press release](https://via.ritzau.dk/pressemeddelelse/14096605/em-client-acquires-postbox-inc-expanding-its-reach-to-a-broader-user-base?lang=en&publisherId=13562157) | First-party reach claims and acquisition framing |
| Migration guide | [Postbox-user guide](https://www.emclient.com/blog/em-client-guide-for-postbox-users-728) | Import, feature mapping, adopted/deferred behavior |
| Apple App Store | [iOS/iPadOS listing](https://apps.apple.com/us/app/em-client/id1561166404) | Current version, rating, languages, privacy card |
| Google Play | [Android listing](https://play.google.com/store/apps/details?hl=en-US&id=com.emclient.mailclient) | Download band, rating/reviews, current update, data-safety card |
| TechRadar | [Best clients](https://www.techradar.com/best/best-email-clients), [Postbox coverage](https://www.techradar.com/pro/em-client-acquires-postbox-enhancing-its-email-offerings-and-expanding-its-user-base) | Independent category assessment and acquisition coverage |
| Macwelt | [Mac review](https://www.macwelt.de/article/2631271/em-client-mac-test.html) | Independent Outlook-alternative assessment and cautions |
| SoftwareHow | [Review](https://www.softwarehow.com/em-client-review/) | Independent product assessment |
| Reddit | [Windows](https://www.reddit.com/r/Windows11/comments/1haxrw1), [software](https://www.reddit.com/r/software/comments/1bp8dng), [Windows alternative](https://www.reddit.com/r/Windows11/comments/1c4u1wz) | Anecdotal recommendations and complaints |

The sitemap advertises an HTTP URL; the live site itself uses HTTPS. No
disallowed or package route was requested.

## Rendered-page audit

The public homepage was rendered without clicking CTAs or cookie controls.
Observed:

- title `eM Client | The Best Email Client for Windows and Mac`;
- H1 copy “Boost your email / Skyrocket your productivity”;
- desktop/mobile, workflow, team, feature, and compatibility sections;
- first-party claim of more than 100,000 businesses and four million users;
- visible Pricing, Free download, and Get Free License routes;
- Windows, macOS, Android, and iOS routes;
- Google Workspace, Office 365, Outlook, and Exchange compatibility;
- scripts or hosts associated with Google Tag Manager, Google Analytics,
  Microsoft/Bing, LinkedIn, SharpSpring, Trustpilot, OpenWidget, first-party
  services, and Cloudflare Insights;
- an Accept cookie control; and
- no visible lead/signup form on the homepage beyond ASP.NET infrastructure
  fields.

Direct desktop setup links existed in the DOM but were not activated or
requested. Their artifact URLs are deliberately omitted.

## Deliberately not done

- No client, installer, setup package, application bundle, disk image, archive,
  store app, or old version was requested, saved, opened, mounted, installed,
  inspected, or executed.
- No direct artifact URL discovered in the page, robots file, backlink sample,
  store, or search result was followed.
- No Free download CTA was clicked.
- No free license was requested.
- No trial or account was started.
- No mailbox or calendar was authorized.
- No partner, business, support, or contact form was submitted.
- No FastSpring checkout was opened.
- No Apple App Store or Google Play install action was used.
- The cookie banner was not accepted or declined.
- No consent-state network comparison was performed.
- No application telemetry, local storage, database, or executable was
  inspected.
- No source was contacted and no private analytics were requested.
- No paid API request beyond the 13 disclosed tasks was made.

The local research material consisted only of public website HTML/JavaScript,
headers, robots/sitemap text, rendered public-page observations, and public API
JSON responses.

## Evidence limits

Unknowns include:

- first-party sessions and unique visitors;
- channel mix and attribution;
- free-license form completion;
- setup and activation;
- account connection and sync;
- import success;
- first useful action;
- day/week/month retention;
- free-to-paid conversion;
- subscription renewal and one-time upgrade;
- refunds and cancellations;
- support burden;
- partner applications, sales, and retention;
- Postbox offer redemption and migrated cohorts;
- mobile-to-desktop cross-use;
- ad spend, impressions, clicks, CAC, and payback;
- privacy/consent network behavior; and
- active/paid definitions behind audience claims.

Provider estimates, public pages, release histories, store metadata, press,
reviews, links, and archived creatives establish visible activity. They do not
fill those gaps.
