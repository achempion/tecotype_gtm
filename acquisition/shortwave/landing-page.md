# Shortwave landing-page evidence

Research date: **2026-07-17**

Primary URL: **https://www.shortwave.com/**

Market: **US-English public web**

## Inspection mode and boundary

The current public HTML, metadata, linked public website JavaScript, public
documentation, and rendered US-English homepage were inspected. The rendered
page confirmed the headline, section order, platform text, Pricing and Download
routes, repeated `Get started for free` controls, and the public script hosts.
No visible dialog or form appeared in that state. Responsive variants,
animation details, consent-gated behavior, regional variants, and post-login
screens remain unverified.

No Shortwave desktop or mobile client, PWA, installer, extension, app package,
or other client artifact was downloaded, opened, mounted, installed, executed,
or inspected. No CTA was clicked in the rendered pass. No form was submitted,
and no account, OAuth grant, trial, checkout, or payment flow was started.

## Current page

| Field | Observed value |
| --- | --- |
| Title | `Shortwave — Automate your email with AI` |
| Description | `Agentic AI that helps you organize, write, search, schedule, and more with just a prompt` |
| Canonical | `https://www.shortwave.com/` |
| Language | `en` |
| Public framework | Next.js static output; build ID observed as `HOfcPPcaJmFviyiwdJEzn` |
| Hero | “Automate your email with AI” |
| Supporting copy | “Save hours each day with the Shortwave Agent — organize, schedule, write and search with just a prompt” |
| Primary CTA | `Get started for free` → `https://app.shortwave.com/login` |
| Offer qualifier | “No credit card required” |
| Platform line | “Available on iOS, Android, Mac & Windows” |

These values are also present in the current
[public homepage response](https://www.shortwave.com/). The unauthenticated
[login response](https://app.shortwave.com/login) exposed only the Shortwave
brand and a JavaScript-required notice in this inspection. It did not expose a
usable form without executing the application, so the login or OAuth sequence
was not continued.

## Audience and positioning

| Question | Evidence | Assessment |
| --- | --- | --- |
| Who is it for? | “Ambitious teams,” business users, professionals with high email volume, and teams that coordinate external communication | **Observed** in homepage, pricing, billing, and team copy |
| What creates demand? | An overflowing inbox, repetitive organization and writing, interruption, difficult search, scheduling work, and unclear ownership | **Observed** |
| What is promised? | Save hours each day by asking an agent to organize, schedule, write, search, and connect other tools | **Observed first-party claim**; no independent time study was found |
| Why this product? | AI actions and filters, personalized writing, AI search, bundles, splits, delivery schedules, todos, keyboard operation, and team collaboration | **Observed** |
| Emotional angle | Ambition and productivity at the top of the page; control, focus, relief, and fewer interruptions in the inbox sections | **Inferred from repeated copy** |
| What supports it? | Customer quotations, named professional roles, company logos, product demonstrations, press excerpts, “thousands of companies,” and CASA Tier 2 | **Observed first-party proof**; customer status and compliance were not independently audited |
| What is the offer? | A no-card free entry point on the homepage; a 14-day trial and tiered paid plans on Pricing | **Observed** |
| What action is requested? | Start free, start a trial, inspect pricing, or move to the separate Tasklet automation product | **Observed** |

The original 2022 launch said Shortwave was redesigned so people could stay
“calm, focused, and in control.” The current hero gives the AI agent priority,
but the older emotional contract survives in delivery schedules, bundles,
notification controls, Do Not Disturb, and copy about attention. That mix is
close to Tecotype's intended equanimity in outcome, but not in mechanism:
Shortwave now leads with cloud AI and automation, while Tecotype's current
position is keyboard-first local operation and local search.

## Message architecture

The rendered page follows this sequence:

```text
AI automation outcome
→ no-card free CTA and cross-platform availability
→ company-logo proof
→ agent actions: organize, integrate, filter, write, search, schedule
→ sister-product automation
→ inbox control: splits, bundles, todos, delivery schedules, keyboard
→ team collaboration
→ testimonials and press
→ security, privacy, and long-tail features
→ repeated free CTA
```

The strongest aspect is breadth connected to one command model: “just ask.”
The weakness is message competition. Calm inbox control, an AI executive
assistant, team collaboration, and cross-application automation all compete
for attention on one long page.

## Public CTA and attribution behavior

The public `_app` website bundle records:

- `utm_medium`, `utm_source`, `utm_content`, `utm_campaign`, and `utm_term`;
- a first-touch/last-touch style attribution record with anonymous ID, page,
  and timestamps;
- `gclid` and `fbclid`;
- a Google Analytics event named `sign_into_app_clicked` for links to
  `app.shortwave.com`; and
- a corresponding X/Twitter conversion event when its tag is available.

This is evidence of source-continuity and conversion-event capability. It does
not show whether the login, activation, payment, or retention datasets join
correctly.

The homepage also links to Tasklet with visible UTM parameters:
`utm_source=shortwave`, `utm_medium=website`, and
`utm_campaign=nyt_feature`. That is a concrete cross-product acquisition path,
not evidence of how many Shortwave visitors adopt Tasklet.

## Publicly visible measurement technology

| Technology | Public identifier or behavior | What it supports | What it does not prove |
| --- | --- | --- | --- |
| Google Analytics | `G-EM5K59TV8Z` | Page and CTA-event measurement | Data quality, consent state, or downstream retention |
| X/Twitter Universal Website Tag | Pixel/config ID `obu4f`; CTA conversion event | X attribution or retargeting capability | Active spend or return |
| Meta Pixel | `2073634749747616`; `PageView` | Meta measurement or retargeting capability | Active spend or return |
| First-party attribution cookie | UTM fields, anonymous ID, page, and timestamps | Carrying acquisition context across page views | Correct source classification or durable account linkage |
| Click-ID cookie | `gclid` and `fbclid` handling | Paid-click continuity | Campaign efficiency |

The rendered page loaded scripts from `www.googletagmanager.com`,
`static.ads-twitter.com`, `connect.facebook.net`, and first-party
`www.shortwave.com`. No visible consent dialog appeared in the captured
US-English state. Server-side, geographically conditional, blocked, or
consent-gated systems may exist beyond this evidence.

## Offer and pricing

The current [pricing page](https://www.shortwave.com/pricing/) defaults to
business plans and says “Start your 14 day free trial.”

| Audience | Monthly plan shown or defined publicly | Annual-billing equivalent defined in public page code |
| --- | ---: | ---: |
| Individual | Free $0; Pro $18/month | Pro $14/month equivalent |
| Business | $30/seat/month | $24/seat/month equivalent |
| Premier | $45/seat/month | $36/seat/month equivalent |
| Max | $120/seat/month | $100/seat/month equivalent |

The individual tab values were verified in the pricing page's public
JavaScript, while the server-rendered page exposed the business tab. The
[billing guide](https://www.shortwave.com/docs/guides/billing/) says a paid
rate covers a person's linked email accounts, all team members use the same
plan, Stripe processes payments, and full refunds can be requested within 14
days of payment. These are current public terms, not a checkout test.

The Free plan makes the product broadly evaluable but includes a mandatory
`Sent with Shortwave` signature. Paid plans remove it. Higher tiers expand AI
models, quota, context, search history, filters, integrations, and
collaboration rather than merely removing an evaluation time limit.

## Provider and platform boundaries

Shortwave publicly claims availability on web, iOS, Android, Mac, and Windows.
The [Spark migration guide](https://www.shortwave.com/docs/migrations/migrating-from-spark-mail/)
also states that platform matrix. This research records the claim only; no
client or distribution artifact was obtained or tested.

Provider support is narrower than the platform line suggests. The current
[other-provider guide](https://www.shortwave.com/docs/how-tos/microsoft-outlook-exchange-other-sign-in-support/)
says:

- a Gmail or Google Workspace account is required to sign in;
- Yahoo, iCloud, Fastmail, Zoho, and providers with forwarding plus SMTP can
  be bridged through Gmail;
- Outlook.com can forward inbound mail but cannot send from that address
  through this workaround; and
- Microsoft 365 and Exchange are not supported.

This is a meaningful acquisition constraint and a potential Tecotype
differentiator after release because Tecotype supports Gmail and generic IMAP.
It must not be framed as a current public-distribution advantage while
Tecotype's Mac release remains gated and Windows remains unshipped.

## Privacy tension visible in the offer

The page promotes inbound tracker blocking, image proxying, and privacy mode.
It also promotes outbound read statuses, recent-open feeds, link tracking, and
team visibility into recipients' reads. Both claims are first-party and
simultaneously present.

For Tecotype, the lesson is not to choose stronger copy for one side. It is to
avoid hidden recipient surveillance altogether. Privacy expectations extend to
people who never chose the product.

## Landing-page conclusion

Shortwave has a mature, instrumented public surface with a low-friction free
entry, clear AI-agent promise, extensive proof, comparison/migration paths,
cross-platform claims, and an intentional Tasklet cross-sell. The page also
reveals two strategic tensions: broad AI/business scope versus the simpler
calm-control story, and privacy protection for the user versus tracking of
recipients. Public website evidence cannot show signup completion, inbox
connection, first value, retained use, or paid conversion.
