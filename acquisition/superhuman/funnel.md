# Superhuman Mail public funnel

Research date: **2026-07-17**

Scope: **public pages and unauthenticated metadata only**

## Historical funnel

Superhuman's early system deliberately combined acquisition and activation:

```text
Product Hunt / press / founder network / “Sent from Superhuman”
→ invitation waitlist
→ referral priority
→ qualification survey
→ invitation
→ $30 per month
→ mandatory 30-minute onboarding
→ workflow transition
→ ongoing use and referrals
```

The waitlist moved from 60,000 Product Hunt preview subscribers to 180,000 in
2019 and more than 275,000 in February 2020. Those are interest counts, not
users. The $30 monthly price and mandatory guided setup filtered for
high-expectation professionals and gave Superhuman a chance to teach a
keyboard-first workflow.

The former growth lead's
[retrospective](https://review.firstround.com/superhuman-onboarding-playbook/)
says more than 65% of new customers fully transitioned after human onboarding,
nearly twice the activation of self-serve, and generated twice as many
referrals. The author explicitly notes selection bias. No public cohort links
those results to a specific discovery source or later retention.

## Current public route

The current public path is structurally different:

```text
Search / ad / referral / partner / review / direct
→ Mail landing or campaign page
→ Get Started
→ /signup with source and referral parameters preserved
→ Google or Microsoft identity/provider eligibility
→ pricing or checkout route
→ Mail onboarding/download route
→ productized interactive onboarding
→ subscription, referral, or team expansion
```

The visible path was inspected only through public responses and scripts. No
signup field was entered, identity provider selected, account created,
mailbox authorized, app or extension obtained, trial started, or checkout
opened.

## Step-by-step observations

| Step | Public evidence | Status |
| --- | --- | --- |
| Landing | `/products/mail` promises four hours saved each week and repeatedly asks visitors to `Get Started` | **Observed** |
| Attribution | CTA code preserves UTM, click IDs, Impact, Dub, promo, and referral fields; emits link-click telemetry | **Observed capability** |
| Experiment | LaunchDarkly can redirect qualifying non-paid Mail visitors to `/mail` while preserving query/referrer | **Observed capability** |
| Signup | `/signup` offers Google or Microsoft paths; public logic checks provider, team/singleton, and security eligibility | **Observed in public code** |
| Unsupported provider | Public strings say Superhuman will be in touch when the provider is supported | **Observed** |
| Plan choice | Default code path leads to Mail pricing; public route constants also support checkout and onboarding/download | **Observed in public code** |
| Onboarding | First Round says the general path became fully self-serve after three years of productization; white-glove time moved to highest-value and B2B prospects | **First-party retrospective** |
| Current assistance | Starter has group coaching/public webinars; Business has private group coaching/private webinars; Enterprise lists priority 1:1 coaching and dedicated support | **Observed on pricing page** |
| Activation | Public retrospective reports self-serve activation moving from 40% to 50% after focusing onboarding on core Inbox Zero actions | **First-party historical result** |
| Payment and retention | No public source provides current completion, conversion, retention, CAC, or LTV | **Unobservable** |

## Offer and pricing

Superhuman currently exposes both Mail-only and suite paths.

### Mail a la carte

The [Mail pricing page](https://superhuman.com/pricing) shows annual-equivalent
prices:

- Starter: **$25 per user per month**;
- Business: **$33 per user per month**; and
- Enterprise: talk to sales.

The [Mail pricing help article](https://help.superhuman.com/hc/en-us/articles/46005733349517-Pricing-Plans)
states the billing options explicitly:

- Starter: **$30 monthly or $300 annually**;
- Business: **$40 monthly or $396 annually**; and
- Enterprise: sales-assisted.

The two pages are consistent: $25 and $33 are monthly equivalents of the
annual prices.

### Superhuman suite

The [suite plans page](https://superhuman.com/plans) offers Free and Pro
without Mail, Business at **$33 per member per month billed annually** or
**$40 monthly** with Mail, and custom Enterprise. The suite's claims of more
than 40 million people and 50,000 teams describe the combined platform, not
Mail customers.

The [suite help article](https://help.superhuman.com/hc/en-us/articles/46185486670733-Superhuman-Suite)
says new customers and teams, plus individual Mail subscribers, can access the
suite. Existing Mail-team migration remained incomplete at capture. It also
confirms new customers can still buy Mail alone.

### Trial ambiguity

The `/email` acquisition page says `Get Started for Free`, and public signup
code contains a conditional feature for offering a free trial without a
credit card. The principal Mail and suite pricing pages do not present one
universal Mail trial. A trial should therefore be described as conditional or
campaign-dependent, not as a guaranteed current offer.

## How activation was productized

Superhuman's onboarding retrospective says the team transferred years of
human instruction into a controlled, interactive flow:

- focusing the first workflow on `e` and `h` increased use of those commands
  50% and raised self-serve activation from 40% to 50%;
- moving important setup from a tucked-away checklist to full-screen required
  steps raised completion from 30% to over 98%;
- key-feature opt-in rose from 45% to nearly 80%; and
- 57% opted into “Get Me To Zero,” which the article says archived close to
  one billion messages.

These are first-party product results, not independently reproduced figures.
They nevertheless explain the current model: teach the new workflow through
safe action, preserve human help where account value justifies it, and make
the general funnel self-serve.

## Conversion and trust friction

The current funnel has several unavoidable decision points:

- granting Google or Microsoft access to a primary mailbox;
- learning a keyboard-centered workflow;
- choosing between Mail-only and suite pricing;
- understanding which AI features, security controls, and collaboration
  features belong to each plan;
- obtaining the web extension or desktop/mobile client; and
- trusting an email product with message and calendar data.

Public offer differences—`Get Started`, `Get Started for Free`, Mail-only
pricing, suite pricing, and transitional account rules—can create additional
choice friction. The extensive source-preservation code suggests Superhuman
can diagnose those paths internally, but no public conversion data is
available.

## Funnel conclusion

Historically, Superhuman made premium human onboarding the bridge between
attention and a difficult behavior change. It later encoded that knowledge in
self-serve onboarding and kept high-touch help for more valuable accounts.
That sequencing is more credible than treating the waitlist or referral count
as the engine by itself.

For Tecotype, guided activation is worth testing only after a safe, release-
ready path exists. It should be a learning and transition aid, not a gate that
manufactures exclusivity or hides missing core functionality.
