# Epistles request ledger

Requests and observations were made on **2026-07-17**.

Search requests used Google United States, English, desktop Windows where
applicable. Reusable endpoint and credential instructions live in
[DataForSEO documentation](../../tools/dataforseo.md). No credential is
included here.

## DataForSEO cost ledger

| Category | Endpoint or query | Task ID | Result | Cost |
| --- | --- | --- | --- | ---: |
| Search | Domain Rank Overview | `07171713-2101-0388-0000-05c350f455c0` | 1 summary; 4 organic keywords | $0.012120 |
| Search | Ranked Keywords | `07171713-2101-0381-0000-2017885c1dc0` | 4 rows | $0.012480 |
| Search | Relevant Pages | `07171713-2101-0385-0000-4434d5557651` | 2 rows | $0.012240 |
| Backlinks | Summary | `07171713-2101-0265-0000-4dd383f89755` | 1 summary | $0.024036 |
| Backlinks | One per domain | `07171713-2101-0269-0000-b166b39a2471` | 43 rows | $0.025548 |
| Mentions | Exact-domain Content Analysis | `07171713-2101-0463-0000-a61b1d9214b7` | 0 items | $0.024036 |
| Advertising | Advertiser search | `07171713-2101-0139-0000-902a5828f403` | `No Search Results` | $0.002000 |
| Advertising | Creative search | `07171714-2101-0139-0000-a95fdc78ab72` | `No Search Results` | $0.002000 |
| SERP | `epistles mail` | `07171714-2101-0139-0000-da6f533b59bd` | Successful | $0.002000 |
| SERP | `email client for multiple accounts` rerun | `07171714-2101-0139-0000-233f6343cca1` | Successful | $0.002000 |
| SERP | `mimestream alternative` rerun | `07171714-2101-0139-0000-03c7b9dd46aa` | Successful | $0.002000 |
| SERP | `proton mail client without bridge` rerun | `07171714-2101-0139-0000-3cb27934f524` | Successful | $0.002000 |
| **Total charged** | | | **12 tasks** | **$0.122460** |

The total is below the $0.25 competitor cap.

## Rejected zero-cost tasks

The first live organic SERP request incorrectly sent four task objects even
though this live endpoint accepts one at a time. DataForSEO processed the first
and rejected the other three with status `40000` and message
`You can set only one task at a time.`

| Query | Rejected task ID | Cost |
| --- | --- | ---: |
| `email client for multiple accounts` | `07171714-2101-0139-0000-fe990cd6e18b` | $0 |
| `mimestream alternative` | `07171714-2101-0139-0000-8a77bc62a184` | $0 |
| `proton mail client without bridge` | `07171714-2101-0139-0000-6fa2904e1af9` | $0 |

Each was rerun individually and charged once, as shown above. All returned task
IDs—charged and rejected—are recorded.

## Exact DataForSEO request bodies

### Domain Rank Overview

```json
[{
  "target": "epistles.com",
  "location_code": 2840,
  "language_code": "en",
  "ignore_synonyms": true
}]
```

### Ranked Keywords

```json
[{
  "target": "epistles.com",
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
  "target": "epistles.com",
  "location_code": 2840,
  "language_code": "en",
  "ignore_synonyms": true,
  "limit": 50
}]
```

### Backlink Summary

```json
[{
  "target": "epistles.com",
  "include_subdomains": true,
  "exclude_internal_backlinks": true
}]
```

### Backlinks, one per domain

```json
[{
  "target": "epistles.com",
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
  "keyword": "epistles.com",
  "search_mode": "as_is",
  "limit": 100
}]
```

### Google Ads advertiser search

```json
[{
  "keyword": "epistles mail",
  "location_code": 2840,
  "device": "desktop",
  "os": "windows"
}]
```

### Google Ads creative search

```json
[{
  "target": "epistles.com",
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

### Live organic SERPs

Each query below was sent as its own one-element request after the batching
error:

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

`QUERY` was exactly one of:

- `epistles mail`
- `email client for multiple accounts`
- `mimestream alternative`
- `proton mail client without bridge`

## Headline endpoint results

### Labs

- Domain Rank Overview: 4 organic keywords, 0 paid keywords, organic ETV
  0.328.
- Ranked Keywords: 4 rows, of which 3 pointed to the Mimestream alternative
  page and 1 irrelevant row pointed to the compare hub.
- Relevant Pages: Mimestream alternative page with 3 keywords / 0.244 ETV;
  compare hub with 1 keyword / 0.084 ETV.

Full interpretation is in [traffic.md](./traffic.md).

### Backlinks and mentions

The backlink summary returned 86 backlinks, 46 referring domains, 43
referring main domains, 84 referring pages, spam score 53, and a first-seen
date in 2019.

The detail response returned 43 one-per-domain rows. Most belonged to inherited
domain history, automated reports, nameserver lists, or spam. The Privacy
Guides discussion was the clearest current independent row. The Content
Analysis request returned no items.

Full qualification is in [referrals.md](./referrals.md).

### Live SERPs and advertising

- Exact brand: homepage absolute 1, Google Play absolute 4, Stalwart launch
  thread absolute 5, subreddit absolute 7.
- `mimestream alternative`: Epistles absolute 8.
- Other two category/problem queries: Epistles absent from the returned top
  ten.
- Both advertising calls: `No Search Results`.

## Public HTTP and browser source ledger

| Surface | URL or method | Observation |
| --- | --- | --- |
| Homepage | [epistles.com](https://epistles.com/) | Rendered desktop, source, metadata, scripts, structured data, headers |
| Download | [Download page](https://epistles.com/download/) | Store and direct-package routes |
| Pricing | [Pricing page](https://epistles.com/pricing/) | Free, annual, and lifetime offers |
| Annual gate | [Annual upgrade](https://app.epistles.com/upgrade?plan=annual) | Sign-in/create-account state only |
| Lifetime page | [Bereans](https://epistles.com/bereans/) | Offer, counter narrative, and promises |
| Lifetime counter | [Count endpoint](https://api.epistles.net/api/bereans/count) | First-party JSON snapshot |
| Security | [Security page](https://epistles.com/security/) | Data-path, telemetry, subprocessor, source, and carve-out claims |
| Privacy | [Privacy policy](https://epistles.com/privacy/) | Current described processing |
| Promises | [Promises page](https://epistles.com/promises/) | Marketing commitments |
| Terms | [Terms](https://epistles.com/terms/) | Current governing text compared with promises |
| Developers | [Developer page](https://epistles.com/developers/) | Source and roadmap statements |
| Changelog | [Changelog](https://epistles.com/changelog/) | 1.0–1.3.8 public release sequence |
| Sitemap | [`sitemap.xml`](https://epistles.com/sitemap.xml) | 25 URLs |
| Robots | [`robots.txt`](https://epistles.com/robots.txt) | Pricing exclusion and stale comment |
| Apple | [US App Store](https://apps.apple.com/us/app/epistles-mail/id6767441738) and iTunes lookup | Dates, version, seller, ratings, size |
| Google | [Google Play](https://play.google.com/store/apps/details?id=com.epistles) | Download band, version, developer, data-safety declarations |
| Packages | `repo.epistles.com` manifests reached from download page | Versions, dates, sizes, and hashes; manifest metadata only, with no artifact body or download counts |
| Wayback | CDX index plus selected captures | Old-domain separation and June 18 private beta |
| Reddit | Selected founder, independent, launch, and support threads | Dynamic scores and qualitative evidence |
| Privacy Guides | [Current thread](https://discuss.privacyguides.net/t/has-anybody-tried-epistles-mail/39055) | Low-value-account trial and telemetry/source objections |
| GitHub | Public founder profile/API | No public Epistles client source repo found in listed repositories |
| CASA assessor list | [App Defense Alliance public assessor list](https://appdefensealliance.dev/casa/casa-assessors) | TAC Security authorization corroborated; Epistles report not obtained |

## Actions deliberately not taken

- No Epistles account was created.
- No mailbox or provider account was connected.
- No package was downloaded, installed, or executed.
- No trial was started.
- No payment, refund, or support form was submitted.
- No private analytics, store console, source repository, customer list, or
  assessment report was accessed.

## Remaining unknowns

The work does not reveal:

- site sessions or CTA clicks;
- source-to-install attribution;
- exact unique installs;
- account-connection success;
- useful actions;
- active users or cohort retention;
- verified purchases, complimentary seats, refunds, or net revenue;
- the Epistles-specific CASA scope or findings; or
- actual client/backend behavior beyond public artifacts and claims.
