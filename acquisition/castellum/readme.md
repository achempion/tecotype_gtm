# Castellum acquisition report

Research date: **2026-07-17**

Scope: **Castellum, the Apple Silicon email client at
`castellummail.com`; unrelated companies and products named Castellum are
excluded**

Market: **Google US-English, desktop where applicable**

Castellum is a very early, founder-built Mac email client. Its first public
release appeared on June 29, 2026, and the latest public release is
[v0.2.2](https://github.com/joanmarcriera/castellum-releases/releases/tag/v0.2.2),
published the next day. The current homepage offers that build directly and
free during early access.

The report treats public release notes and manifests as evidence of the
released boundary. Homepage feature and privacy statements remain first-party
claims where they cannot be verified without installing the client, connecting
a mailbox, or running local AI. None of those actions was performed.

## Executive answer

No repeatable Castellum acquisition channel is publicly evidenced yet.

The strongest observable path is simply:

```text
existing awareness from an unknown source
→ focused manager/private-AI homepage
→ direct GitHub disk-image link
→ install, provider connection, first value, and return unknown
```

The landing page is unusually specific for such a young product. It is for
managers who run projects from email, leads with a “command HQ” rather than a
minimal inbox, and uses local AI, keyboard operation, and local storage as
proof. That message is clear. Public distribution is not.

At capture:

- GitHub recorded **24 disk-image asset requests** across five releases,
  including **8** for the stable v0.2.2 asset.
- The first build’s own release history says it crashed at launch; v0.1.1 fixed
  it 48 minutes later.
- The v0.2.1 release note says Gmail sign-in was still limited to
  developer-approved test users, despite the homepage saying “Gmail in one
  click.”
- DataForSEO modeled only one US keyword, `castellum ai`, at absolute position
  39 and **0.672 ETV**. A same-day live check did not show the email product in
  the returned results, which were dominated by the unrelated
  `castellum.ai` compliance company.
- The email product was absent from the tested live exact/descriptive-brand
  and category result sets.
- The backlink index contained only two obvious nofollow SEO-spam pages.
- Exact-domain Content Analysis returned no mentions, and the narrow Google
  advertising checks returned no results.

The public release repository has zero stars, forks, and open issues. Narrow
searches found no product-specific Hacker News, Product Hunt, Reddit, LinkedIn
post, X, press, review, or partnership result. Those are point-in-time negative
observations, not proof that private, deleted, unindexed, or future activity
does not exist.

The most defensible conclusion is:

> Castellum has built a clear direct-download offer, not an evidenced
> acquisition system. Its launch history also shows why a public download is
> not a useful funnel until launch reliability and provider authorization are
> ready.

## Headline evidence

| Signal | Observed result | Boundary |
| --- | ---: | --- |
| First public release | 2026-06-29 | GitHub release metadata |
| Current public release | v0.2.2, 2026-06-30 | No later binary release found |
| Disk-image requests across v0.1.0–v0.2.2 | 24 | Asset requests, not unique users or installs |
| Stable v0.2.2 disk-image requests | 8 | Dynamic GitHub counter |
| Update-manifest requests across releases | 4 | Can include app checks, the maker, testing, or research |
| GitHub stars / forks / open issues | 0 / 0 / 0 | Repository activity, not product use |
| Labs organic ranked keywords | 1 | Current modeled US snapshot |
| Modeled organic ETV | 0.672 | Estimate, not analytics |
| Qualified live brand/category visibility found | 0 tested results | Six narrow query snapshots |
| Backlinks / referring domains | 2 / 2 | Both nofollow SEO spam from one IP |
| Exact-domain content mentions | 0 returned | Provider coverage is incomplete |
| Google advertiser / creative results | 0 / 0 | Narrow archive coverage |
| Current offer | Free during early access | No public checkout |
| DataForSEO spend | **$0.128504** | 18 task IDs, including failures and one corrective duplicate |

## Discovery paths

The only directly observable path is:

```text
unknown awareness
→ castellummail.com
→ internal “Download for Mac” anchor
→ untagged GitHub release asset
→ install and first launch unknown
```

Public release notes imply two post-download branches:

```text
download
→ sample-data exploration, connect email, or skip for now
→ product comprehension and return unknown
```

```text
download
→ Gmail sign-in
→ approved-test-user gate as of v0.2.1
→ mailbox connection and activation unknown
```

or:

```text
download
→ guided IMAP/SMTP setup
→ provider/app-password configuration
→ sync, first useful action, and retained use unknown
```

The current public offer has no payment step:

```text
free early-access build
→ future paid plan mentioned
→ timing, price, license transition, and conversion unknown
```

## Channel scorecard

| Channel | Observed activity | Downstream signal | Contrary evidence or limit | Verdict | Confidence |
| --- | --- | --- | --- | --- | --- |
| Direct homepage/download | Clear manager/private-AI page linked to a public build | 24 captured disk-image requests | No source tags, unique installs, account connections, or return data | Distribution surface exists; acquisition source unknown | High |
| GitHub releases | Five releases, checksums, release notes, updater manifests | 8 requests for latest stable disk image | Zero stars, forks, and issues; counters include repeats and internal work | Useful release ledger, not a community channel | High |
| Organic search | One modeled keyword and one ranked root page | 0.672 modeled ETV | Same-day live checks did not surface the product; major name collisions | Negligible and unqualified visibility | High |
| Backlinks | Two indexed links | Two referring domains | Both are nofollow SEO-spam pages, rank 0, from one IP | No credible referral path | High |
| Founder public presence | Public portfolio, GitHub profile, and LinkedIn profile exist | Establishes maker identity | No Castellum promotion or referral was found in narrow public checks | Potential future founder channel, not observed acquisition | Medium |
| Product Hunt, HN, Reddit, LinkedIn posts, X, press | No exact-domain/product result found | None | Search coverage and indexing are incomplete | Not observed | Low |
| Paid search | No advertiser or creative result | None | Other identities, markets, networks, and dates remain possible | Not evidenced | Low |
| Partnerships / affiliates | None found | None | Private or future relationships remain possible | Not evidenced | Low |
| Email capture | No waitlist, newsletter, or lead form on the current page | None | Direct policy contact is not an acquisition form | Not present | High |

## What Castellum tried and changed

- **June 29:** the release repository, v0.1.0, and first public landing page
  appeared. The page already used the current fortress, manager, local-AI,
  keyboard, and privacy frame.
- **48 minutes later:** v0.1.1 fixed a packaged native-module mismatch that
  caused the installed v0.1.0 app to crash at launch.
- **June 30:** the homepage added a product screenshot, a three-step Ollama
  setup, FAQ, and “free during early access” language.
- **June 30:** v0.2.0 added automatic updates, optional sample data, and guided
  local-AI setup.
- **June 30:** v0.2.1 fixed Gmail’s token exchange but disclosed that the
  Google consent screen remained in testing mode.
- **June 30:** v0.2.2 added guided configuration for 31 providers and
  Thunderbird autoconfig fallback.
- **July 17:** privacy, terms, and Google Limited-Use pages were added. The
  public commit says they support Google OAuth verification and introduces
  policy language for optional cloud AI and future licensing.

Wayback returned no successful page captures. The public Git history preserves
the observable changes but cannot show why they were made or how they
performed.

## Evidence files

- [Landing page, metadata, message, rendered hierarchy, and claim boundary](./landing-page.md)
- [Search snapshot, keyword ambiguity, and live SERPs](./traffic.md)
- [Backlinks, public profiles, and narrow community checks](./referrals.md)
- [Download, onboarding, provider, AI, feedback, and future-payment funnel](./funnel.md)
- [Release, message, and legal-page history](./history.md)
- [Staged Tecotype experiments and release gate](./opportunities.md)
- [DataForSEO, GitHub, HTTP, browser, and archive request ledger](./requests.md)

## Implications for Tecotype

- **What appears to be working:** Castellum communicates one recognizable
  audience and a coherent mechanism. Its direct download, release notes,
  checksums, and update manifests make the offer inspectable. Eight current
  disk-image requests show that the latest asset has been requested, but not
  that the page or message converted a qualified user.
- **What appears weak, discontinued, or inconclusive:** No credible discovery
  source, category search, referral, mention, ad, activation, retention, or
  payment signal is public. The first build failed at launch, and the public
  Gmail path remained approval-gated in the latest explicit OAuth note.
- **What Tecotype should test now:** Test whether one implemented job—keyboard
  triage, calm Gmail/IMAP control, or “Find mail the way you remember
  it”—earns qualified research conversations. Prepare a release-truth matrix
  that separates implemented, release-gated, and future work.
- **What Tecotype should test after the release gate:** Use a small,
  source-tagged invited cohort and measure signed install, first run, provider
  connection, usable sync, message-matched first value, voluntary return,
  day-seven use, and payment separately.
- **What Tecotype should avoid:** Do not open a public download before
  first-run/no-account onboarding, the public site, licensing/payment, Gmail
  restricted-API review, signed/notarized updateable distribution, safe-send
  behavior, and privacy-compatible source-to-activation measurement work end
  to end. Do not say mail “never leaves the Mac”; it still communicates with
  the user’s provider.
- **Evidence strength and remaining unknowns:** The rendered page, public HTML,
  policy pages, Git history, GitHub API metadata, release notes, current SERPs,
  backlink rows, founder profiles, and archive index were directly inspected.
  The client was not downloaded, installed, or launched. Mailbox connection,
  feature behavior, signing/notarization acceptance, unique installs,
  acquisition source, first value, retained use, future checkout, revenue, and
  customer satisfaction remain unknown.

Detailed experiment designs are in [opportunities.md](./opportunities.md).
