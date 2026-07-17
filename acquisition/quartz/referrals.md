# Launch amplification, referrals, and backlinks

Quartz's link graph is a launch-period snapshot. The raw total includes
repeated links, launch mirrors, AI-tool directories, newsletters, and owned
datarockets pages. It is useful for reconstructing visibility, not for counting
users.

## Raw link-index snapshot

DataForSEO reported on 2026-07-17:

| Metric | Result |
| --- | ---: |
| Backlinks | 216 |
| Referring domains | 24 |
| Referring main domains | 24 |
| Referring pages | 185 |
| Nofollow referring pages | 132 |
| Broken backlinks | 0 |
| First backlink seen | 2026-05-23 |

The summary endpoint reported 24 referring domains. The detail endpoint
reported 25 available records but returned 24 items under its one-per-domain
setting. The endpoints therefore differ by one record. A large share of the
raw pages are repeated or low-authority directory surfaces. A backlink is not
a session, download, connected account, or activated user.

## Reconstructed launch sequence

| Date / period | Source | What is observed | What it supports | What it does not support |
| --- | --- | --- | --- | --- |
| May 15 | [The Shift AI newsletter](https://theshiftai.beehiiv.com/p/openai-brings-coding-to-mobile) | Quartz appears in an AI-tools roundup before the first archived landing page | Early newsletter visibility | Sponsorship, clicks, or waitlist conversion |
| May 23 | [Archived BetaList listing](https://web.archive.org/web/20260523204739/https://betalist.com/startups/quartz) and [private-beta page](https://web.archive.org/web/20260523204711/https://www.quartzmail.ai/?ref=betalist) | Featured placement led through `ref=betalist` to an email waitlist | A concrete prelaunch discovery path | Visits, signup count, or activation |
| May 28–June 2 | [Indie Hackers](https://www.indiehackers.com/post/did-ai-make-inbox-overload-worse-from-10-to-100-unwanted-emails-a-day-1fcc12664f) and [HackerNoon](https://hackernoon.com/did-ai-make-inbox-overload-worse-from-10-to-100-unwanted-emails-a-day) | Founder-authored problem article linked Quartz and was syndicated | Founder-led content distribution | Indie Hackers showed only two likes and one comment; referrals unknown |
| May–June | Founder LinkedIn activity | Founder described the problem, closed beta, privacy, focus, and personal drafting | Owned-audience warming and product narrative | Qualified reach or activated users |
| June 15 | [Fazier](https://fazier.com/launches/quartz-2) | Source-tagged launch page, 23 upvotes, and a founder feedback request | Deliberate pre-Product Hunt launch seeding | Downstream action |
| June 17 | [Product Hunt](https://www.producthunt.com/products/quartz-3) | Public launch, maker thread, #4 Product of the Day, source-tagged website link | Concentrated visible launch attention | Source-to-install or source-to-retention |
| June 17 | Maker and [datarockets LinkedIn](https://www.linkedin.com/company/datarockets) posts plus a [founder support post on Reddit](https://www.reddit.com/r/ProductHunters/comments/1u88s9o/just_launched_quartz_currently_5_of_the_day/) | Multiple posts asked people to try, vote, comment, and share, and reported rank progress | Deliberate owned-network amplification | Reddit post had only four votes and one congratulatory comment; incremental effect is unknown |
| June onward | Launch trackers and AI directories | ProductCool, Just Launched, AIToolly, Toolworthy, AI Tool Archive, and similar pages link to Quartz | Broad directory placement and syndication | Intent, traffic quality, or activation |
| June onward | Newsletters and articles | [Andrew Bolis](https://andrewbolis.kit.com/posts/claude-for-small-business-google-smart-device-updates-alexa-shopping-ai-assistant), MaxiApple, and other roundups included Quartz | Additional audience exposure | Paid/earned classification or downstream results |
| Current | [datarockets case study](https://datarockets.com/case-studies/quartz-mail-ai/) | Detailed build story, #4 result, 269 launch-time upvotes, and “hundreds” in daily use | Owned proof asset and a first-party adoption claim | Independent verification or Product Hunt attribution |

The archived [BetaList listing](https://web.archive.org/web/20260523204739/https://betalist.com/startups/quartz)
and tagged destination establish the path. [BetaList's own
support page](https://betalist.com/support) says its featured-site redirects add
`ref=betalist`. The path still reveals no impressions, visits, or signups.

## Product Hunt

The public Product Hunt page ties several pieces together:

- The product promise matches the site: focus, Mac, local AI, and Gmail.
- The launch team is the three datarockets makers.
- The maker introduction explains the same problem and says the beta is free.
- The discussion answers setup and product questions in detail.
- The result is visibly #4 Product of the Day for June 17, 2026.
- The captured overview showed 278 points and 401 followers.
- Two reviews existed; both were positive, but both also requested basic
  workflow improvements.

The makers answered questions about the model download, which they described
as roughly 4 GB, plus onboarding preferences, categorization feedback, local
drafting, and missing custom categories. The referenced model file is
4,977,171,584 bytes. These answers exposed setup details, costs, and product
limitations that the landing page did not state. Their effect on visitor
confidence or conversion is unknown.

The [maker case
study](https://datarockets.com/case-studies/quartz-mail-ai/) says Product Hunt
put Quartz in front of thousands and that hundreds now use it daily. These
statements make Product Hunt more credible than a link-only channel, but they
still leave a missing causal step:

```text
Product Hunt exposure
→ visit
→ download
→ Gmail connection
→ useful inbox
→ daily use
```

No public source reports the rate at any arrow.

## Founder and agency amplification

Quartz was not launched from an empty account:

- Pavel Demeshchik's public LinkedIn surface showed roughly 8,000 followers in
  the captured search result.
- datarockets' company page showed roughly 1,970 followers.
- The company and individual makers posted several times during the launch:
  initial announcement, an invitation to try, live rank progress, and a
  follow-up result.
- A founder later said the launch had no marketing budget, marketing team, or
  popular hunter. This is a first-party statement; the public evidence does
  show substantial maker and company amplification.

The repeatable mechanism is not “launch without an audience.” It is:

```text
Several weeks of maker narrative
→ concentrated launch-day posts from multiple related accounts
→ maker participation on Product Hunt
→ direct product access
```

Tecotype should treat the maker audience and Product Hunt listing as separate
sources in its own measurement.

## Community boundary

- No relevant Hacker News submission or discussion was found by exact product
  and domain searches. This is “not found,” not proof of absence.
- The founder's Product Hunters Reddit post was launch support rather than a
  product discussion and had little visible engagement.
- A separate Product Hunt launch roundup on Reddit also had minimal
  interaction.
- Indie Hackers preserved a founder-authored article, not independent community
  validation.
- Product Hunt is the only community-shaped surface with material visible
  attention. Its two reviews contain use feedback, but the sample is tiny.

## Parameterized destinations

Examples in the backlink index include:

| Referrer | Destination shape |
| --- | --- |
| Product Hunt | `?ref=producthunt` |
| BetaList | `?ref=betalist` |
| Fazier | `?ref=fazier` |
| ProductCool | `?ref=productcool` |
| Just Launched | `utm_source=justlaunched&utm_medium=referral...` |
| AIToolly | `utm_source=aitoolly.com&utm_medium=referral` |
| Toolworthy | Source, medium, campaign, and CTA-content parameters |
| AI newsletters | Newsletter-domain source and campaign parameters on some links |

These parameters make source analysis possible in principle. They may have been
added by the referring platform rather than Quartz, and they do not prove that
Quartz preserved or used them after the download.

## What appears productive or weak

**Strongest evidence:** Product Hunt produced an observed #4 daily result
during coordinated maker promotion and sits next to a first-party daily-use
claim. The maker posts' incremental effect and the relationship between the
launch and later use are unknown.

**Plausible prelaunch support:** A newsletter placement, a BetaList-attributed
waitlist listing, founder articles/posts, and Fazier preceded the launch. The
public record does not expose waitlist size or invitation outcomes.

**Presence only:** AI directories and launch trackers created many links, often
with useful source parameters. No activation is visible.

**Weak as a durable system:** Quartz still lacks non-brand search visibility,
a content library, or observable community discussion with sustained user
depth. Public evidence does not assign that outcome to the link burst.

## Repeatable candidates for Tecotype

1. Warm up a launch with a small number of accurate, concrete product proofs.
2. Coordinate maker posts and a launch platform only after first-run activation
   works.
3. Preserve each source through the download and first app launch.
4. Submit to a small, relevant directory/newsletter batch, then stop sources
   that produce no activated users.
5. Treat maker replies as part of the acquisition surface: answer concrete
   privacy, setup, provider, and product-limit questions plainly.

Do not use Quartz's 216 backlinks as a target. The useful unit is activated and
retained users per source, not referring pages.
