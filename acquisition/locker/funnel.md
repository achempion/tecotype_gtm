# Locker funnel

Research date: **2026-07-17**

Scope: **public path through direct download, Polar checkout, and public
license instructions**

No disk image was fetched or executed, and the app was not installed or
launched. No license was claimed or purchased, and no mailbox was connected.
Post-install behavior is reconstructed from the current site, legal pages,
changelog, GitHub release metadata, and the public post-purchase welcome
route.

## Funnel summary

Locker separates trial from purchase:

```text
Homepage
→ free public disk-image download
→ install and inspect
→ separate $39.99 purchase
→ publisher says Polar emails a license key
→ paste key into Locker settings
→ connect mailbox
→ first useful action and retained use unknown
```

It also exposed a small giveaway path:

```text
Founder beta request or another unknown source
→ homepage
→ one of five free keys
→ key claim
→ install, mailbox connection, and retained use unknown
```

The five keys were shown as claimed at capture. The page offered a pre-filled
email to contact the maker about testing.

## Stage 1: landing page

The current page asks for three actions:

1. Download the app.
2. Buy the current founder license.
3. Contact Nathan to test.

The direct download appears in the navigation and hero. The buy CTA appears
after the feature and privacy sections. No email, account, or payment is
required before obtaining the disk image.

No visible acquisition-source parameter is attached to the download, checkout
endpoint, or maker-email link.

## Stage 2: download

The download URL is:

```text
https://github.com/newtophilly/locker-releases/releases/latest/download/Locker.dmg
```

It resolves to v0.3.0 in the public
[`locker-releases`](https://github.com/newtophilly/locker-releases) repository.

### Public release ledger

| Release | Published | Disk-image size | Captured downloads | Public notes |
| --- | --- | ---: | ---: | --- |
| v0.1.0 | 2026-06-23 | 113,072,932 bytes | 6 | First Apple Silicon build; release notes claim signed/notarized |
| v0.2.0 | 2026-06-23 | 113,376,118 bytes | 4 | Updates, command bar, Sent, fixes |
| v0.3.0 | 2026-06-24 | 158,996,673 bytes | 17 | Meaning search and port selection |

GitHub also exposes SHA-256 digests. The v0.3.0 disk-image digest is:

```text
ca01250784211d1e191257f5978c3949158b48c3ce0dad6139bad36bf714996d
```

The repository description and v0.1.0/v0.2.0 release text describe the
downloads as signed and notarized. Those are publisher-authored claims. The
disk images were not fetched, so their code signatures and notarization were
not independently verified.

The download count measures asset requests. It can include:

- The maker.
- Repeated downloads.
- Update or installation testing.
- One person downloading more than one release.
- Requests that never became an install.

It does not reveal unique users, successful installs, mailbox connections, or
retention.

## Stage 3: public license offer

The visible ladder is:

| Tier | Price | Quantity / duration |
| --- | ---: | --- |
| Founder lifetime | $39.99 | First 10 customers |
| Lifetime | $70 | Next 50 customers |
| Four-year updates | $129 | After the first 60 |

The app keeps working after the update window. Future updates require renewal
at the then-posted rate. The page promises no monthly subscription.

At capture:

```text
Founder lifetime — $39.99 · 10 of 10 left
```

This is consistent with no completed purchase having reduced the first paid
tier. It is not proof of zero revenue because the counter's implementation,
refresh behavior, manual adjustments, refunds, and alternative sales are not
public.

## Stage 4: checkout

The homepage endpoint:

```text
/api/license/checkout?plan=current
```

redirected to a live Polar checkout for:

```text
Pin311
Locker — Lifetime (Mac)
$39.99
```

The captured checkout:

- Asked for email, card, cardholder name, and billing address.
- Calculated taxes at checkout.
- Offered a discount-code control.
- Described the payment as a one-time charge.
- Named Polar Software, Inc. as merchant of record.

No payment details were entered and `Pay now` was not selected.

The homepage does not explain which exact v0.3.0 capabilities require a
license, how long an unlicensed evaluation lasts, or the moment a user is
expected to pay. The refund page only says the app is free to download so a
person can see what they are getting.

## Stage 5: license delivery and activation

The public [`/welcome`](https://www.inbox.locker/welcome) route says:

1. Polar emails a `LOCKER-…` key.
2. The buyer opens `Locker → Settings → License`.
3. The buyer pastes the key and selects `Activate`.

The privacy policy says the app connects to a license-validation service. The
actual delivery time, activation success, offline behavior, device limit,
recovery flow, and support burden were not tested.

## Stage 6: mailbox connection

Public copy describes:

- Gmail and other IMAP accounts connected directly.
- App passwords for relevant providers.
- Apple Mail automation for some Outlook, Microsoft 365, Exchange, or managed
  accounts that permit Apple Mail.
- Direct SMTP or Apple Mail sending.
- Local processing for the bundled on-device search behavior.

The changelog labels the Apple Mail work-account path as v0.4.0 “in testing,”
so it must not be treated as part of v0.3.0.

No public path establishes:

- Install success on a clean Mac.
- Gatekeeper or permission behavior.
- License-before-account or account-before-license order.
- Provider-specific app-password guidance.
- First-sync duration or mailbox-size handling.
- The first useful search, triage, or reply.
- Day-one or day-seven return.

## Giveaway path

The homepage showed:

- Five free keys.
- All five marked `Taken`.
- A note that the claimed key unlocks the full app.
- A contact link for additional testers.

The page did not show:

- Claim timestamps.
- Source tags.
- Whether claims required an email address.
- Whether one person could claim more than one.
- Whether any key was activated.
- Whether any claimant connected a mailbox or returned.

The Reddit post is temporally and conceptually adjacent, but there is no public
evidence assigning any of the five claims to it.

## Refund and risk allocation

The [refund policy](https://www.inbox.locker/refunds) says all sales are final
except where law requires otherwise. It points to the public download as the
way to evaluate before paying.

The [terms](https://www.inbox.locker/terms) say:

- The license is personal and non-transferable.
- The product is provided as is.
- The user is responsible for reviewing actions before approval.
- The Mac and future web products are separate.

This makes the free-download stage especially important. The public funnel
still lacks a clearly stated evaluation limit and release-accurate checklist.

## Conversion evidence

| Funnel stage | Public evidence | What remains unknown |
| --- | --- | --- |
| Visit | Live page and search result | Visitors and source mix |
| Community response | One interested Reddit comment | Click or download |
| Download | 27 disk-image requests across releases | Unique installs |
| Free license | 5 keys shown as claimed | Counter implementation, activations, and use |
| Paid checkout | Live $39.99 Polar checkout page; completion untested | Checkout starts and completions |
| Paid inventory | 10 of 10 shown left | Counter reliability and revenue |
| License activation | Public instructions | Completion rate |
| Mailbox connection | Public copy | Completion, errors, and provider mix |
| First value | Product examples | Actual behavior |
| Retention | None | Entirely unknown |

## Tecotype implications

- Separating download from purchase is worth testing only after Tecotype has a
  public site, no-account first run, verified signed/notarized updateable
  distribution, Gmail restricted API audit readiness, safe compose/reply/send
  behavior, licensing and payment, and source-to-activation measurement.
- The evaluation promise should state what works in the downloaded build and
  what requires payment.
- Source, download, install, account connection, first value, retention, and
  purchase should remain separate events.
- A claimed key is not activation; a disk-image request is not a user.
- Tecotype should avoid no-refund pressure and count-based urgency in favor of
  an explicit, calm evaluation policy once that policy is decided.
