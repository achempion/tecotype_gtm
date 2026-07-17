# Epistles acquisition funnel

Research date: **2026-07-17**

The public funnel was inspected without creating an account, connecting a
mailbox, downloading or installing a package, starting a trial, or submitting
payment.

## Funnel summary

Epistles now offers three routes:

```text
Homepage, community post, store search, or comparison page
→ free platform download
→ up to two accounts, with no Epistles account claimed as required to start
→ first successful sync and useful mail action unobserved
```

```text
Free use or pricing page
→ annual Pro upgrade
→ Epistles sign-in / account creation / email-code flow
→ 14-day trial
→ $35/year
→ renewal and retained use unobserved
```

```text
Pricing or Bereans page
→ $79 / $99 lifetime offer
→ Epistles sign-in / account creation
→ Stripe checkout
→ first-party seat counter
→ payment, activation, refund, and retained use mostly unverified
```

The broad download path is unusually accessible. The paid path introduces a
new Epistles identity before checkout.

## Offer structure

| Offer | Public terms | Public action | Boundary |
| --- | --- | --- | --- |
| Free | $0; up to 2 accounts; all 8 claimed platforms | Download | No account claimed as required to start; actual onboarding not exercised |
| Pro annual | $35/year; unlimited accounts; 14-day trial | `app.epistles.com/upgrade?plan=annual` | Route showed sign-in gate; trial and cancellation flow not tested |
| Founding lifetime, seats 1–100 | $79 once | `app.epistles.com/upgrade?plan=bereans` | Capped offer; first-party counter, terms conflict, and refunds unverified |
| Founding lifetime, seats 101–500 | $99 once | Same route | Advertised future tier; no seat in this tier yet on research date |

The current paid price is far below Tecotype's intended €149/year or
€15/month. That is a competitor fact, not a price recommendation: public
evidence does not show Epistles' retention, refund rate, support cost, provider
maintenance cost, or unit economics.

## Download distribution

The [download page](https://epistles.com/download/) offered:

| Platform | Route | Current evidence |
| --- | --- | --- |
| macOS | Direct DMG and Apple App Store | Direct manifest 1.3.9; US App Store 1.3.8 |
| Windows | Direct x64 and arm64 packages | Direct manifest 1.3.9 |
| Linux | APT, RPM, Flatpak, and Arch paths | Installation instructions and hosted repositories |
| iOS / iPadOS | Apple App Store | Same universal listing |
| Android | Google Play and direct APK | Google Play 1.3.8; direct APK manifest 1.3.8 |
| Web | Claimed platform | Public web-app use was not exercised |
| Apple Watch | Companion app claim | Store/build behavior not tested |
| Wear OS | Companion app claim | Store/build behavior not tested |

Direct artifact metadata captured on the research date:

- macOS 1.3.9, published 2026-07-17 05:14 UTC, 57,293,437 bytes,
  SHA-256
  `0179c6479ed48c8aa3e456de6e372889b5b4907a2d0fe33db910d3e26bb18094`;
- Windows 1.3.9 x64 and arm64, published 2026-07-17 01:41 UTC;
- Android 1.3.8, published 2026-07-16 21:31 UTC, 107,424,509 bytes,
  SHA-256
  `89b6dd08606b67e12f1921d0dfaadd70382aa5133b099faca173d6409ab6c18e`.

The manifests establish listed availability, not download count, successful
installation, or safe operation.

## Store evidence

### Google Play

The [Google Play listing](https://play.google.com/store/apps/details?id=com.epistles)
showed:

- **100+ downloads**;
- version 1.3.8;
- updated 2026-07-16;
- developer **Moriah LLC**; and
- developer-supplied declarations of no data collected and no data shared.

The download band is the clearest independent distribution signal. It is not
an exact count, unique users, connected accounts, or retained users.

The data-safety declarations conflict with Epistles' own privacy and security
pages, which describe processing account identifiers, authentication and
session data, some provider tokens, push tokens, support records, and optional
tracking metadata. The dossier records the textual conflict without inferring
intent.

### Apple App Store

The US listing and iTunes metadata showed:

- original release on 2026-06-04;
- current version 1.3.8, released 2026-07-16 22:43 UTC;
- average rating **3.66667/5** from **3 ratings**;
- listed size 77,533,184 bytes; and
- seller/developer **Netwarden LLC**.

The sample is too small for a stable satisfaction conclusion. The seller name
also differs from the website footer and Google Play; that adds verification
work but is not evidence of misconduct.

## Paid handoff

Both upgrade routes rendered the same Epistles identity gate:

- email and password;
- forgot-password link;
- create-account path; and
- email-code option.

No account was created and no form was submitted. Stripe is named as the
billing provider in the
[security page](https://epistles.com/security/), and the changelog mentions
web checkout plus Apple Pay and Google Pay. The actual checkout, taxes,
renewal, cancellation, refund, and receipt experience were not observed.

## Lifetime counter

The public endpoint
[`/api/bereans/count`](https://api.epistles.net/api/bereans/count) returned:

```json
{
  "total": 500,
  "sold": 83,
  "remaining": 417,
  "current_tier": "true-bereans",
  "current_price_cents": 7900,
  "next_milestone": 100,
  "updated_at": "2026-07-17T14:12:21.636Z"
}
```

If all 83 counted seats represented completed $79 payments, their nominal
face value would be **$6,557** before tax, fees, refunds, chargebacks, and
complimentary seats.

That conditional arithmetic is not revenue evidence:

- the endpoint is operated by Epistles;
- the meaning of “sold” was not independently audited;
- buyer uniqueness and payment completion are unknown;
- refunds are not netted publicly; and
- one public commenter claimed buying seat 54 and requesting a refund.

The counter is best treated as a first-party commercial signal.

## Legal and trust friction

The [Bereans page](https://epistles.com/bereans/) and
[promises page](https://epistles.com/promises/) say the lifetime refund,
funding/acquisition, abandonment, and MIT source-release promises are mirrored
in the Terms. The current
[Terms](https://epistles.com/terms/) do not contain those clauses and allow
features to change or be discontinued.

The Bereans page also refers to a public client repository and a no-commit
shutdown trigger. No public Epistles client source repository was linked or
found in the captured founder profile; `repo.epistles.com` distributes
packages, not source.

These conflicts sit immediately beside the purchase decision and therefore
belong in the funnel analysis.

## Attribution audit

| Handoff | Visible source data |
| --- | --- |
| Homepage → download | None |
| Homepage → pricing | None |
| Download page → Apple / Google stores | No campaign parameter observed |
| Download page → direct repositories | No campaign parameter observed |
| Reddit post → homepage or old waitlist | No UTM/source parameter observed |
| Annual upgrade | `plan=annual` only |
| Lifetime upgrade | `plan=bereans` only |

Google Analytics, referrers, server logs, store consoles, or private event
tracking may contain more information. The public URLs do not show a durable
source identity through install and activation.

## What the public funnel proves

Observed:

- a broad free distribution surface;
- a two-account free tier;
- live paid upgrade gates;
- a stated 14-day annual trial;
- a public lifetime counter;
- at least 100 Google Play downloads;
- three US App Store ratings; and
- one unverified public self-report of a lifetime purchase and refund request.

Not observed:

- landing-page sessions or CTA clicks;
- package request counts;
- completed installs;
- account-connection success;
- first completed sync;
- a useful mail action;
- next-day or day-seven return;
- completed or net paid transactions;
- refunds or chargebacks;
- active paid seats;
- renewal; or
- source-level conversion.

## Tecotype implication

Tecotype should keep the first public path narrower and fully measurable:

```text
source-tagged problem page
→ signed Mac download
→ first-run/no-account state
→ Gmail or IMAP connection
→ first successful sync
→ message-matched first-value action
→ voluntary return
→ license/payment
```

That path is only suitable after the current public-site, licensing/payment,
Gmail restricted-API audit, signing/distribution, safe-send, and acquisition
measurement prerequisites are complete. Before then, interviews and private
problem validation should not be described as access to a shipped product.

Source details are in [requests.md](./requests.md).
