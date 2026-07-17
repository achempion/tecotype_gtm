# Canary Mail public funnel

Captured: **2026-07-17**

Research boundary: This is a map of public pages, public store metadata, policies, and help content. No client or installer artifact was downloaded or opened; no account, mailbox, trial, form, store action, purchase, or checkout was attempted.

## Current public path

The observable acquisition path is:

```text
search / store / referral / brand
→ article, homepage, or app-store listing
→ Download or Start Free Trial
→ /downloads or platform store
→ client download and install
→ existing email-account connection
→ seven-day all-feature trial
→ Free downgrade or in-app Growth / Pro+ purchase
→ activation, retention, and renewal unknown
```

There are several important handoffs:

1. an owned website page to `/downloads`;
2. `/downloads` to Apple, Google, or Microsoft distribution;
3. store acquisition to a native client;
4. client setup to an external mail-provider authorization;
5. trial to a usable free plan or in-app purchase.

The public website can measure the first handoff. Store operators, the native clients, OAuth providers, app analytics, and purchase systems control later parts. A complete attribution model therefore requires a durable source identifier and privacy-safe event reconciliation across surfaces.

## Entry surfaces

### Broad informational search

Canary’s largest modeled entry pages address CC/BCC, free business email, Yahoo setup, Outlook passwords, unsending mail, read receipts, and archived Gmail messages. These topics maximize reachable demand but often precede any intention to replace an email client.

Likely public route:

```text
problem query
→ answer
→ internal feature/category framing
→ download CTA
```

Unknowns include CTA visibility, click-through, platform fit, store completion, and whether the reader ever intended to switch.

### Product and brand search

The homepage ranks first for `canary mail` and appeared in the sampled top ten for `ai email client`. Branded results also include platform stores, a YouTube review, Setapp’s comparison, and Wikipedia. This gives an evaluating person multiple forms of proof and multiple exits from Canary’s owned measurement.

### App stores

The iOS, macOS, Android, and Windows listings can acquire directly without a website visit. Public ratings, screenshots, release recency, privacy labels, reviews, and in-app-purchase metadata reduce or increase trust at the point of install.

### Referrals and partners

Product Hunt, press, security guides, comparisons, historical Setapp distribution, and portfolio cross-promotion can route directly to the site or stores. The Product Hunt and Dove links show UTM use, but public event counts are absent.

## Website decision layer

The homepage asks visitors to accept a broad bundle:

- AI Copilot;
- integrated calendar and scheduling;
- multiple-account unified inbox;
- read receipts and power-user controls;
- PGP and SecureSend/HIPAA;
- cross-platform access.

It supports the decision with:

- a “1,000,000+ users” first-party claim;
- a large organization-logo row;
- a republished editorial quote;
- current platform links;
- security and privacy language;
- Free/Growth/Pro+ pricing.

This reduces feature uncertainty but creates a different risk: a person may not know which single job Canary is best at or how each capability handles data.

## Offer and trial

The [pricing page](https://canarymail.io/pricing) describes:

### Free

- $0 forever;
- core inbox;
- unlimited email accounts;
- unified inbox;
- Read Receipts Lite;
- snooze and pin;
- templates;
- Inbox Zero;
- basic customization.

### Growth

- $36 per year, displayed as $3 per month;
- AI Copilot;
- full read receipts;
- send later;
- calendar and scheduling;
- inbox cleaner;
- integrations;
- advanced customization.

### Pro+

- $100 per year, displayed as $10 per month;
- PGP;
- SecureSend/HIPAA;
- phishing and ransomware protection;
- impersonation and misdirection protection;
- priority support.

The current public terms say:

- the trial lasts seven days;
- all features are available;
- no card is required;
- there is no automatic billing;
- the account downgrades to Free after the trial;
- purchases and upgrades occur in-app;
- paid plans can be used on up to five devices, while Free is limited to two;
- annual and lifetime purchase options exist for Growth and Pro+.

The inspected public HTML did not reliably expose the current lifetime prices, so they are not stated here. Apple metadata exposes multiple historical and current-looking lifetime SKU names, but store metadata alone does not establish which offer every person sees.

## Funnel strengths

### Low billing anxiety

No card and no auto-billing eliminate the fear of an unwanted renewal. A functional Free plan means the trial ends in continued product access instead of an immediate hard stop.

### Multi-platform continuity

One paid plan can span up to five supported devices. This can make the value proposition stronger for people with mixed device ecosystems and can allow a mobile or desktop listing to reinforce the other.

### Frequent public release proof

Current release notes and store metadata show ongoing updates. That matters in a client whose acquisition promise depends on continued compatibility with providers and operating systems.

### Feature-based expansion

The pricing ladder maps visible product problems to upgrades:

```text
core email
→ productivity and AI
→ regulated/security-sensitive use
```

This is easy to understand even if the practical distinctions and value realization require product use.

## Funnel friction and risk

### Trial clock starts too early

The FAQ says the trial starts when the app is downloaded. A person may lose trial time to installation, provider authorization, sync, indexing, migration, or troubleshooting before reaching value. A fairer activation point is successful account connection or a meaningful in-product milestone.

### Monthly-looking annual price

Growth and Pro+ are visually presented as `$3/month` and `$10/month`, but the purchase is billed at `$36/year` and `$100/year`. The page explains this, yet the framing creates avoidable pricing interpretation work.

### Platform handoff fragments attribution

A website CTA leaves for a store; some people discover the store directly. Without deliberate linking and post-install source recovery, owned analytics will overcount clicks and under-explain activation.

### Provider authorization is a hidden gate

The product supports Gmail, Outlook, iCloud, IMAP, and Exchange, but public marketing cannot show the actual success rate, consent friction, sync time, or mailbox completeness for each provider and platform.

### Privacy detail is displaced

The homepage uses broad on-device and security language, while the privacy policy explains server-mediated push, Cloud Sync, hosted Copilot processing, analytics, and mobile attribution. An evaluating person must reconcile those surfaces.

### Quality varies by platform

Public iOS and Android scores differ materially, and public release notes repeatedly address sync, search, crashes, and reliability. Cross-platform breadth increases acquisition reach and the surface area for a poor first experience.

### Licensing and legacy SKU complexity

Annual, lifetime, Free, Growth, Pro+, store purchases, device limits, restore paths, and legacy in-app SKU names can create support work even when the headline ladder looks simple.

## Measurement observed

The public homepage HTML exposed:

- GA4 identifier `G-6NRDJKDL7C`;
- custom events named `download`, `hipaa`, and `canary_for_support`;
- HubSpot;
- Ahrefs Web Analytics;
- a first-party chatbot loader;
- UTM-tagged Dove cross-promotion.

The privacy policy names:

- Firebase Analytics / Google Analytics;
- Crashlytics;
- Intercom;
- AppsFlyer for mobile installation attribution.

This supports an inference that Canary has the components to measure web actions, app behavior, crashes, and mobile installs. It does not show:

- event definitions;
- consent configuration;
- source persistence;
- cross-device identity logic;
- attribution windows;
- funnel rates;
- experiment results;
- revenue.

## A defensible funnel measurement model

For any email client, raw downloads are an especially weak success metric. A useful minimum chain is:

| Stage | Example event | Why it matters |
| --- | --- | --- |
| Qualified discovery | page or store view with source and platform intent | Separates broad information demand from product demand |
| Distribution | signed download or verified store acquisition | Distinguishes CTA clicks from actual acquisition |
| Setup | provider authorization completed | Identifies the first hard gate |
| Mailbox readiness | initial sync/index reaches a defined usable threshold | Prevents false activation on empty or incomplete states |
| First value | a meaningful workflow completed | Connects acquisition promise to use |
| Retention | meaningful use after a defined interval | Rejects one-session novelty |
| Commercial | trial-to-paid, retained Free, lifetime, annual, or churn state | Connects behavior to economics |

The public record exposes none of Canary’s rates at these stages.

## Implications for Tecotype

Tecotype should define the event chain before a public release, but only emit the smallest privacy-preserving data needed.

For macOS, the post-release experiment should begin only after the public website, signed/notarized distribution, Gmail audit requirements, provider onboarding, update path, licensing/payment, and safe compose/reply flow are ready. The activation event should be successful Gmail or IMAP readiness plus a meaningful keyboard or local-search action—not download.

For Windows, Tecotype should design the same source and activation vocabulary now, but it must not expose an “available” download funnel until the signed Windows distribution and update path actually ship. Mac success cannot stand in for Windows readiness.

Tecotype’s decided €149/year or €15/month price should be presented in the billing cadence actually offered. A free tier, trial length, or lifetime option should not be copied from Canary without evidence that it supports Tecotype’s support load, privacy model, and unit economics.
