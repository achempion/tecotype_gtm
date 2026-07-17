# Spark Mail public funnel

Captured: **2026-07-17**

Research boundary: This is a map of public pages, rendered public DOM, public
store metadata, help and policy text, and destination `href` values. No Spark
client, installer, package, extension, or binary was downloaded or opened. No
account, mailbox authorization, trial, form, demo, store action, purchase, or
checkout was attempted. The `/download` route was deliberately not opened
because Spark uses it for platform-specific client delivery.

## Current public path

The primary individual path is:

```text
search / ad / store / referral / brand / Readdle portfolio
→ article, homepage, pricing page, or store listing
→ Free download or Buy now
→ /download, app store, or Stripe route
→ client acquisition and install
→ Spark Account and existing mail-provider connection
→ Free use or seven-day Plus/Pro trial
→ monthly/annual subscription through supported payment channel
→ cross-platform use, retention, and renewal unknown
```

A team path is also visible:

```text
team search / case study / collaboration feature / team pricing
→ Plus, Pro, Enterprise, or Book a demo
→ form, checkout, or client setup
→ Spark team / shared inbox / collaboration
→ activation, expansion, and retention unknown
```

The public site exposes the beginning and decision layer. Distribution,
provider authorization, mailbox readiness, product use, subscription
entitlement, and retention move across native clients, stores, email
providers, Spark services, and payment processors.

## Entry surfaces

### Broad informational search

Spark's largest modeled search entries are CC/BCC explainers and email-writing
templates. Their route is likely:

```text
generic email question
→ owned answer or template
→ internal Spark framing
→ Free download or pricing
```

The intent gap is large. A person learning what CC means may have no desire to
replace an email client. Public data does not reveal CTA exposure, click rate,
eligible platforms, provider fit, installation, or activation.

### Brand search

The sampled `spark mail` result page placed the homepage first and also showed
iOS, Google Play, Reddit, YouTube, Spark Desktop's Mac listing, and Trustpilot.
This creates a rich evaluation surface and multiple exits from Spark's owned
website measurement.

### Paid Google advertising

Google's public archive returned 10 Spark creatives, including text, image,
and video records active in 2026. The landing destinations and post-click
performance were not inspected through ad interaction. Archive presence does
not disclose delivery, spend, audience, or conversion.

### App stores

iOS, Android, macOS, and Windows stores can acquire without an owned-site
visit. Ratings, privacy labels, release recency, requirements, screenshots,
and reviews influence the decision at the point of distribution.

### Product Hunt, press, and Setapp

Spark has 12 Product Hunt launches, a decade of editorial coverage, and a
current Setapp bundle listing. These sources may route to the site, store, or
partner entitlement. Public attribution parameters prove measurement intent,
not channel results.

### Team consideration

Case studies, collaboration pages, team pricing, Enterprise, and Book a demo
create a second funnel. The form was not submitted, and no public source
exposes lead qualification, sales cycle, conversion, seat expansion, or churn.

## Website decision layer

The homepage asks a visitor to believe one simple lead promise:

> Smart. Focused. Email.

It substantiates that promise with a wide product:

- Priority, Pin, Group by Sender, Done, and Set Aside;
- Smart Inbox, Home Screen, newsletter and notification grouping;
- Send Later and Reminders;
- Spark +AI writing, Assistant, summaries, and translation;
- calendar and Meeting Notes;
- Gmail, IMAP, iCloud, Exchange, Outlook, Yahoo, and Google support;
- integrations;
- shared drafts, comments, delegation, and team collaboration;
- cross-platform use.

Decision proof includes:

- the first-party 19.5 million cumulative download claim;
- a 4.8 / 154K aggregate rating claim;
- Apple Editors' Choice;
- publisher logos;
- a named user quote;
- product screenshots and workflow explanations;
- Free, Plus, Pro, and Enterprise pricing;
- security and privacy language.

This reduces feature and vendor uncertainty. It creates complexity around plan
fit, AI data handling, two Mac products, current-versus-SOON features, and the
meaning of Spark's broad privacy sentence.

## Offer and checkout routes

### Free

The Free plan publicly includes:

- Smart Inbox;
- unlimited email accounts;
- unified email;
- Smart Notifications;
- essential productivity features;
- calendar.

The detailed comparison includes features such as search, scheduled send, and
snooze. Free is a continuing product tier rather than only a temporary trial.

### Plus

Plus is:

- $10 per user per month when billed monthly;
- $99 per user per year when billed annually;
- displayed as $8.25/month on the annual option;
- positioned around advanced productivity, Spark +AI, AI Assistant,
  40 AI Meeting Notes, integrations, templates, and essential team
  collaboration.

### Pro

Pro is:

- $20 per user per month when billed monthly;
- $199 per user per year when billed annually;
- displayed as $16.58/month on the annual option;
- positioned around unlimited AI Meeting Notes, read statuses, advanced team
  collaboration, HubSpot, and Spark CLI triage access.

Workflows, Auto-Labels, and Auto-Drafts are marked **SOON**. They are not
current conversion proof.

### Enterprise

Enterprise uses a contact route and publicly adds security/administrative
controls, customer success, and coaching. The price and sales process are not
public.

### Trial and entitlement

Spark's current public help says:

- Plus or Pro has a seven-day trial when a person subscribes directly in the
  app;
- the subscription works across platforms through the same Spark Account;
- support can sometimes extend or change the trial start;
- AI is disabled by default;
- AI use is quota-limited, with additional credits purchasable;
- existing Premium customers keep the legacy plan.

The public language does not establish that every Free download automatically
begins a trial. This report therefore maps download, Free use, and trial as
distinct possible states.

The pricing page exposed Stripe URLs for monthly and annual Plus and Pro. Only
the link destinations were recorded:

- `type=individuals-plus-plans-month`;
- `type=individuals-plus-plans-year`;
- `type=individuals-pro-plans-month`;
- `type=individuals-pro-plans-year`.

No checkout page was opened.

## Funnel strengths

### Useful product before payment

Unlimited accounts and core organization in Free allow evaluation without an
immediate billing decision. A seven-day paid trial exists when advanced plans
are started.

### Real billing cadences

Monthly and annual subscriptions both exist. Spark displays annual savings and
annualized monthly equivalents, but unlike an annual-only offer, it provides a
true monthly option.

### Cross-platform entitlement

The same Spark Account carries the subscription across supported platforms.
Mobile, Mac, Windows, and partner discovery can reinforce each other.

### Public proof at multiple stages

Release recency, large mobile review counts, long-running press, Product Hunt,
Setapp, cases, and Readdle's product portfolio reduce vendor-risk uncertainty.

### Explicit web measurement

The site implements source persistence, page-view events, CTA-specific events,
plan/cadence checkout fields, consent mode, Amplitude, and experimentation
code. This is a coherent web decision-layer measurement system.

## Funnel friction and risk

### Installer handoff

The primary Free CTA uses `/download`, which is intended to begin
platform-specific client delivery. The page does not keep a researcher inside
a purely informational web step. A prospective user may still need to resolve
OS requirements, signing trust, installation, and updates before value.

### Provider authorization and server data flows

A working inbox requires a Spark Account and access to an existing mail
provider. OAuth tokens or encrypted credentials can be stored. Push, Send
Later, shared mail, read statuses, collaboration, Meeting Notes, AI, and
related features introduce server or contracted-provider processing.

The public funnel does not disclose authorization failure, first-sync time,
mailbox completeness, or provider-specific quality.

### Two Mac products

Spark Classic and Spark Desktop remain maintained. Spark explains migration
and says the products can run side by side, but a person must understand:

- which app to install;
- which behavior transfers;
- which features differ;
- whether a review refers to Classic or Desktop;
- how long maintenance-only support will continue.

This is both acquisition friction and retention risk.

### Product and plan accumulation

Free, legacy Premium, Plus, Pro, Enterprise, personal, team, AI quotas,
add-on credits, multiple payment channels, and future Pro automation create a
large decision surface. The main prices are clear; the complete entitlement
model is not simple.

### Annual savings presentation

The annual page visually compares $99 with a $120 monthly-billing total and
$199 with a $240 total. That comparison is valid, but the crossed-out
annual-looking values require interpretation. Billing cadence should be stated
next to every amount.

### Public privacy-language mismatch

The homepage says data is “never shared with third parties,” while the policy
describes service providers, AI providers, integrations, payment processors,
analytics, and lawful disclosure. An evaluating person must reconcile a broad
assurance with a more accurate detailed account.

### Reliability and migration counterevidence

Large mobile and Setapp ratings are positive proof. Selected current desktop
discussion also reports freezing, resource use, sync/send problems, and
preference for Classic. These reports are not representative, but a poor first
desktop experience can erase the value of every upstream channel.

### Future features inside current Pro framing

Workflows, Auto-Labels, and Auto-Drafts are visibly labeled SOON. Clear labels
are better than implied availability, but planned capability should not be
included in current value or retention measurement.

## Measurement observed

The website exposed:

- one-year first-party source persistence;
- source, medium, initial source, initial medium, and campaign values;
- Google Tag Manager;
- consent-mode defaults with analytics/ad storage denied before choice;
- page-view event `ev_page_view`;
- `ev_free_download` / `Free Download Clicked`;
- `ev_buy_now` / `Buy Now Clicked`;
- `ev_checkout_event` / `Checkout Clicked`;
- product, plan, billing cadence, and element-position fields;
- Amplitude;
- Tailor AI experimentation;
- Meta script presence in the rendered page;
- a visible cookie choice with Accept all and Manage cookies.

This supports a web chain:

```text
source
→ page
→ free or paid intent
→ selected plan and cadence
→ checkout handoff
```

The public site does not reveal:

- consent distribution;
- event transmission or deduplication;
- CTA counts;
- store/client attribution continuity;
- trial activation;
- provider connection;
- first value;
- retention;
- payment completion;
- experiment results.

## A defensible email-client funnel

Downloads are cumulative and especially weak as a success metric for a
multi-platform client. A minimum chain is:

| Stage | Example event | Why it matters |
| --- | --- | --- |
| Qualified discovery | Source plus platform/provider intent | Separates generic email information from product demand |
| Distribution | Verified signed direct/store acquisition | Distinguishes CTA interest from product acquisition |
| Setup | Provider authorization completed | Identifies the first hard product gate |
| Mailbox readiness | Sync/index reaches a defined usable threshold | Rejects empty or incomplete “activation” |
| First value | Meaningful prioritization, keyboard, organization, or retrieval action | Connects the promise to use |
| Retention | Meaningful use after a defined interval | Rejects one-session novelty |
| Commercial | Retained Free, trial state, paid conversion, renewal, churn | Connects use to economics |
| Quality | Crash, send/sync failure, support, deletion, refund | Prevents growth from hiding harm |

No public Spark source exposes complete rates across these stages.

## Implications for Tecotype

Tecotype should define a similarly complete chain before release while
collecting the smallest privacy-preserving event set.

For macOS, the public acquisition test must wait until the website,
signed/notarized Apple Silicon build, Gmail restricted-API requirements,
onboarding, provider setup, compose/send safety, licensing/payment, and update
path are ready. Activation should require mailbox readiness plus a meaningful
keyboard or local-search action, not a download.

For Windows, event names and page research can be designed now, but no
available-download path should be published until signed NSIS/Store
distribution, a direct fallback, updates, and platform-specific smoke tests
ship.

Tecotype's decided Individual price is **€149/year or €15/month**. It should
show both real cadences plainly and avoid using future capabilities to justify
current payment. A small paid acquisition test can follow only after
source-to-retention measurement works.
