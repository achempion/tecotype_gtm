# Locker acquisition report

Research date: **2026-07-17**

Scope: **Locker, the Mac email client at `inbox.locker`; the founder's
`drop.inbox.locker` file-transfer product and unrelated “Locker” brands are
excluded**

Market: **Google US-English, desktop where applicable**

Locker is a very early Apple Silicon email client that its founder describes
as solo-built. Its public evidence connects a founder beta request, a free
direct download, five claimed giveaway licenses, and a separate paid checkout
handoff. It does not connect any of those surfaces to account connection,
useful mail work, retained use, or paid conversion.

The current homepage also presents several capabilities as part of the product
while its own changelog labels overlapping work as the next release “in
testing.” Conclusions below use the public v0.3.0 release as the shipped
boundary.

No disk image was fetched or executed, and the app was not installed or
launched. Signing, notarization, install behavior, and post-install product
behavior were not independently verified.

## Executive answer

The strongest public evidence of how people discover Locker is:

1. **One founder Reddit beta request.** The June 24 post offered free lifetime
   access to people willing to provide feedback. The captured thread had a
   score of +1, one interested reply, and a maker response pointing to free
   keys and the direct download.
2. **A friction-light public download.** The homepage links directly to the
   latest Mac disk image. The publisher describes the repository's downloads
   as signed and notarized, but this was not independently verified. GitHub
   showed 27 disk-image downloads across three releases, including 17 for
   v0.3.0. These are asset requests, not unique installs or active users.
3. **Weak exact-brand capture.** The homepage appeared at absolute position 6
   and the Reddit post at absolute position 7 for `inbox locker email client`.
   DataForSEO Labs returned no ranked domain keywords or relevant pages.
4. **No credible backlink program.** The domain-level summary included 20
   links from 13 referring domains, but the detailed rows were old domain
   artifacts, obvious backlink spam, generic report pages, or links to the
   separate Locker Drop product.

The homepage said all five free keys had been claimed while its paid counter
still showed “10 of 10 left” at $39.99. If the counter is accurate, that is
consistent with free tester interest but no completed paid founder sale.
Neither counter exposes activation or retention, and the free-key claims
cannot be attributed to Reddit.

The most defensible lesson is:

> A precise local-privacy story and a download-before-payment path can make a
> new product easy to try. Scarcity counters, asset downloads, and claimed
> keys still do not establish a usable primary inbox or willingness to pay.

## Headline evidence

| Signal | Observed result | Boundary |
| --- | ---: | --- |
| Public Reddit beta posts found | 1 | Narrow public search; other posts or deleted submissions may exist |
| Visible Reddit response | +1 and one interested comment | Dynamic engagement, not activation |
| Homepage free-key display | 5 of 5 shown as claimed | Counter implementation, source, account connection, use, and retention unknown |
| $39.99 founder inventory | 10 of 10 left | Visible counter; implementation and purchase completeness are unverified |
| Current public release | v0.3.0 | v0.4.0 is explicitly “in testing” |
| v0.3.0 disk-image downloads | 17 | Requests, not unique installs |
| Disk-image downloads across v0.1.0–v0.3.0 | 27 | May include the maker, repeat users, and update testing |
| Labs ranked keywords / relevant pages | 0 / 0 returned items | Current Google US-English snapshot, not an all-time zero |
| Exact-brand SERP | Homepage absolute 6; Reddit post absolute 7 | Rank can change; clicks unknown |
| Raw backlinks / referring domains | 20 / 13 | Includes subdomains, spam, pre-product artifacts, and a separate product |
| Relevant Google ad creatives found | 0 | Narrow archive coverage; historical paid use is not disproven |
| DataForSEO cost | $0.118540 | Eleven calls in one market |

## Discovery paths

The only public path with a visible human response is:

```text
Founder beta request
→ r/software self-promotion thread
→ one interested commenter
→ homepage or direct conversation
→ free key or direct download
→ install, mailbox connection, first value, and retention unknown
```

The public trial and purchase paths are separate:

```text
Existing awareness or exact-brand search
→ homepage
→ direct GitHub disk-image download
→ local license and mailbox setup
→ useful mail action and return unknown
```

```text
Homepage founder offer
→ $39.99 Polar checkout, submission not tested
→ publisher says Polar sends a license key by email
→ paste key in Locker settings
→ mailbox connection, activation, and retention unknown
```

## Channel scorecard

| Channel | Observed activity | Downstream signal | Contrary evidence or limitation | Verdict | Confidence |
| --- | --- | --- | --- | --- | --- |
| Founder Reddit post | One June 24 beta request with a free-lifetime offer | One interested comment and maker reply | +1 score; no source tags or user outcome | Only visible community path; very small signal | High for activity |
| Direct GitHub download | Three public releases and 27 disk-image requests | v0.3.0 had 17 requests | Downloads are not unique installs, mailbox connections, or retained users | Observable trial surface; outcome unknown | High |
| Free-key giveaway | Five keys shown as claimed | Five claims | Source and use are unavailable; keys may have been claimed without installing | Interest signal only | Medium-high |
| Paid founder offer | Live $39.99 Polar checkout handoff | 10 of 10 spots still visible | Checkout completion was not tested; counter reliability and abandoned checkouts are unknown | Checkout handoff exists; no completed sale is publicly evidenced | Medium |
| Organic search | Homepage and Reddit post visible for an exact-brand query | Absolute positions 6 and 7 | Labs found no domain keywords; product absent from two tested category results | Weak brand capture, not a category engine | High for captured date |
| Backlinks | 20 links from 13 domains in the summary | Indexed links | Detailed rows are spam, old domain artifacts, generic reports, or Locker Drop links | No credible email-product referral signal | High |
| Founder portfolio | Public maker portfolio | Establishes maker identity | No `inbox.locker` or Locker project link was found on the captured page | Background proof, not an observed route | Medium-high |
| Paid search | No relevant advertiser or creative result | None | Other identities, networks, markets, and dates remain possible | Not evidenced | Low |
| Product Hunt, HN, LinkedIn, X | No exact-domain result in narrow checks | None | Search coverage is incomplete | Not observed | Low |

## What Locker tried and changed

- A July 2025 Wayback capture shows the domain redirecting to a generic
  `/lander`, before the current email product.
- A search-indexed earlier page state led with “Email, with the cloud taken
  back out,” described an open-source MCP and approval-queue product, and
  requested one email notification when the app became installable.
- Locker published v0.1.0 and v0.2.0 on June 23, then v0.3.0 on June 24.
- The June 24 Reddit post offered feedback-oriented testers a free lifetime
  key and linked to the public product.
- The current page leads with a private on-device AI inbox, a direct download,
  five claimed free keys, and a staged lifetime-price offer.
- The current changelog labels v0.4.0 “Next release · in testing,” while the
  homepage already presents several overlapping notification, rule, reminder,
  and work-account capabilities as current.
- A future browser product is mentioned in the privacy policy but is not
  available and has a different planned privacy model.

The exact date of the earlier indexed page is unavailable. Search-title lag and
the current page's cache state are not proof of when or why the message
changed. See [history.md](./history.md).

## Evidence files

- [Landing page, metadata, message, instrumentation, and claim boundary](./landing-page.md)
- [Search traffic and live SERPs](./traffic.md)
- [Founder post, backlinks, and excluded Locker Drop links](./referrals.md)
- [Download, giveaway, purchase, and activation paths](./funnel.md)
- [Domain, offer, release, and positioning history](./history.md)
- [Tecotype experiments and release gates](./opportunities.md)
- [DataForSEO, GitHub API, HTTP, and browser request ledger](./requests.md)

## Implications for Tecotype

- **What appears to be working:** Locker has one concrete community response,
  five claimed giveaway keys, and a public download-before-payment path.
  Those observations show that a specific privacy proposition can earn a small
  amount of early interest. They do not establish source attribution,
  activation, retention, or revenue.
- **What appears weak, discontinued, or inconclusive:** Category search,
  credible referrals, paid acquisition, and public paid conversion are not
  evidenced. The earlier waitlist/MCP framing was replaced. The homepage and
  changelog disagree about what is currently available, which makes its
  feature-heavy pitch unsafe to treat as shipped proof.
- **What Tecotype should test now:** Use a small, disclosed research invitation
  around one product proof, either keyboard triage or “Find mail the way you
  remember it.” Record the message that earned the conversation. Do not offer
  public access while Tecotype's no-account first run, public site,
  signed/notarized updateable distribution, Gmail restricted API audit,
  safe compose/reply/send behavior, license and payment flow, and
  source-to-activation measurement remain unfinished or unverified.
- **What Tecotype should test after the release gate:** Let a tightly bounded
  cohort try a verified signed, notarized, updateable release before purchase,
  then measure source, installation, account connection, first sync, a
  message-matched first-value action, voluntary next-day return, day-seven
  use, and payment separately. Compare calm control with the concrete Better
  search demonstration.
- **What Tecotype should avoid:** Do not use limited lifetime spots or claimed
  keys as proof of demand. Do not count disk-image requests as users. Do not
  publish capabilities before the shipped build supports them. Do not say mail
  “never leaves the device,” because Tecotype still communicates with the
  user's mail provider.
- **Evidence strength and remaining unknowns:** The page, checkout handoff,
  legal terms, release metadata, GitHub-reported asset counters, Reddit
  thread, current SERPs, and backlink rows were directly observed. Actual
  visitors, acquisition source, unique installs, mailbox connections, first
  value, retained use, paid checkouts, revenue, and customer satisfaction
  remain unavailable.

Detailed experiment designs are in [opportunities.md](./opportunities.md).
