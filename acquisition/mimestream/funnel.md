# Public funnel

Research date: **2026-07-17**

No email address, Google authorization, purchase, or live app launch was performed. The reconstruction below uses current public pages, network-visible form behavior, pricing/account screens, installer metadata, and archived pages.

## Current trial path

```text
Press, community, review, partner, or search
→ homepage: “Made for Mac. Optimized for Gmail.”
→ Download Free Trial
→ /download
→ automatic Mimestream_1.10.4.dmg download
→ install and launch
→ Google sign-in / Mimestream trial setup inferred from static app resources
→ account sync and first meaningful use unobserved
→ 14-day trial
→ subscription or deactivation
```

### Homepage to installer

Observed:

- Primary CTA links directly to [the download route](https://mimestream.com/download).
- The download page says the download should begin automatically and provides a direct fallback link.
- The page points to `Mimestream_1.10.4.dmg`.
- Current public requirement is macOS 12 Monterey or newer.
- Homepage does not require an email address or card before download.

Before the user clarified the no-download research boundary, the current disk
image was downloaded for metadata inspection, mounted read-only, and never
launched or installed. The temporary disk image was removed on 2026-07-17;
all subsequent research is public-web and metadata only:

| Field | Observed value |
| --- | --- |
| File | `Mimestream_1.10.4.dmg` |
| Size | 12,824,884 bytes |
| SHA-256 | `4c741d311148a4f3aaf94a797c6e3d34fc446473a675acc69d3546eb5c0296f3` |
| App version / build | 1.10.4 / 392 |
| Architectures | Apple Silicon and Intel |
| Minimum macOS | 12.0 |
| Bundle ID | `com.mimestream.Mimestream` |
| Updates | Sparkle feed metadata present |
| Signing | Runtime signature metadata present; notarization ticket stapled |

The local system-security assessment command returned an internal signing error, so it is not used as proof of acceptance. The static signature and notarization metadata are evidence of a prepared direct-distribution artifact, not a complete installation/security test.

### Post-install boundary

Static bundle resources include text such as:

- “Welcome to Mimestream”
- “Sign in with Google”
- “I already have a license”
- “Buy Now”
- trial and subscription states

Those strings support the broad presence of onboarding, Google connection, trial, and licensing paths. They do not prove exact screen order, usability, authorization scopes, sync completion, or activation. The app was not launched and Gmail OAuth was not granted.

Likely activation candidates, which remain inferred:

- successful Google authorization;
- initial mailbox sync;
- first label/category triage action;
- first successful Gmail search;
- first completed compose/reply.

Mimestream’s actual activation definition and analytics are not public.

## Current purchase path

The public pricing route can bypass the trial-first CTA:

```text
Pricing page
→ choose annual or monthly, individual or group
→ Subscribe
→ accounts.mimestream.com/create-account
→ enter email + complete Cloudflare Turnstile
→ agree to Terms and Privacy Policy
→ Continue
→ verification/password/checkout sequence unobserved
→ Paddle payment inferred from public pricing code and policy
→ subscription activation unobserved
```

Observed on the unauthenticated [account-creation page](https://accounts.mimestream.com/create-account?plan=annual&purchase=true):

- heading: “Create your account”;
- one email field;
- Cloudflare Turnstile;
- agreement to Terms and Privacy Policy;
- disclosure that the account receives Mimestream emails;
- Continue remains unavailable until the anti-bot step completes;
- existing-account sign-in link;
- strict session cookie with a one-week lifetime.

No email was entered and no form was submitted. The verification, password, checkout, tax, payment, and activation screens remain unobserved.

Public [pricing](https://mimestream.com/pricing/) and [FAQ](https://mimestream.com/faqs) state:

- trial is 14 days and fully functional;
- no card is required for the trial;
- app functionality deactivates after trial expiration without a subscription;
- annual individual plan is $49.99 and monthly is $4.99;
- group plans are per seat;
- purchases are direct rather than through the Mac App Store;
- annual refunds are available within 30 days; monthly payments are non-refundable.

The page sends plan, purchase, seat, and coupon parameters into the account route. Paddle’s script appears on the pricing page and Paddle is named in the privacy policy. Checkout completion remains inferred, not tested.

Mimestream’s [promotion FAQ](https://mimestream.com/pricing/promotion-faqs) says occasional offers apply to a new annual license’s first year and may expire before a visitor finishes the full trial. It also says a person whose previous trial was more than a month ago can become eligible for another 14-day trial. This is observed policy, not evidence of promotion use or lift.

## Newsletter path

```text
Homepage footer
→ enter email
→ /api/v1/listSignup with source “website”
→ confirmation message
→ confirmation email
→ confirmed subscriber
→ later release/marketing email actions unknown
```

The form includes a honeypot and the endpoint receives the email, website source, and an iOS-beta value when applicable. No address was submitted. List size, confirmation rate, send frequency, clicks, and downstream product use are unknown.

## iOS beta path

The current [iOS beta page](https://mimestream.com/ios-beta) requires:

- iOS 26 or newer;
- an available TestFlight place; and
- a Mimestream customer account subscribed for at least 12 months.

The route therefore serves expansion and retention among established subscribers. It is not a normal first-touch acquisition funnel.

The general FAQ still says there is no iOS version and describes TestFlight as future work. The dedicated iOS page and current Private Push deployment page are more specific and current, but the inconsistency can confuse visitors.

## Historical funnels

### May–June 2020: invitation-gated beta

```text
Early discovery
→ “The best Gmail experience for macOS”
→ Request Access
→ Mailchimp waitlist
→ invitation and install unknown
```

The archived page explicitly describes joining a waitlist for a beta invitation. Wait time, invitation rate, and use are unavailable.

### September 2020–May 2023: public free beta

```text
Show HN / Product Hunt / Mac press / word of mouth
→ “A native macOS email client for Gmail”
→ Join the Beta
→ beta signup/download
→ Google connection
→ repeated beta use and feedback unknown
```

The free beta lasted more than two years. Mimestream’s 1.0 launch says more than 167,000 users joined, but supplies no source or active-use definition.

### May 2023: beta-to-paid conversion

```text
Existing beta user
→ product/in-app/email notice
→ beta build expires June 1
→ special beta-user offer or public 40%-off annual offer
→ Mimestream 1.0 download
→ 14-day no-card trial
→ subscription
```

New visitors saw the same 14-day trial and a first-year annual price of $29.99 until June 9. The special beta-user offer was not publicly specified.

Observed public friction:

- short interval between launch and beta expiration;
- subscription objections;
- some users felt pricing/transition communication was abrupt;
- other users publicly said they paid or considered the app worth the price.

The discussion is self-selected and small. It reveals possible failure modes, not the net effect of the transition.

## Funnel evidence table

| Step | Status | Evidence |
| --- | --- | --- |
| Discovery impression | Observed surfaces | Search results, launch pages, publications, backlinks |
| Homepage visit | Surface observed | No analytics |
| CTA destination | Observed | Direct download or account route |
| Installer transfer | Observed technically | No user completion rate |
| Install and app launch | Not executed | Static artifact only |
| Google authorization | Not executed | Static strings and product documentation |
| First sync | Unobservable | No internal telemetry |
| Meaningful activation | Undefined publicly | Candidate events are inferred |
| Trial start | Public offer / app state inferred | No test account |
| Retained use | Unobservable | First-party aggregate claims lack retention definition |
| Payment | Public price and checkout provider observed | No purchase |
| Source-level revenue | Unobservable | No internal attribution or finance data |

## Measurement lessons

Mimestream’s public surfaces contain only limited visible source instrumentation:

- Product Hunt’s destination has `?ref=producthunt`.
- Newsletter submissions label the source as `website`.
- Pricing carries plan, purchase, seat, and coupon values.
- No general source parameter was observed on the homepage download CTA.

Mimestream may use app events, server logs, account data, or other systems that are not public. The absence of visible browser analytics is not evidence of no measurement.

For Tecotype, the minimal useful sequence after the release gate is:

```text
source-tagged landing visit
→ installer download
→ first app launch
→ successful Gmail or IMAP account connection
→ meaningful keyboard/search/triage activation
→ retained use
→ paid conversion when licensing exists
```

Source data should be privacy-preserving, documented, and optional where appropriate. Raw visits and downloads should not be treated as value.

## What can and cannot be learned

Supported:

- Mimestream reduced top-of-funnel friction with direct download and no-card trial.
- Its long free beta preceded the paid launch and a large cumulative first-party count.
- Pricing can be entered either after trial or directly from the website.
- The paid transition used both a deadline and a first-year discount.

Not supported:

- the best source;
- page-to-download rate;
- installer-to-account rate;
- time to first value;
- trial start or trial-to-paid rate;
- retention or lifetime value;
- whether discounting was incremental;
- whether the free-beta duration produced more customers than a paid path would have.
