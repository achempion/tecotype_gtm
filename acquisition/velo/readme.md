# Velo acquisition report

Research date: **2026-07-17**

Market: **Google US-English; desktop/Windows for live search snapshots**

Scope: **Velo’s public landing page, repository, releases, launch discussions, referral surfaces, and observable acquisition path**

## Executive answer

Velo’s strongest observable acquisition mechanism was not search or a conventional email-product launch. It was a provocative founder story:

> In one LinkedIn launch post, a developer said he built a free, open-source, local-first desktop email client with Claude in roughly two days, then showed the work to developer communities.

That story generated attention quickly. The principal Reddit launch was captured at **+246 votes** and passed **200 comments**; a public LinkedIn launch post showed **68 reactions and 12 comments**; a third-party YouTube Short appeared in the current branded Google results with **38.7K+ views**; and the repository had **664 stars and 112 forks** on the research date. These are public attention signals, not users.

The downstream acquisition system is much weaker than the launch attention:

- all prominent landing-page download CTAs send people to a generic GitHub releases page;
- Velo has almost no observable category-search footprint in the US snapshot;
- the public site exposes no recognizable product analytics or source tagging;
- Gmail users must create their own Google Cloud OAuth client before connecting;
- the latest macOS release workflow explicitly uploaded an unsigned build;
- the configured updater URL for the latest release returned `404`;
- there is no Velo account, trial, license key, checkout, or observed revenue path; the current product is offered at $0 under Apache 2.0;
- no public source connects a post, view, star, release-asset request, or backlink to a working mailbox, first value, retention, or contribution.

The launch therefore proves that an unusual build story can earn developer attention. It does **not** prove that Velo acquired or retained a corresponding audience of email users.

## Headline evidence

| Signal | Observed result | Evidence boundary |
| --- | ---: | --- |
| Principal Reddit launch | +246 votes; thread passed 200 comments | Public thread/search capture; attention and controversy, not use |
| Public LinkedIn founder post | 68 reactions; 12 comments | Public capture; no click or activation data |
| Show HN, 2026-02-21 | 7 points; 0 comments | Public item; much smaller than Reddit |
| YouTube Short in current branded SERP | 38.7K+ views | Google result breadcrumb for third-party video; YouTube analytics unavailable |
| GitHub repository | 664 stars; 112 forks | Current public counters; stars and forks are not installs |
| Current release asset requests | 1,088 across nine assets | GitHub counters; repeat requests, bots, and failed installs are possible |
| All release asset requests | 2,725 across 270 assets | Cumulative dynamic snapshot; not unique people |
| Current domain ranked keywords | 2 | Third-party US estimate |
| Current modeled organic ETV | 2.98 | DataForSEO estimate, not visits |
| Current paid ranked keywords | 0 | Current Labs snapshot only |
| Google advertising lookups | No search results | Narrow archive coverage; not proof of no historical advertising |
| Domain backlinks / referring domains | 13 / 8 | Small third-party index; known launch pages were omitted |
| Repository-URL backlinks / referring domains | 15 / 11 | Links to one URL only; known social links were omitted |
| Latest public release | `velo-v0.4.21`, 2026-02-27 | Public GitHub release |
| Latest macOS build path | Unsigned | Exact workflow run skipped all signed/notarized steps |
| Configured updater-manifest URL | `404` | Public metadata-only request on 2026-07-17 |

## What appears to have worked

### First-party observed

- The founder centered the build process in the launch posts.
- The site repeatedly pairs “open source” and “free forever” with keyboard use, local storage, and AI breadth.
- A public repository supplied inspectable code, screenshots, releases, and issue history.
- The project published rapid releases, and the founder replied in launch discussions.
- The website repeats one strong phrase: **“The email client you’d build for yourself.”**

### Third-party observed

- Reddit produced the clearest visible discussion burst.
- LinkedIn extended the founder story into the founder’s professional network.
- A YouTube Short and several small software publications created durable branded search results.
- Community and package surfaces linked directly to the repository, including an AUR package and a Brave community discussion.

### Inference

The open-source developer story likely explains more of the repository attention than the email-product promise does. The strongest public reactions concern AI-built software, code quality, signing, OAuth setup, and feature velocity—not a repeated, high-value inbox job.

### Unknown

- landing-page visits and CTA rate;
- unique downloads or successful installs;
- platform mix;
- Gmail or IMAP account-connection completion;
- successful first sync;
- time to first useful action;
- daily or weekly active use;
- retention, contributions, or support burden by source.

## Why the public numbers do not form a funnel

```text
post view or vote
≠ site visit
≠ GitHub star
≠ release-page visit
≠ asset request
≠ successful signed install
≠ mailbox connection
≠ successful sync
≠ first value
≠ retained use
```

GitHub’s `download_count` is an asset-request counter. A person can request several installers or retry one asset; automation can also request assets. The figures have no source, uniqueness, installation, activation, or retention dimension.

## The strategic lesson for Tecotype

Velo demonstrates a useful attention mechanism and a caution:

1. A specific technical story can make a young product discussable.
2. If the story is more provocative than the user problem, discussion can select for debate rather than qualified adoption.
3. A source-visible product can accumulate durable proof surfaces without building measurable acquisition.
4. Setup, signing, updates, and truthful privacy language are acquisition work, not post-launch details.

Tecotype should borrow public technical proof and founder credibility, not “AI built this,” feature-count spectacle, absolute privacy claims, free/open-source economics, or votes-as-users reporting. The release gate and staged tests are in [opportunities.md](opportunities.md).

## Evidence standards

This report uses four labels:

- **First-party:** Velo’s site, repository, manifests, workflows, releases, and founder posts.
- **Observed:** a page, counter, response, or public metadata value directly inspected on the research date.
- **Third-party:** search indexes, publications, package pages, and community counters.
- **Inference:** an interpretation that is plausible but not directly measured.

“Unknown” is used where the public record cannot support a claim. Planned or source-present behavior is not presented as validated product behavior.

## Files

- [Landing page](landing-page.md)
- [Search traffic](traffic.md)
- [Referrals, communities, and backlinks](referrals.md)
- [Public funnel](funnel.md)
- [History](history.md)
- [Tecotype experiments](opportunities.md)
- [Request and cost ledger](requests.md)

## Research boundary

No Velo binary was downloaded, installed, or launched. No account was created, mailbox connected, Google Cloud project configured, OAuth flow started, form submitted, trial started, or purchase made. Public HTML, metadata, source, manifests, workflow logs, release metadata, archives, search results, and third-party pages were inspected. The paid DataForSEO run cost **$0.167272**, below the **$0.25** cap; exact tasks and bodies are in [requests.md](requests.md).
