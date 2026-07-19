# Mac App Store distribution

Status: Distribution and pricing decision; implementation pending

Last reviewed: 2026-07-19

## Decision

Tecotype will have two independent purchase channels:

| Purchase channel | Product purchased | Billing |
| --- | --- | --- |
| Mac App Store | Mac App Store build on macOS only | Apple in-app purchase |
| Tecotype website | Direct builds for macOS, Windows, and Linux | Tecotype website checkout |

Both channels use the same Individual price:

- €15 per month.
- €149 per year.

The two macOS builds should have the same mail features, but their platform
licences are different:

- An App Store subscription unlocks only the Mac App Store build.
- A website subscription unlocks the direct macOS, Windows, and Linux builds.
- A purchase from one channel does not unlock the other channel.
- Website customers on Mac install the direct build, not the Store build.
- Store customers who later want all desktop platforms cancel with Apple and
  buy from the website after the Apple subscription expires.

This separation is deliberate. Tecotype will not build an Apple-to-Tecotype
cross-platform entitlement bridge for launch.

## Why keep the Mac App Store

The Store is a trust and purchase-choice channel.

For an unknown email client, an Apple-reviewed listing, familiar installation,
Apple-managed payment, purchase restoration, and App Store updates can reduce
concern about installing software that will access a mailbox.

That trust does not establish demand:

- Do not include Store discovery in the base acquisition forecast.
- Measure Store product-page views, downloads, evaluations, and first paid
  subscriptions separately.
- Do not describe Apple review as a privacy or security audit.
- The direct Mac build still needs signing, notarization, clear privacy
  disclosure, and independent product reviews.

The Store listing can also reassure a person who ultimately buys the
cross-platform edition on the website. Apple has reviewed the Store build, not
the separate direct binary, so public copy must not blur that distinction.

## Mac App Store purchase

The Store build is free to download and offers Apple auto-renewable
subscriptions:

```text
Download from the Mac App Store
        ↓
One month free with Apple
        ↓
€149/year or €15/month
        ↓
Mac App Store build on macOS
```

Use localized prices returned by Apple. Before confirmation, state:

- the trial or offer duration;
- the renewal price and interval;
- that billing renews automatically unless cancelled; and
- that the purchase covers the Mac App Store edition only.

Include `Restore purchases` and `Manage subscription`. Apple owns payment,
refund, cancellation, and payment-method management for this channel.

The Store build must not ask for a licence key. The Mac-only purchase removes
the need for a Tecotype billing account whose only purpose would be transferring
an Apple entitlement to Windows or Linux.

## Affiliate offer codes

Apple supports subscription offer codes. They make a cookie-free Store
affiliate path possible:

```text
independent review
→ creator-specific Apple redemption link
→ App Store installs Tecotype if necessary
→ customer redeems a paid first-year offer
→ Apple reports the custom code
```

For the first bounded affiliate test:

- Create a distinct pay-up-front first-year offer for each approved affiliate
  at €99, or the selected localized storefront equivalent.
- Give each offer a distinct reference name and custom code. The pilot limit of
  five affiliates remains inside Apple's limit of ten active offers per
  subscription product.
- Give the affiliate Apple's redemption URL with the code included.
- Treat the paid first-year offer as replacing the free introductory month.
  Do not combine the two in the pilot.
- Disclose that the subscription renews at the normal €149 annual price unless
  cancelled.
- Calculate commission from confirmed, non-refunded paid redemptions. A 40%
  commission on a €99 sale is €39.60 and remains below the approved USD 50
  per-customer commission ceiling.
- Pay affiliates separately. Apple does not calculate or send their
  commission.

Tecotype may also show `Redeem offer code` on its Store paywall. The redemption
URL is preferable because the customer does not need to copy or type the code.
Apple currently requires macOS 15 or later for offer-code redemption, so the
pilot cannot count older Macs as reachable code traffic.

Apple's redemption report exposes each custom code and its redemption count.
The separate offer reference names allow paid sales, proceeds, and refunds to
be reconciled per approved affiliate in Apple's subscription reports. Neither
report proves review traffic or conversion before the code is redeemed.
Store-code attribution therefore repairs the purchase-attribution mechanism,
not the discovery or capacity gate.

## Website purchase

The website route is the cross-platform and business-billing route:

```text
Tecotype website
→ website evaluation and checkout
→ direct signed application
→ macOS, Windows, and Linux
```

Website checkout should accept the legal name, billing address, and VAT number
needed for a business invoice where applicable. The payment and tax provider
must validate the final invoice and VAT treatment.

Affiliate attribution on this route should use an explicit referral code tied
to the checkout and order. It must not require third-party tracking cookies,
advertising pixels, or a consent banner.

## Business purchasing boundary

The App Store edition is an individual purchase route, not Tecotype's business
procurement route.

- The purchaser receives Apple's receipt, not a Tecotype invoice.
- Tecotype cannot add a company name or VAT number to Apple's individual IAP
  checkout.
- Apple Business can distribute app licences, but Apple states that in-app
  purchases and subscriptions are not compatible with volume purchasing,
  managed apps, or Managed Apple Accounts.
- A person may expense an Apple purchase using their employer's card or
  process, but Tecotype should not promise that it satisfies the employer's VAT
  or procurement requirements.

A buyer who needs a Tecotype invoice with company and VAT information should
use website checkout and the direct application.

Team licences, seat administration, purchase orders, and enterprise contracts
remain future decisions. They are not included in the Individual plan.

## Trial

The ordinary offer in both channels is `One month free` followed by the
selected subscription:

- Apple handles payment authorization and eligibility for the Store trial.
- Website checkout collects a payment method before its trial begins.
- The two trials are independent because the purchase channels are not linked.
- Say `One month free`, not `30 days free`; a calendar month can contain 28 to
  31 days.
- Show the renewal price and platform scope before confirmation.

The paid affiliate offer code replaces the free month for that Store purchase
so a redemption is a paid acquisition event.

## Two Mac builds

| Concern | Direct Mac build | Mac App Store build |
| --- | --- | --- |
| Distribution | Signed and notarized download | App Store |
| Purchase | Tecotype website | Apple IAP |
| Platform licence | macOS, Windows, Linux | Store build on macOS |
| Updates | Tecotype updater | App Store |
| Sandbox | Direct-app requirements | Apple App Sandbox |
| Affiliate attribution | Website referral and order code | Apple custom offer code |
| Business invoice | Tecotype checkout | Not offered by Tecotype |

The mail experience should remain equivalent on macOS. Packaging, commerce,
licensing, updates, and sandbox behavior differ by build.

## Current implementation boundary

The verified source state on 2026-07-19 is direct-distribution-only:

- `electron-builder.yml` targets DMG and ZIP, not `mas` or `mas-dev`.
- There is no Store-specific sandbox target or Apple IAP flow.
- The current Mac application uses Tecotype's updater.
- Website billing and the direct cross-platform licence are not implemented.

The Store build, Apple purchase flow, offer codes, website checkout, and public
Windows and Linux releases must not be presented as shipped.

## Store release gate

Before release:

1. Build and sign the App Sandbox target.
2. Verify Gmail, generic IMAP, SMTP, attachments, credential storage, local
   search, Better search, sleep/wake, and relaunch in the sandbox.
3. Remove Tecotype's updater from the Store build.
4. Test monthly and annual purchase, introductory trial, paid offer code,
   refund, cancellation, expiry, restore, and interrupted transactions.
5. Verify that Store and direct subscriptions never silently unlock or bill
   the other build.
6. Put the Mac-only licence statement on the Store product page and purchase
   screen.
7. Confirm affiliate reporting with a sandbox offer code before recruiting
   creators.
8. Release only after the Store build passes the same mail regression coverage
   as the direct Mac build.

## Primary sources

- [App Review Guidelines](https://developer.apple.com/app-store/review/guidelines/).
- [Auto-renewable subscriptions](https://developer.apple.com/app-store/subscriptions/).
- [Set up subscription offer codes](https://developer.apple.com/help/app-store-connect/manage-subscriptions/set-up-subscription-offer-codes/).
- [Subscription offer redemption report](https://developer.apple.com/help/app-store-connect/reference/reporting/subscription-offer-redemption-report/).
- [Apple content distribution for organizations](https://support.apple.com/guide/deployment/intro-to-content-distribution-depe1553f932/1/web/1.0).
- [Electron Mac App Store submission](https://www.electronjs.org/docs/latest/tutorial/mac-app-store-submission-guide/).
