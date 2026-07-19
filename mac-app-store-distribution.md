# Mac App Store distribution

Status: Working distribution decision; implementation pending

Last reviewed: 2026-07-19

Policy snapshot: Apple's App Review Guidelines last updated June 8, 2026.
Re-check the linked primary sources before the first submission and whenever
the purchase flow changes.

## Decision

Publish Tecotype in the Mac App Store as a second macOS acquisition channel if
the application passes the sandbox and review release gate.

- Keep the direct, Developer ID-signed Mac build and website checkout.
- Make the Mac App Store build free to download.
- Ask people to continue with a Tecotype account before checking access.
- Unlock an existing website or Apple entitlement after sign-in.
- Offer Apple in-app purchase to a Store user who has no entitlement.
- Use website billing in the direct Mac, Windows, and Linux distributions.
- Give every active Individual entitlement access on all supported desktop
  platforms. An Apple subscriber does not buy a second Windows or Linux
  subscription.
- Do not use license keys in the Mac App Store build.

This is a distribution and billing design, not a description of the current
client. The Store build, Tecotype account, entitlement service, Apple purchase
flow, and website billing flow have not been implemented.

## What the Store is expected to do

The reason to add the Mac App Store is install confidence and customer choice,
not an assumption that its search will produce material demand.

Apple says Store apps are reviewed and scanned for malware, and that editorial
and search surfaces help people discover apps. That establishes the Store's
trust and browsing mechanisms, but it is not evidence that an unknown premium
desktop email client will receive meaningful organic acquisition. Whether
Store installation materially improves Tecotype's conversion remains a
hypothesis to measure.

The strongest directly relevant but still weak public sales evidence is an
[Electron case note](https://www.electronjs.org/blog/in-app-purchases) from 2018. One developer reported a 40% increase in sales after adding Mac App Store
in-app purchase. It is a single, old, self-reported example and does not isolate
Store discovery from the simpler purchase flow.

The current paid email-client comparison is more useful as a policy and
customer-expectation signal than as an acquisition forecast. Canary, Airmail,
Mailbird, Spark, Outlook, and Spike all expose Apple in-app purchase in their
Mac-capable Store listings. Superhuman, Polymail, Missive, and Front demonstrate
that higher externally billed subscriptions also exist, but their products and
distribution differ. Prices and links are maintained in
[pricing](./pricing.md).

Therefore:

- Do not include Store discovery in the base acquisition forecast.
- Attribute Store product-page views, downloads, Tecotype account creation,
  trials, and first-time paid subscriptions as a separate funnel.
- Compare net new paid customers and contribution after Apple commission
  against the engineering and review cost.
- Keep the Store listing if it creates worthwhile first-time paid acquisition
  or materially reduces installation objections.
- Treat the Mac App Store as an acquisition surface, not as a qualifying
  distribution partnership under Tecotype's stricter permanent-placement
  definition.

## Why a license-code-only Store app is not the plan

Apple's current rules create two separate constraints:

1. [Guideline 2.4.5(vi)](https://developer.apple.com/app-store/review/guidelines/)
   says Mac App Store apps may not present a license screen at launch, require
   license keys, or implement their own copy protection.
2. [Guideline 3.1.1](https://developer.apple.com/app-store/review/guidelines/)
   says functionality unlocked inside an app must use in-app purchase and
   explicitly lists license keys as a prohibited alternative.

Emailing a free license code to anyone who enters an address would still make a
license code the Store build's unlock mechanism. It is not the recommended
review position.

Apple does permit important exceptions, but neither removes the need for IAP in
Tecotype's proposed Store flow:

- Guideline 3.1.3(b) permits a multiplatform app to recognize subscriptions or
  features acquired on another platform or website when the same access is
  also available as IAP in the app.
- Guideline 3.1.3(f) permits a free stand-alone companion to a paid web tool,
  including an email service, when the app contains neither purchasing nor an
  external purchase call to action.

HEY and Basecamp are account services, so their Store presence does not prove
that an independently sold desktop client may use license keys. Tecotype should
use the clearer multiplatform path: recognize existing website customers and
also offer an equivalent Apple purchase in the Store build.

Except where a storefront-specific rule explicitly permits it, the Store build
must not direct a new user to website checkout. Maintain one conservative
global Store experience:

```text
Continue with email
        ↓
Active entitlement? ── yes ──> Open Tecotype
        │
        no
        ↓
Start one-month trial with Apple
```

The direct Mac, Windows, and Linux builds use the same account check but send a
new customer to Tecotype's website checkout.

## Plan and trial

Create one App Store subscription group named `Tecotype Individual` with two
auto-renewable products:

- Individual monthly.
- Individual annual.

Both products unlock the same capabilities. The annual option is primary and
the monthly option is the lower-commitment alternative described in
[pricing](./pricing.md). Use the localized prices returned by the Store rather
than hard-coding a currency or amount in the Store build.

The working launch offer is one free month for an eligible new subscriber:

- Configure a free introductory offer for both products in the same
  subscription group.
- Describe it as `One month free`, not `30 days free`. Apple's one-month trial
  can last 28 to 31 days.
- State the selected renewal price, billing interval, and automatic renewal
  before opening the Apple purchase sheet.
- Treat it as a payment-authorized trial: Apple handles payment authorization
  for Store IAP, and website checkout collects a payment method before its
  trial starts.
- Let Apple decide Apple Account eligibility. A person can use only one
  introductory offer per subscription group.
- Mirror the one-month offer in website checkout so the public proposition is
  consistent.
- Treat the trial as an active cross-platform entitlement. A person who starts
  it on the Mac App Store can use Tecotype on Windows or Linux after signing in.
- If the person cancels, preserve access through the expiration Apple reports.

Apple and Tecotype operate separate billing systems, so it is not possible to
guarantee a single lifetime trial across both systems without adding
disproportionate friction. The entitlement service should suppress a website
trial for a Tecotype account that already used one. Apple may still consider
the associated Apple Account eligible for its introductory offer. Accept this
limited duplication at launch and measure it before adding controls.

Apple documents free trials as
[introductory offers](https://developer.apple.com/help/app-store-connect/manage-subscriptions/set-up-introductory-offers-for-auto-renewable-subscriptions).
The trial begins through the normal IAP confirmation flow and renews at the
displayed price unless the subscriber cancels.

## One Tecotype account

The Tecotype account is the cross-platform identity. It is separate from both
the person's Apple Account and the email accounts they read in Tecotype.

Use one entry point for registration and sign-in:

```text
Continue with email
Email address
Six-digit code
```

- The person chooses the Tecotype account email. It is not necessarily their
  App Store email, and Tecotype must not assume Apple will disclose one.
- If the address is new, successful verification creates the account. If it
  exists, the same flow signs in. Do not ask people to choose between account
  creation and sign-in.
- Sign in before starting IAP so the completed Apple transaction can be linked
  deterministically to the Tecotype account.
- The account service stores entitlement and device-session data. It must not
  receive mailbox credentials, tokens, message metadata, or message contents.

Apple's login guideline does not require Sign in with Apple when an app
exclusively uses its own account setup and sign-in system. Do not add a social
login only for review compliance.

### Passwordless authentication

Use passwordless email verification rather than passwords:

- Six numeric digits, single use, expiring after ten minutes.
- At most five verification attempts per challenge.
- Resend cooldowns and rate limits by address, IP address, and device signal.
- Store a keyed HMAC of the code using a server-held secret, compare it in
  constant time, and never write the code to logs. A plain hash is insufficient
  for a six-digit value because its entire keyspace is cheap to enumerate.
- Invalidate the previous challenge when a new code is issued.
- Bind a challenge to its purpose and the session that requested it.
- Use a generic response that does not disclose whether the account exists.
- Require fresh verification for a new device, email change, account deletion,
  or other sensitive recovery action.

Do not request a code on every launch. After verification, issue a revocable,
long-lived device session and store its secret using the operating system's
credential protection. Cache a signed, bounded entitlement lease so an
existing session can keep working during a temporary Tecotype or mail-delivery
outage.

A typed code is preferable to a magic-link-only design because Tecotype may not
yet be configured to read the inbox receiving the message. A magic link may be
included as a convenience, but the code must remain available.

Passwords are not a fallback. Passkeys can be added later if account-security
or enterprise requirements justify them.

## Entitlement model

The billing provider collects money. Tecotype's entitlement service decides
whether a signed-in account can use Tecotype across desktop platforms.

At minimum, record:

```text
tecotype_account_id
plan
billing_source: apple | web | support
provider_customer_or_transaction_id
state: trialing | active | grace | expired | revoked
starts_at
expires_at
auto_renews
last_verified_at
```

Do not expose a transferable license key. Clients receive a signed entitlement
for the authenticated Tecotype account and periodically refresh it.

### Apple purchase

1. The Store build authenticates the Tecotype account.
2. It loads the localized monthly and annual products from Apple.
3. It begins the selected purchase with a stable, non-email Tecotype account
   UUID in Electron's `username` purchase option.
4. The client submits the resulting Apple transaction evidence to Tecotype's
   entitlement service.
5. The service verifies Apple-signed transaction data, binds the original
   transaction to exactly one Tecotype account, and returns an entitlement.
6. App Store Server Notifications V2 keep renewal, grace-period, expiration,
   refund, and revocation state current.
7. Periodic reconciliation with the App Store Server API repairs missed
   notifications.

Apple documents that a UUID supplied through the original
`applicationUsername` field is returned as `appAccountToken`, which associates
the transaction with a customer on the developer's service. The account UUID
must not contain the person's email or other identifying information.

Do not build new server validation on Apple's deprecated `verifyReceipt`
endpoint. Electron can initiate Mac App Store purchases and expose transaction
and receipt evidence; the server should use Apple's signed transaction data,
App Store Server API, and Server Notifications V2 as the durable source.

### Restore and account conflicts

Include `Restore purchases` in the Store build.

- If an Apple original transaction is unclaimed, a successful restore can bind
  it to the currently verified Tecotype account.
- If it is already bound, do not silently move it to another account. Ask the
  person to sign in to the existing Tecotype account or use an explicit support
  recovery process.
- The same original transaction must never unlock multiple unrelated Tecotype
  accounts.
- Before offering any checkout, check for an active entitlement from any
  provider to reduce accidental double subscriptions.

### Windows and Linux access

Windows and Linux do not verify an App Store receipt locally. They authenticate
the Tecotype account and request its entitlement from Tecotype's service. The
service has already verified the Apple transaction and continues to receive
subscription changes from Apple.

An Apple purchaser therefore uses:

```text
Apple Account ── pays Apple
       │
Apple transaction ── linked to Tecotype account
                              │
                 macOS, Windows, and Linux
```

No second license or platform-specific purchase is required.

## Subscription management

The billing source owns subscription management:

| Billing source | Management location                        | In-app action                                           |
| -------------- | ------------------------------------------ | ------------------------------------------------------- |
| Apple          | Apple's subscription-management experience | `Manage in App Store`                                   |
| Website        | Tecotype's authenticated billing portal    | `Manage billing`                                        |
| Support grant  | Tecotype support                           | Show the grant and expiration without a purchase action |

Show the source plainly:

```text
Tecotype Individual
Active
Billed by Apple
Renews 19 August 2027

Manage in App Store
```

or:

```text
Tecotype Individual
Active
Billed by Tecotype
Renews 19 August 2027

Manage billing
```

For Apple billing:

- Open Apple's management experience or
  `https://apps.apple.com/account/subscriptions`.
- Tecotype cannot directly cancel, change, refund, or update the payment method
  for an Apple subscription.
- Use the same Apple management link on Windows and Linux.

For website billing:

- Manage payment methods, invoices, cancellation, and plan interval in
  Tecotype's website portal.
- A Store build may link an existing website subscriber to a narrowly scoped
  management portal, but the destination must not become a disguised external
  purchase or upgrade funnel. Re-check this behavior during App Review because
  the multiplatform rule expressly permits access to an external entitlement
  but does not provide a general external-purchase exception.

Do not migrate an active subscription between providers automatically. To move
from Apple to website billing, cancel with Apple, keep access through the
Apple-reported expiration, and subscribe on the website afterward. Apply the
same cancel, expire, then subscribe sequence in the other direction.

If two paid subscriptions nevertheless overlap, show both billing sources and
their management actions. Do not silently combine, extend, or cancel either
one.

## Account deletion

Because the Store build creates Tecotype accounts, it must offer account
deletion in the app.

- Put `Delete account` in account settings.
- Explain which Tecotype account and entitlement records will be removed.
- For an Apple subscriber, warn that deleting the Tecotype account does not
  cancel Apple billing and provide `Manage in App Store`.
- Offer immediate deletion even if a second option schedules deletion for the
  subscription expiration date.
- Keep mailbox deletion behavior separate. Deleting the Tecotype entitlement
  account must not imply that Tecotype can delete mail held by Gmail or an IMAP
  provider.

Apple's
[account-deletion guidance](https://developer.apple.com/support/offering-account-deletion-in-your-app/)
requires in-app initiation and explicitly says Apple billing continues until
the subscriber cancels it.

## Two macOS builds

The Store and direct applications should provide the same mail capabilities but
use different packaging, commerce, and update adapters.

| Concern                 | Direct Mac build                                    | Mac App Store build                                                                        |
| ----------------------- | --------------------------------------------------- | ------------------------------------------------------------------------------------------ |
| Package                 | Developer ID-signed DMG and ZIP                     | MAS package submitted to App Store Connect                                                 |
| Runtime                 | Standard Electron macOS build                       | Electron MAS build                                                                         |
| Sandbox                 | Hardened runtime; App Sandbox not currently enabled | App Sandbox required                                                                       |
| New purchase            | Tecotype website                                    | Apple IAP                                                                                  |
| Existing entitlement    | Tecotype account                                    | Tecotype account                                                                           |
| Updates                 | Tecotype updater                                    | App Store only                                                                             |
| Better search model     | Explicit post-install download                      | Bundle with the Store build unless App Review confirms the existing download is acceptable |
| Subscription management | Provider-specific                                   | Provider-specific                                                                          |

Feature names, mailbox behavior, local data ownership, and entitlement semantics
must remain the same. Conditional behavior should be selected by a signed build
channel constant, not by unreliable runtime guesses.

## Current implementation gap

The verified source state on 2026-07-19 is direct-distribution-only:

- `electron-builder.yml` targets DMG and ZIP, not `mas` or `mas-dev`.
- The existing macOS entitlements enable V8 JIT but do not enable App Sandbox
  or declare Store-specific network and file access.
- The application uses its own macOS updater. That path must be disabled in the
  Store build.
- Electron 43 includes the Mac App Store `inAppPurchase` API, but Tecotype does
  not call it.
- There is no Tecotype account, OTP authentication, entitlement service,
  website billing, Apple server integration, or subscription settings UI.
- Gmail and Fastmail OAuth use a temporary loopback callback server.
- Better search downloads a verified model after installation.

The loopback OAuth server, Gmail and IMAP networking, local database and
credential storage, attachment import/export, native `native_core.node` module,
and optional model download all require explicit sandbox validation.

The model download is also a separate review risk. Guideline 2.4.5(iv) says a
Mac App Store app may not download code or resources that add functionality or
significantly change the reviewed app. Better search is optional, but its
downloaded model enables that capability. The conservative Store build should
bundle the verified model rather than depend on post-install delivery unless
App Review confirms the current design is acceptable.

An App Store listing is conditional on these validations; the direct build
remains the fallback if the sandbox or review rules break a core workflow.

Electron's
[Mac App Store guide](https://www.electronjs.org/docs/latest/tutorial/mac-app-store-submission-guide/)
confirms that Store submissions require the MAS Electron build and App Sandbox.

## Release gate

Before deciding that the Store channel is operational:

1. Produce a signed `mas-dev` build with the final provisioning profile and
   minimum necessary entitlements.
2. On a clean supported Mac, verify Gmail OAuth, Fastmail OAuth, IMAP, SMTP,
   attachment open/save, local credential storage, sync, search, Better search
   model availability and activation, sleep/wake, and relaunch.
3. Verify that the Tecotype updater is absent and cannot run.
4. Test monthly and annual IAP in Apple's sandbox, including purchase,
   cancellation, renewal, billing retry, grace period, expiration, refund,
   revoke, restore, and interrupted transactions.
5. Verify account linking and conflict handling across two Macs, Windows, and
   Linux.
6. Verify offline startup and bounded entitlement refresh behavior.
7. Verify account deletion without implying that it cancels Apple billing.
8. Provide App Review with a working review account or full demo mode and
   explain the existing-web-entitlement flow in Review Notes.
9. Release to the Store only after the Store build passes the same mail
   regression coverage as the direct build.
10. Measure the Store as its own first-touch-to-paid funnel rather than claiming
    discovery or distribution value before evidence exists.

## Economics

Enroll in the
[App Store Small Business Program](https://developer.apple.com/app-store/small-business-program/)
if eligible. Apple currently states a 15% commission for qualifying developers
with up to USD 1 million in proceeds. Outside that program, Apple states that
the developer receives 70% of an auto-renewable subscription price during a
subscriber's first paid year and 85% after one year, in both cases minus
applicable taxes. Free-trial days do not count toward the paid year.

Use the same Individual plan and comparable customer-facing price across
billing systems. Apple controls storefront localization, tax treatment, and
available price points for IAP. Compare actual proceeds rather than multiplying
the displayed euro price by a commission percentage.

The commission buys Apple payment processing, subscription management,
refund handling, Store delivery, and the customer's familiar purchase
experience. It does not buy guaranteed discovery.

## Primary sources

- [App Review Guidelines](https://developer.apple.com/app-store/review/guidelines/),
  especially 2.4.5, 3.1.1, 3.1.2, 3.1.3, 4.8, and 5.1.1.
- [Auto-renewable subscriptions](https://developer.apple.com/app-store/subscriptions/).
- [Introductory offers](https://developer.apple.com/help/app-store-connect/manage-subscriptions/set-up-introductory-offers-for-auto-renewable-subscriptions).
- [App Store Server API](https://developer.apple.com/documentation/appstoreserverapi).
- [App Store Server Notifications](https://developer.apple.com/documentation/appstoreservernotifications).
- [Apple account deletion guidance](https://developer.apple.com/support/offering-account-deletion-in-your-app/).
- [Electron Mac App Store submission](https://www.electronjs.org/docs/latest/tutorial/mac-app-store-submission-guide/).
- [Electron in-app purchase API](https://www.electronjs.org/docs/latest/api/in-app-purchase).
