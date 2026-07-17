# MonoMail acquisition research

Research date: **2026-07-17**

Scope: **the Android project at `monomail.millosaurs.me` and
`shrivatsav-org/monomail`; the unrelated commercial `monomail.co` is excluded**

Market: **Google US-English, desktop where applicable**

## Executive answer

MonoMail's strongest observed acquisition pattern is a compact founder-led
community launch:

```text
founder or community Reddit post
→ GitHub repository or product page
→ public release page
→ release-asset download
→ account setup and useful email action unobservable
```

The public [repository](https://github.com/shrivatsav-org/monomail) was created
on June 11, 2026. By the July 17 snapshot it had **144 stars, 10 forks, and 30
releases**. GitHub's public release metadata reported **3,215 cumulative asset
downloads**. These are download events across versions, not unique people,
installs, active users, retained users, or customers.

Reddit supplied the clearest public discovery:

- a June 14 founder
  [update](https://www.reddit.com/r/HowToMen/comments/1u5s3fn/app_update_monomail_a_minimalistic_email_client/)
  had 39 votes in the indexed snapshot;
- a June 17 community
  [post](https://www.reddit.com/r/foss/comments/1u83c2v/monomail_an_open_source_gmail_alternative/)
  had 177 votes; and
- the founder repeated similar launch copy across several subreddits on June
  20, with much smaller visible responses.

Those discussions also exposed a distribution constraint. People reported
that Google sign-in was blocked, and the founder said a 100-person Google
OAuth test cap was full. The public landing page distinguishes a GitHub build
without preconfigured Gmail sign-in or push notifications from a fuller Play
Store build in closed testing. The public Play Store URL returned a
not-found page during research. No test was joined and no app or release
asset was opened.

The project does not show a subscription funnel. It is free and open source,
with UPI and Ko-fi support links. A founder post offered a personalized signed
build for `$5` if the user supplied cloud credentials, but no completed
purchase was observed. Donations, one-off build support, repository stars,
and release downloads do not demonstrate activation-to-paid distribution.

The most relevant conclusion for Tecotype is:

> A narrow visual promise and a genuine community conversation can create
> fast early discovery, but every public source needs its own attributable
> path through desktop activation and payment before it becomes a channel.

## Headline evidence

| Signal | Observed result | Boundary |
| --- | ---: | --- |
| GitHub repository | 144 stars; 10 forks; 6 open issues/PRs reported by API | Attention and project activity, not users |
| Release cadence | 30 releases from June 13 to July 15, 2026 | Public metadata; no asset was opened |
| Release-asset downloads | 3,215 cumulative events | Not deduplicated people, installs, or active users |
| Largest single release total | `v1.3.2`: 499 downloads | One asset count, still not unique users |
| Highest-vote observed Reddit post | 177 votes in `r/foss` | Community attention, not attributable activation |
| Google test access | Founder said 100/100 places were filled | First-party comment; cohort quality unobservable |
| Owned-domain search | 0 modeled keywords and 0 modeled ETV | DataForSEO US-English snapshot |
| Brand SERP | Reddit and GitHub visible; owned site absent from top ten | Brand discovery exists outside the owned domain |
| Category SERP | MonoMail absent from top ten | No observed category-search discovery |
| Backlink index | 4 links from 3 domains | All detailed domains were automated code indexes |
| Public price | Free/open source; donation links | No recurring paid offer observed |
| DataForSEO spend | `$0.088144` | 7 successful one-object tasks; below `$2` per competitor |

## Observed acquisition paths

```text
Reddit discovery
→ project site or GitHub
→ latest-release link
→ release asset
→ install, account connection, activation, and retention unobservable
```

```text
project site
→ public Play Store link
→ not-found response in the research snapshot
→ closed-test access, install, and activation unobservable
```

```text
GitHub or product-page trust
→ Discord
→ support, feedback, or contributor relationship
→ downstream activation and payment unobservable
```

```text
product-page appreciation
→ UPI or Ko-fi
→ donation
```

The last path is creator support rather than a paid email-client subscription.
None of the paths exposes a permanent source identifier connected to product
activation and payment.

## What appears transferable

- A precise visual identity makes the product easy to describe in a community
  post.
- A public repository and release history provide permanent evaluation and
  trust surfaces.
- Founder replies turned launch comments into objection research about access,
  security, and account setup.
- Community posts can produce more visible response than a new owned domain
  with no search footprint.
- Frequent public updates give interested people reasons to return.

The transfer to Tecotype is marketing-only. Tecotype should use one canonical
desktop page, one source-tagged link per community, public proof and changelog
pages, and an activation-to-paid measurement path. It should not imitate
Android distribution, side-loaded packages, or closed-test mechanics.

## Dossier

- [Landing page](./landing-page.md)
- [Traffic and search](./traffic.md)
- [Referrals and community](./referrals.md)
- [Offer and funnel](./funnel.md)
- [History](./history.md)
- [Tecotype opportunities](./opportunities.md)
- [Request ledger](./requests.md)

## Research boundary

Research used public webpages, server-delivered HTML and headers, public
GitHub API metadata, public search extracts, and DataForSEO. The in-app
browser was unavailable, so no rendered-DOM pass was possible.

No repository was cloned. No source checkout, client, application, installer,
package, binary, release asset, or app payload was downloaded, opened,
mounted, executed, installed, or inspected. No Google test was joined. No
account, mailbox authorization, trial, Discord, form, checkout, UPI, Ko-fi,
or payment flow was entered.

## Implications for Tecotype

- **What appears to be working:** founder and community Reddit posts created visible attention around a narrowly described open-source project, while GitHub supplied permanent proof, 144 stars, 30 releases, and 3,215 cumulative release-asset download events; no public source connects that attention to retained use or payment.
- **What appears weak, discontinued, or inconclusive:** the owned domain has no modeled search footprint, the category query does not surface MonoMail, repeated cross-posts quickly lost response, the public store route was unavailable, and release downloads cannot establish users or activation.
- **What Tecotype should test:** give each high-fit desktop-workflow community a distinct, useful demonstration and source-tagged canonical link, then compare qualified visits, desktop activation, payment, and renewal by source.
- **What Tecotype should avoid:** copying posts across communities, counting votes, stars, downloads, test capacity, Discord joins, or donations as distribution, or sending people through an unmeasured external handoff.
- **Evidence strength and remaining unknowns:** public landing-page, Reddit, repository, release, search, and backlink evidence is strong for early discovery and friction; unique visitors, installs, connected accounts, first value, retention, donation completion, recurring revenue, and source-level activation-to-paid remain unobservable.
