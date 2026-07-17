# Epistles search traffic

Research date: **2026-07-17**

Market: **Google United States, English, desktop Windows**

Target: **`epistles.com`, including subdomains only for the backlink calls**

DataForSEO Labs is an estimated search model. The live SERPs are current
visible result pages. Neither source is Epistles analytics, and neither can
show a click, install, connected account, useful mail action, payment, or
retained user.

## Headline result

Epistles has one early purchase-adjacent search result, but not a general
organic-acquisition engine.

- Labs modeled four ranking keywords and **0.328 estimated visits**.
- Three of the four keyword rows point to the
  [Mimestream alternative page](https://epistles.com/mail/mimestream-alternative/).
- A current live check placed that page at absolute position **8** for
  `mimestream alternative`.
- Epistles was absent from the returned top ten for
  `email client for multiple accounts` and
  `proton mail client without bridge`.
- Exact-brand search was healthy after awareness existed: the homepage ranked
  first, the Google Play listing fourth, the Stalwart launch thread fifth, and
  the branded subreddit seventh.

The result is meaningful for a product that reached general availability nine
days before the snapshot. It is still too small to establish repeatability.

## Labs snapshot

| Metric | Result |
| --- | ---: |
| Organic keyword count | 4 |
| Organic ETV | 0.328 |
| Paid keyword count | 0 |
| Ranked pages | 2 |
| Mimestream-page keywords | 3 |
| Mimestream-page ETV | 0.244 |
| Compare-hub keywords | 1 |
| Compare-hub ETV | 0.084 |

ETV is DataForSEO's estimated traffic volume for the modeled rankings, not a
visitor count from Epistles.

## Modeled keyword rows

| Keyword | Group rank | Absolute rank | Search volume | ETV | Destination | Interpretation |
| --- | ---: | ---: | ---: | ---: | --- | --- |
| `mimestream alternative` | 13 | 16 | 20 | 0.118 | `/mail/mimestream-alternative/` | Relevant, purchase-adjacent query |
| `mime stream` | 51 | 58 | 30 | 0.063 | `/mail/mimestream-alternative/` | Relevant brand variant, too low to expect material clicks |
| `mimestream download` | 62 | 70 | 30 | 0.063 | `/mail/mimestream-alternative/` | Relevant competitor query, weak rank |
| `www lexulous com email version` | 76 | 84 | 40 | 0.084 | `/compare/` | Semantically irrelevant artifact |

The live Mimestream check was stronger than the Labs snapshot. That can reflect
normal time, device, and model differences; it should not be averaged into a
synthetic rank.

## Live SERPs

### `epistles mail`

Observed Epistles-controlled or Epistles-specific results:

| Absolute position | Result |
| ---: | --- |
| 1 | [Epistles homepage](https://epistles.com/) |
| 4 | [Google Play listing](https://play.google.com/store/apps/details?id=com.epistles) |
| 5 | [Stalwart 1.0 launch thread](https://www.reddit.com/r/stalwartlabs/comments/1uqu9y2/epistles_mail_10_is_now_available/) |
| 7 | [r/EpistlesMail](https://www.reddit.com/r/EpistlesMail/) |

The query is ambiguous: unrelated “Epistle” products and academic results also
appeared. Epistles nevertheless captures the most important exact-brand result.

### `mimestream alternative`

The [Epistles comparison page](https://epistles.com/mail/mimestream-alternative/)
appeared at absolute position **8**.

That is the dossier's clearest SEO win because it sits close to a product
choice. Click-through and conversion are unknown, and the query's modeled US
monthly volume was only 20.

### `email client for multiple accounts`

No `epistles.com` result appeared in the returned top ten.

This directly tests the broad homepage promise. The absence means the current
comparison inventory has not translated into visible general-category reach.

### `proton mail client without bridge`

No `epistles.com` result appeared in the returned top ten.

Epistles has a distinctive implementation claim and public Proton discussions,
but did not own this narrow problem query in the captured result page.

## Index and content inventory

The current sitemap lists **25 URLs**, including:

- homepage, download, FAQ, security, promises, watch, developers, changelog,
  Linux, support, privacy, and terms;
- a comparison hub; and
- 12 alternative pages for Newton, Mimestream, Gmail, Outlook, Proton,
  Apple Mail, Fastmail, Spark, Superhuman, Canary, Thunderbird, and Mailbird.

The homepage also carries `SoftwareApplication`, `Organization`, `WebSite`,
`WebPage`, and `FAQPage` structured data. This is a deliberate
search-and-answer surface, although its general-availability chronology is
stale relative to the public changelog.

Two purchase pages are not part of the indexable acquisition inventory:

- `/pricing/` is disallowed by `robots.txt` and marked `noindex, nofollow`;
- `/bereans/` is marked `noindex, nofollow`.

The robots comment still calls pricing unreleased even though the launched
homepage links to it. This may be deliberate conversion-page exclusion, stale
launch configuration, or both.

## Backlink and mention boundary

The backlink summary reported 86 backlinks from 46 referring domains, but
domain reuse makes that headline misleading:

- many rows are nameserver lists, automated website reports, low-quality
  directories, or old pages for prior uses of `epistles.com`;
- one current, directly captured independent link is the
  [Privacy Guides discussion](https://discuss.privacyguides.net/t/has-anybody-tried-epistles-mail/39055);
- a DataForSEO row pointed to a
  [Mac Power Users thread](https://talk.macpowerusers.com/t/what-email-clients-are-people-using-in-2026/45455?page=4),
  but Epistles was not visible in the current captured page, so it is treated
  as stale, removed, or displaced rather than a verified referral;
- the exact-domain Content Analysis request returned no items.

Backlink detail is in [referrals.md](./referrals.md).

## Paid-search check

The Google Ads advertiser and creative-archive requests both returned
`No Search Results`.

That means no matching creative was found in the narrow identity, country,
platform, format, and archive checks. It does not prove Epistles has never
advertised under another identity, network, market, or date.

## Acquisition conclusion

Current organic acquisition is:

1. strong exact-brand capture after somebody already knows the name;
2. one early Mimestream-comparison result;
3. a broad indexable inventory whose other pages have not yet produced modeled
   visibility; and
4. essentially no measured category reach.

For Tecotype, the useful pattern is not “publish 12 comparison pages.” It is to
earn one release-accurate answer for one real switching problem and tag the
entire path from discovery to retained use. A ranking is an intermediate
signal, not demand or product-market fit.

Exact request bodies, costs, and task IDs are in
[requests.md](./requests.md).
