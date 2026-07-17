# Mailbird request and evidence ledger

Requests and observations were made on **2026-07-17**.

Search requests used Google United States, English, desktop Windows where
applicable. Reusable credential and endpoint guidance lives in
[DataForSEO documentation](../../tools/dataforseo.md). No credential is
included here.

Every live API POST made in the documented final pass contained **exactly one
task object**. No task was batched.

## DataForSEO final-pass cost ledger

| # | Category | Endpoint or query | Task ID | Status | Result | Cost |
| ---: | --- | --- | --- | ---: | --- | ---: |
| 1 | Search | Domain Rank Overview, first projection | `07171912-2101-0388-0000-7bac50dfad45` | 20000 | Successful; local projection omitted nested metrics | $0.012120 |
| 2 | Search | Domain Rank Overview, retained projection | `07171912-2101-0388-0000-c505e5c77775` | 20000 | 9,001 organic keywords | $0.012120 |
| 3 | Search | Ranked Keywords | `07171912-2101-0381-0000-e5832424f510` | 20000 | 250 rows | $0.042000 |
| 4 | Search | Relevant Pages | `07171913-2101-0385-0000-3d1974cf0d38` | 20000 | 50 rows; 1,098 total pages reported | $0.018000 |
| 5 | Backlinks | Summary | `07171913-2101-0265-0000-da7952aba808` | 20000 | 1 summary | $0.024036 |
| 6 | Backlinks | One per domain | `07171913-2101-0269-0000-1693e53858b8` | 20000 | 200 rows | $0.031200 |
| 7 | Mentions | `Mailbird email client` | `07171914-2101-0463-0000-d2b65dd7a701` | 20000 | 100 of 12,655 potential rows | $0.027600 |
| 8 | SERP | `mailbird` | `07171914-2101-0139-0000-feeec1827a14` | 20000 | Successful | $0.002000 |
| 9 | SERP | `best email client for windows` | `07171914-2101-0139-0000-ad85b2639913` | 20000 | Successful | $0.002000 |
| 10 | SERP | `email client for multiple accounts` | `07171914-2101-0139-0000-ca89d2e72ad3` | 20000 | Successful | $0.002000 |
| 11 | SERP | `outlook alternative windows` | `07171914-2101-0139-0000-eb5baef39038` | 20000 | Successful | $0.002000 |
| 12 | SERP | `gmail app for windows` | `07171915-2101-0139-0000-51d9a0fe8509` | 20000 | Successful | $0.002000 |
| 13 | Advertising | Advertiser lookup, `mailbird email client` | `07171915-2101-0139-0000-4e6a50328e98` | 40102 | No Search Results | $0.002000 |
| 14 | Advertising | Creative search, depth 40 | `07171915-2101-0139-0000-d71b6c0e1a48` | 20000 | 40 creatives | $0.002000 |
| 15 | Advertising | Creative format-field retry, requested depth 5 | `07171915-2101-0139-0000-31447b289078` | 20000 | Response again contained 40 creatives | $0.002000 |
| **Final-pass total** | | | | | **15 charged tasks** | **$0.183076** |

The first Domain Rank Overview was successful, but the local projection
discarded the nested metrics needed for the report. It was repeated with the
same API body, and both charges are disclosed.

The second creative request was made to retain raw format fields after the
first projection. The provider returned the same 40-creatives set despite a
requested depth of 5. Both charges are disclosed.

The advertiser lookup's `40102` status means that narrow keyword search found
no advertiser result. It was still a charged task and is not proof that
Mailbird has never advertised. The domain creative search independently found
the verified Mailbird advertiser and current creatives.

## Earlier same-day Mailbird responses found during audit

Three earlier Mailbird DataForSEO response files were present in the shared
temporary workspace. They predate the final pass and were not needed for the
final extraction, but their task IDs and costs are disclosed because they
target the same client:

| Category | Request | Task ID | Status | Result | Cost |
| --- | --- | --- | ---: | --- | ---: |
| Search | Domain Rank Overview | `07171856-2101-0388-0000-35e46fef90fa` | 20000 | Successful | $0.012120 |
| Search | Ranked Keywords, limit 250 | `07171857-2101-0381-0000-6b568a3fffe1` | 20000 | 250 rows | $0.042000 |
| Search | Relevant Pages, limit 100 | `07171857-2101-0385-0000-16fbf12c230a` | 20000 | 100 rows | $0.024000 |
| **Earlier-response total** | | | | **3 charged tasks** | **$0.078120** |

Counting these earlier responses gives an all-in total of **18 charged tasks
and $0.261196**. No further Mailbird paid requests were made after the earlier
spend was reconciled. The final report relies on the later, narrower pass and
keeps all earlier task costs visible. The audited all-in spend is below the
user-confirmed **$2 per-competitor budget**.

## Exact DataForSEO request bodies

Each body was sent as a one-element JSON array.

### Domain Rank Overview

Used for both final-pass overview calls and the earlier overview:

```json
[{
  "target": "getmailbird.com",
  "location_code": 2840,
  "language_code": "en",
  "ignore_synonyms": true
}]
```

Endpoint: `dataforseo_labs/google/domain_rank_overview/live`

### Ranked Keywords

```json
[{
  "target": "getmailbird.com",
  "location_code": 2840,
  "language_code": "en",
  "ignore_synonyms": true,
  "item_types": ["organic", "paid"],
  "limit": 250,
  "order_by": ["keyword_data.keyword_info.search_volume,desc"]
}]
```

Endpoint: `dataforseo_labs/google/ranked_keywords/live`

### Relevant Pages, final pass

```json
[{
  "target": "getmailbird.com",
  "location_code": 2840,
  "language_code": "en",
  "ignore_synonyms": true,
  "limit": 50,
  "order_by": ["metrics.organic.etv,desc"]
}]
```

Endpoint: `dataforseo_labs/google/relevant_pages/live`

The earlier response used the same body with `"limit": 100`.

### Backlink Summary

```json
[{
  "target": "getmailbird.com",
  "include_subdomains": true,
  "exclude_internal_backlinks": true
}]
```

Endpoint: `backlinks/summary/live`

### Backlinks, one per domain

```json
[{
  "target": "getmailbird.com",
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
  "keyword": "Mailbird email client",
  "search_mode": "as_is",
  "limit": 100
}]
```

Endpoint: `content_analysis/search/live`

### Live organic SERPs

Each query was sent in a separate one-element request:

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

- `mailbird`
- `best email client for windows`
- `email client for multiple accounts`
- `outlook alternative windows`
- `gmail app for windows`

### Google Ads advertiser lookup

```json
[{
  "keyword": "mailbird email client",
  "location_code": 2840,
  "device": "desktop",
  "os": "windows"
}]
```

Endpoint: `serp/google/ads_advertisers/live/advanced`

### Google Ads creative search, first pass

```json
[{
  "target": "getmailbird.com",
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

The format-field retry used the same body with `"depth": 5`.

## Headline endpoint results

### Labs

- 9,001 organic keywords and zero paid keywords in the current Labs snapshot.
- Modeled organic ETV of 90,881.0652.
- 1,098 relevant pages.
- Four provider-login pages among the five highest-ETV pages account for
  approximately 58.6% of modeled domain ETV.
- The homepage accounts for approximately 8.3%.

Full interpretation is in [traffic.md](./traffic.md).

### Backlinks and mentions

- 195,381 backlinks.
- 6,584 referring domains and 5,686 referring main domains.
- 116,079 referring pages.
- Approximately 88.5% of referring pages nofollow.
- Approximately 82.0% of referring pages associated with the Netherlands.
- 602 broken backlinks.
- 100 Content Analysis rows returned from 12,655 potential matches; leading
  rows were dominated by syndicated copies of the Mac-launch press release.

Full qualification is in [referrals.md](./referrals.md).

### Live SERPs

- `mailbird`: homepage absolute 1.
- `best email client for windows`: homepage absolute 6.
- `email client for multiple accounts`: homepage absolute 5.
- `outlook alternative windows`: Mailbird page absolute 6.
- `gmail app for windows`: no Mailbird-owned result in the returned organic
  top ten.

### Advertising

- Narrow advertiser-keyword lookup: no result.
- Domain creative lookup: verified advertiser ID
  `AR06045926643971653633`.
- Forty text, image, and video creatives.
- First-shown dates extend to 2021-10-25.
- Multiple creatives were last shown on 2026-07-17.
- Representative creative ID:
  `CR15358996444283404289`, text, first shown 2024-05-03 and last shown
  2026-07-17.

The archive does not expose targeting, spend, impressions, clicks, landing
conversion, activation, or CAC.

## Public web source ledger

| Surface | Direct source | Observation |
| --- | --- | --- |
| Homepage | [getmailbird.com](https://www.getmailbird.com/) | Copy, CTAs, metadata, structured data, scripts, tracking, and headers |
| Pricing | [Pricing](https://www.getmailbird.com/pricing/) | Free, annual, Pay Once, add-ons, feature matrix, FAQ, platform limitations |
| About | [About](https://www.getmailbird.com/about/) | Founding and first-party customer/account claims; stale Mac fragment |
| Business | [Business](https://www.getmailbird.com/mailbird-business/) | Features, team lead form, distributor, stale Mac fragment |
| Privacy | [Privacy policy](https://www.getmailbird.com/privacy-policy/) | Described collection, analytics, targeting, and personalization |
| Press | [Press archive](https://www.getmailbird.com/press/) | First-party coverage index |
| Blog | [Blog](https://www.getmailbird.com/blog/) | Current publishing cadence and newsletter surface |
| Sitemaps | [`robots.txt`](https://www.getmailbird.com/robots.txt), [`sitemap-main.xml`](https://www.getmailbird.com/sitemap-main.xml), [`sitemap-setup.xml`](https://www.getmailbird.com/sitemap-setup.xml) | Inventory and counts |
| Referral launch | [2013 multi-account post](https://www.getmailbird.com/multi-account-launch/) | Giveaway, referrals, loyalty points, and velocity claims |
| Referral milestone | [2016 one-million-account post](https://www.getmailbird.com/email-client-mailbird-celebrates-1m-email-accounts/) | Activated-account unit and referral credit |
| Referral reward | [2017 update](https://www.getmailbird.com/mailbird-updates-may-missed/) | Invite Friends and Pro Lifetime reward |
| Current gifting | [BOGO gift page](https://promos.getmailbird.com/) | Extra-license gifting route |
| Update entitlement | [Lifetime Updates support article](https://support.getmailbird.com/hc/en-us/articles/15354532511255-Why-am-I-being-charged-for-Lifetime-Updates) | Current and older update models |
| Free entitlement | [Free-plan support article](https://support.getmailbird.com/hc/en-us/articles/360026807893-Is-Mailbird-free) | One account, one user, one device |
| Device entitlement | [Device support article](https://support.getmailbird.com/hc/en-us/articles/220108347-Can-I-Use-my-Mailbird-License-Key-for-More-than-One-Computer) | Premium up to three devices |
| Mobile boundary | [Mobile support article](https://support.getmailbird.com/hc/en-us/articles/360014806554-Mailbird-for-Mobile-Android-iOS) | No current iOS/Android app |
| Mac history | [Mac article](https://www.getmailbird.com/mailbird-for-mac-users/) | First-party October 2024 launch date |
| Mac store | [US Mac App Store](https://apps.apple.com/us/app/mailbird-the-email-app/id6749447444?mt=12) | Version, prices, requirements, privacy disclosure, and reviews |
| Mac PR | [ACCESS Newswire release](https://via.tt.se/pressmeddelande/3699346/mailbird-expands-to-mac-popular-windows-email-client-launches-much-anticipated-mac-app?lang=en&publisherId=3236991) | Company press release and reach claims |
| Launch reporting | [TechCrunch](https://techcrunch.com/2013/04/01/mailbird-a-sparrow-like-client-for-windows-is-making-email-a-platform-not-just-an-application/) | Contemporary beta, offer, price, and roadmap reporting |
| Early review | [PCWorld](https://www.pcworld.com/article/457371/hands-on-with-mailbird-a-fast-slick-sparrow-inspired-email-client-for-windows.html) | Independent beta hands-on |
| License discussion | [r/software](https://www.reddit.com/r/software/comments/17k7eim/) and [r/Mailbird](https://www.reddit.com/r/Mailbird/comments/180r53m/) | Individual complaints; not a representative sample |
| Publisher route | [WindowsReport review](https://windowsreport.com/mailbird-review/) | Current tracked outbound links and commission disclosure; backlink index also recorded an older partner-specific target that no longer resolved |

Public page HTML, JavaScript, structured data, response headers, sitemaps,
store metadata, and a rendered public homepage were inspected. The rendered
pass verified visible headings, CTAs, the mobile email-link form, the
unaccepted cookie notice, script hosts, and the footer audience claim. No
control was clicked, no form was submitted, and no network capture was made,
so post-click behavior, state changes, cookie transmission, and request events
could not be tested.

## Actions deliberately not taken

- No Mailbird installer, disk image, package, application, or other client
  artifact was downloaded, fetched, installed, mounted, opened, inspected, or
  executed.
- No download CTA or installer route was activated.
- No Mailbird account or customer portal session was created.
- No mailbox or provider account was connected or authorized.
- No mobile email-link or business lead form was submitted.
- No trial was started.
- No checkout, purchase, refund, affiliate application, or support request was
  attempted.
- No private analytics, advertising account, affiliate dashboard, store
  console, customer list, or internal document was accessed.

## Remaining unknowns

The research does not reveal:

- first-party sessions and unique visitors;
- channel mix or source-level click-through;
- installer or store handoff success;
- unique installs;
- first launches;
- mailbox connections and completed syncs;
- first useful search, triage, or send actions;
- active users or cohort retention;
- referral invitations, acceptance, and referred retention;
- affiliate/partner clicks, commissions, or sales;
- ad spend, impressions, clicks, targeting, CAC, or incrementality;
- business leads, close rate, seats, or contract value;
- paid customers, refunds, churn, renewal, or net revenue; or
- actual consent and telemetry behavior in the rendered product/site.
