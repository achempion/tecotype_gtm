# Shortwave public acquisition funnel

Research date: **2026-07-17**

## Inspection boundary

This report inspected public pages, public website scripts, public
documentation, and the unauthenticated login response. The rendered homepage
CTA was not clicked. No account was created, no Google authorization was
started, no inbox was connected, no trial or payment was initiated, and no
client artifact was downloaded or installed.

Post-login steps are therefore documented from current public guides and
clearly separated from directly observed unauthenticated behavior.

## Current public path

```text
Search / press / Product Hunt / referral / store / directory
→ shortwave.com homepage, content, migration, or pricing page
→ “Get started for free” or “Start free trial”
→ app.shortwave.com/login
→ Google/Gmail authorization (documented, not executed)
→ Gmail settings and recent-history sync
→ Free plan and Shortwave Method
→ AI organization / first useful triage
→ Pro or per-seat Business/Premier/Max
→ signature removal, more AI/history, collaboration, team invites
→ Tasklet automation cross-sell
```

The public evidence does not connect source to retained payment.

## Stage-by-stage evidence

| Stage | Public evidence | Status | Unknown |
| --- | --- | --- | --- |
| Discovery | Brand/category rankings, Google Inbox replacement page, HN and Product Hunt launches, press, stores, directories, backlink and ad archives | **Observed** | Qualified visits and source mix |
| Landing | Current AI-agent hero, proof, features, no-card free CTA, cross-platform line | **Observed** | Page conversion |
| Source continuity | UTM, `gclid`, `fbclid`, anonymous attribution record, and app-link conversion events | **Observed capability** | Whether events join to activation and retention |
| Login | CTA routes to `https://app.shortwave.com/login`; public response requires JavaScript | **Observed** | Exact current Google button copy, abandonment, errors |
| Authorization | Current docs say Gmail or Google Workspace is required | **Documented** | OAuth completion and trust objections |
| Import | Gmail migration guide says labels/settings sync and last 90 days import on sign-in | **Documented** | Time to usable inbox, failure rate, actual history by plan |
| Activation | Shortwave Method teaches single-pass triage into non-actionable, under-two-minute, and larger actionable work | **Documented** | Which action predicts retention |
| Free-to-paid | Free plan plus Pro; 14-day trials for business tiers; paid plans expand AI/history/filter/team capability | **Observed/documented** | Trial eligibility, conversion, plan mix, renewal |
| Payment | Billing guide says Stripe, team-level plans, monthly default, annual option, and 14-day refund requests | **Documented** | Checkout friction, failed payment, refund rate |
| Expansion | Teammate invites, shared threads, assignees, shared labels/prompts, higher tiers, Tasklet | **Observed/documented** | Seat expansion and net retention |

## Offer ladder

The current homepage offers a no-card free start. The pricing page offers a
14-day free trial and exposes two audiences:

| Plan | Public monthly price | Acquisition role |
| --- | ---: | --- |
| Free | $0 | Low-friction evaluation; basic AI and limited history; mandatory signature |
| Pro | $18/month | Individual power use; longer search history and richer AI |
| Business | $30/seat/month | AI integrations, more history/usage, filters, tracking, snippets, and team use |
| Premier | $45/seat/month | Advanced intelligence, more context/usage/history |
| Max | $120/seat/month | Highest intelligence, context, usage, and filter limits |

Annual billing lowers the monthly equivalent. Exact public prices and evidence
are in [landing-page.md](./landing-page.md). Price is not the only gate:
provider compatibility excludes direct Microsoft 365/Exchange use and requires
a Gmail bridge for supported non-Gmail providers.

## Activation mechanism: a taught operating method

The
[Shortwave Method](https://www.shortwave.com/docs/guides/method/) is a
productized behavior-change layer:

1. triage every visible item before deeper work;
2. mark non-actionable mail done, delete it, or snooze it;
3. complete tasks under two minutes immediately;
4. turn larger work into stars or todos;
5. use bundles to reduce repeated decisions; and
6. prioritize remaining work after the inbox is organized.

This is more valuable than a feature tour because it teaches why the controls
exist. It can also create pressure: the guide says users “simply cannot do
their best work” with a messy inbox and recommends completing triage first.
Tecotype should learn from the workflow clarity without adopting shame,
compulsion, or irreversible mass action.

The [Gmail migration guide](https://www.shortwave.com/docs/migrations/migrating-from-gmail/)
reduces switching risk by explaining how labels, stars, signatures, aliases,
filters, settings, shortcuts, snooze, scheduled mail, and history behave. This
continuity is likely important to activation, but “likely” remains an
inference.

## Free-product growth mechanics

The free plan is simultaneously:

- an evaluation path with no card required from the homepage;
- an acquisition surface because sent mail carries Shortwave branding;
- a route to team invitations and shared work; and
- a feeder into more AI, more history, and higher limits.

The mandatory signature is a measurable growth tactic but a poor fit for
Tecotype's calm-control contract. A paid professional should control what is
added to their messages.

## Team and Tasklet expansion

The [team guide](https://www.shortwave.com/docs/guides/team/) recommends one
team for an organization, sends invitation emails, centralizes billing, and
supports roles. The public pricing page says all team members use the same plan.
That creates straightforward seat expansion but may also increase the cost of
moving one advanced user up a tier.

Tasklet creates a second expansion dimension:

```text
Shortwave handles interactive inbox work
→ visitor asks for automatic or scheduled action
→ Tasklet handles triggered background automation
→ direct integration writes drafts, todos, and comments back to Shortwave
```

The homepage carries a source-tagged Tasklet link. Public evidence does not
show attach rate, cross-product retention, or combined economics.

## Historical versus current funnel

### 2022 launch

```text
Firebase reputation / HN / Product Hunt / press
→ Gmail-specific landing page
→ sign in with Gmail
→ free product or $9/month fuller history
→ bundles, todos, channels, and Inbox Organized
```

### 2026 public funnel

```text
AI category / comparisons / content / launches / ads / stores
→ AI-agent and business-team homepage
→ no-card Free or 14-day business trial
→ Gmail authorization and sync
→ productized triage plus AI
→ individual or per-seat intelligence tiers
→ collaboration and Tasklet automation
```

The change widens monetization and campaign surface area, but the Gmail
dependency remains.

## Measurement gaps

The public funnel cannot answer:

- qualified session volume by source;
- login-page view or Google authorization completion;
- sync completion, import time, and errors;
- first organization/search/write action;
- voluntary return on day one, seven, or thirty;
- Free-to-Pro or trial-to-paid conversion;
- team invite acceptance and seat expansion;
- churn, refund, support burden, CAC, LTV, or profitability; or
- the effect of the mandatory signature on acquisition and trust.

The site's tracking stack makes many measurements possible. Capability is not
the result.

## Funnel conclusion

Shortwave's most transferable funnel idea is continuity from a recognizable
problem to a taught workflow and switching guide. Its free/no-card entry,
signature, team loops, and repeated launches amplify that core. Tecotype
should first prove a safe first-value workflow in an invited Mac cohort, then
encode the repeated guidance. It should not imitate freemium, recipient
tracking, or automated branding before retention and trust are established.
