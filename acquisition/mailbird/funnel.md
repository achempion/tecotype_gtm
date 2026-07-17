# Mailbird acquisition funnel

Research date: **2026-07-17**

This is a reconstruction from public pages, scripts, support documentation,
search results, and App Store metadata. No installer or application artifact
was downloaded, installed, mounted, opened, inspected, or executed. No account,
mailbox, trial, form, or checkout was used.

## Executive finding

Mailbird has several low-friction entry routes and unusually rich website
attribution. The observable funnel stops at the handoff:

```text
source
→ landing page
→ free, store, purchase, or business CTA
→ public handoff
→ install and product behavior unknown
```

The site can likely distinguish many campaigns and first/last touches. Public
evidence cannot show whether the identifier continues through first launch,
mailbox connection, sync, first value, return, and payment.

## Funnel map

| Stage | Public evidence | Conversion cue | What is not public |
| --- | --- | --- | --- |
| Awareness | Search, press, referrals, partners, affiliates, stores, ads, blog, localization | Repeated category and platform message | Reach by source; incrementality |
| Landing | Homepage, provider guides, comparison pages, partner pages, pricing, business page | Publication logos, “millions” claims, benefits, discounts | First-party sessions; CTA rate |
| Evaluation | Free plan; one account; store/direct platform routes | “Get Mailbird Free”; no sales call for individuals | Handoff success; installer starts; store conversion |
| First run | Public support describes account setup and license activation | Server autodetection and import are claimed | Launch success; auth; account connection |
| Activation | Unified inbox, search, triage, integrations, sending | Product features and onboarding copy | Completed sync; first useful action |
| Upgrade | Annual Premium, Pay Once, add-ons, in-app purchases | Discount anchors, guarantee, recent-sale widgets | Checkout starts; payment; refund; tax/fee net |
| Business | Team-of-ten-plus lead form and distributor | Dedicated point of contact; bulk discounts | Qualified leads; close rate; seat count |
| Retention | Updates, support, current Mac version history, account portal | Ongoing features and critical fixes | Active cohorts; return; churn; renewal |
| Referral | Invite rewards, BOGO gift, affiliate/partner tracking | Free or lifetime entitlement | Invite rate; referred activation; referral CAC |

## Individual evaluation path

The current [homepage](https://www.getmailbird.com/) and [pricing page](https://www.getmailbird.com/pricing/)
put **Get Mailbird Free** near the primary message.

Mailbird's current [free-plan support article](https://support.getmailbird.com/hc/en-us/articles/360026807893-Is-Mailbird-free)
describes:

- one account per device;
- one user;
- one device;
- basic email access; and
- knowledge-base rather than direct email support.

The free plan is positioned for trial or simple, occasional use. Advanced
features, additional accounts, integrations, and direct support move the user
toward Premium.

That creates a plausible path:

```text
organic, ad, referral, review, or store discovery
→ one-account free evaluation
→ connect a real provider
→ discover multi-account or advanced-feature need
→ Premium upgrade
```

Only the first two steps are visible publicly. It is not known how many users
successfully authenticate, complete sync, send safely, return, or encounter an
upgrade boundary.

## Desktop and mobile routing

Public page code supports campaign- and platform-aware routing:

- Windows can route to current direct distribution, an alpha branch, or the
  Microsoft Store;
- Mac can route directly or to the Mac App Store; and
- a mobile visitor can enter an email address to receive a desktop link.

The mobile email form uses reCAPTCHA Enterprise and posts the email to a
first-party-configured webhook. It was not submitted.

The routing system gives Mailbird flexibility to test store versus direct
distribution or channel-specific experiences. It also creates state-management
risk: dormant page fragments still say Mac is coming even though current
distribution is live.

## Public Mac distribution

The current [US Mac App Store listing](https://apps.apple.com/us/app/mailbird-the-email-app/id6749447444?mt=12)
independently establishes:

| Field | Observed value |
| --- | --- |
| Product | Mailbird – The Email App |
| Seller | Mailbird, Inc. |
| Category | Productivity |
| Offer | Free with in-app purchases |
| Current version | 1.30.2 |
| Current release date shown | July 9 |
| Size | 303.2 MB |
| Minimum OS | macOS 14.0 |
| Annual in-app purchase | $34.49 |
| One-time in-app purchase | $159 |
| Aggregate rating | Too few US ratings/reviews to display an overview |

The listing's version history shows frequent releases and fixes across sync,
search, startup, rendering, crashes, Exchange, contacts, onboarding, and
interface behavior. The latest release adds a calendar and Wingman AI. This
establishes active Mac maintenance; it is not a reliability or retention
measurement.

The store's developer-supplied privacy disclosure says contact info,
identifiers, usage data, and diagnostics may be collected without being linked
to identity for marketing, analytics, or app functionality. Apple explicitly
notes that it has not verified the disclosure.

Mailbird's website says Mac requires Ventura or later, while the current US App
Store listing requires macOS 14.0 or later. Distribution route and current
build can therefore affect the practical minimum. This report uses the store
requirement for the store build and does not assume parity.

## Platform and provider boundaries

The current [pricing FAQ](https://www.getmailbird.com/pricing/) states:

- Mailbird 3.0 Premium licensing works on Windows and Mac;
- one Premium license can be used on up to three devices;
- Windows supports POP3, but connecting a POP3 account on Mac is not currently
  supported;
- Mac website requirements start at Ventura; and
- there is no current iPhone, iPad, or Android client, although mobile is on the
  future roadmap.

The [mobile support article](https://support.getmailbird.com/hc/en-us/articles/360014806554-Mailbird-for-Mobile-Android-iOS)
also says there is no current iOS or Android version.

These platform boundaries matter to funnel qualification. A mobile visitor or
Mac POP3 user may be attracted by the broad multi-account promise but cannot
complete the same product path.

## Paid paths

### Annual Premium

The website presents **$4.03 per user/month billed annually**, discounted from
$5.75. It adds:

- unlimited email accounts;
- advanced and integration features;
- direct email support; and
- a cross-platform entitlement.

The actual billing total, regional tax, and promotion can vary. The report did
not enter checkout.

### Pay Once

The website presents **$99.75 per user**, discounted from $399, and currently
offers an additional free Premium license.

The offer separates:

- permission to keep using the purchased product/version; and
- **Lifetime Updates**, currently shown as a separate $69 one-time add-on for
  future features and major versions.

Mailbird's [Lifetime Updates article](https://support.getmailbird.com/hc/en-us/articles/15354532511255-Why-am-I-being-charged-for-Lifetime-Updates)
explains that update charging has varied by purchase era. Current clarity at
the point of sale is essential because earlier customers have publicly
described different expectations.

### Partner add-on

The pricing page also offers Leave Me Alone lifetime access for $59. This can
increase order value and borrow another inbox-control product's value
proposition. Attachment rate and partner economics are private.

### Guarantee

All plans are presented with a 14-day money-back guarantee. The public page
does not expose claims, approval rate, refund time, or net retention after the
window.

### License activation and account portal

Mailbird's [activation article](https://support.getmailbird.com/hc/en-us/articles/220108027-Activating-Mailbird-License)
says a buyer receives a license key by email and activates it in application
settings.

The [MyMailbird portal article](https://support.getmailbird.com/hc/en-us/articles/39121847435543-MyMailbird-Mailbird-s-Customer-Portal)
describes license, device, product/version, renewal, order, and upgrade
management. This is useful retention infrastructure; no portal was accessed.

## Business funnel

The [business page](https://www.getmailbird.com/mailbird-business/) offers an
individual free CTA and a separate path for teams of ten or more:

```text
business feature proof
→ first name, last name, company, work email, country, phone, and seats
→ dedicated point of contact
→ qualification and sale unknown
```

Pricing FAQ describes automatic volume discounts:

| Quantity | Published additional discount |
| --- | ---: |
| 2–10 | 5% |
| 11–25 | 10% |
| 26–50 | 15% |
| 51–100 | 20% |
| 101+ | 25% |

The business page also lists an official India/UAE distributor. No lead form
was submitted and no price quote or sales contact was requested.

## Attribution continuity

Public JavaScript records:

- referrer;
- UTM source, medium, campaign, term, and content;
- major ad click IDs;
- Impact affiliate parameters;
- first- and last-touch URLs;
- page views;
- banner impressions and clicks;
- mobile signup; and
- a product-download event on the download page.

This yields a plausible website model:

```text
first touch
→ later campaign touch
→ landing behavior
→ CTA or handoff
```

The crucial product events are not exposed:

```text
handoff
→ verified install
→ first launch
→ account authorization
→ completed initial sync
→ first search, triage, or send value
→ voluntary day-1/day-7 return
→ payment and refund
```

The absence of public evidence does not mean Mailbird fails to measure these
privately. It means an outsider cannot use the visible web instrumentation as
proof of a complete funnel.

## Conversion strengths

- The free entry is clear and requires no sales call.
- Campaign, affiliate, and advertising identifiers are retained on the web.
- Direct and store routes support different trust and attribution needs.
- Annual, Pay Once, business, volume, and add-on offers monetize different
  preferences.
- A portal and active support corpus can reduce license-management friction.

## Conversion risks

- Provider-help traffic may have little initial product intent.
- Website and store prices are not normalized.
- Mac/Windows feature and protocol parity is incomplete.
- Stale Mac-coming fragments can confuse current availability.
- Discount anchors, “last sold” notices, and repeated save language can reduce
  calm trust.
- Pay Once plus separate Lifetime Updates is cognitively and reputationally
  costly.
- First-party reach numbers are not consistently defined.
- No public cohort connects acquisition to useful, retained use.

## Implications for Tecotype

Tecotype should design one measurable path before adding channel variety:

```text
release-accurate source
→ calm landing page
→ verified signed Mac handoff
→ clean first launch
→ mailbox connection
→ completed sync
→ message-matched Better search or keyboard-triage value
→ voluntary day-1 and day-7 return
→ €149 annual or €15 monthly payment
```

The current signed Mac target is an internal release capability, not proof of a
public release. The CTA must remain gated until clean-machine install, update,
auth, licensing/payment, privacy, safe-send, and support readiness are
verified. Windows demand can be researched now, but its planned signed
distribution must not be presented as shipped.

The site should capture only the attribution needed to decide whether a source
produces retained value. Tecotype does not need Mailbird's volume of
identifiers, promotional widgets, or pricing variants to run the first test.
