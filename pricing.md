# Tecotype pricing

Status: Pricing decision

Last reviewed: 2026-07-19

## Individual plan

Tecotype Individual costs:

- €15 per month.
- €149 per year.

The annual plan is the primary offer. The monthly plan provides a
lower-commitment alternative without changing the product or feature set.

Public pricing should lead with the complete annual price:

```text
€149 per year
or €15 per month
```

Do not lead with an annualized monthly equivalent such as "€12.42 per month,
billed annually." The customer should be able to see the actual commitment
without doing additional arithmetic.

## Positioning role

The price positions Tecotype as a serious professional tool rather than a
general-purpose free email client or an enterprise productivity suite.

The value comes from the combined experience:

- Calm control over mail.
- Fast keyboard-driven operation.
- Gmail and IMAP accounts in one client.
- Local search and optional on-device Better search.
- Precise organization through Split Inboxes and reminders.

Pricing copy should use these concrete product qualities as proof. It should not
justify the price with unverified time-saved claims, feature quantity, artificial
urgency, or technology-first language.

## Current market comparison

These are public US prices checked on 2026-07-19. They are market context, not
evidence that Tecotype's price will convert. App Store prices can vary by
region, promotion, and retained legacy purchase product.

| Product                                                                                       |                  Current annual price or nearest equivalent | Purchase and distribution context                                                                                                                |
| --------------------------------------------------------------------------------------------- | ----------------------------------------------------------: | ------------------------------------------------------------------------------------------------------------------------------------------------ |
| [Canary Mail](https://canarymail.io/pricing)                                                  |                                       Growth $36; Pro+ $100 | Native Mac App Store client with Apple in-app purchase; also covers other supported platforms                                                    |
| [Airmail](https://apps.apple.com/us/app/airmail-lightning-fast-email/id918858936?mt=12)       |                                                  Pro $49.99 | Native Mac App Store client with Apple in-app purchase; optional AI Composer is listed separately at $14.99/month                                |
| [Mailbird](https://apps.apple.com/us/app/mailbird-the-email-app/id6749447444?mt=12)           |                                $34.49/year or $159 one-time | Native Mac App Store client with Apple in-app purchase                                                                                           |
| [Spark](https://sparkmailapp.com/help/billing-subscription/understanding-spark-billing)       |                                          Plus $99; Pro $199 | Native Mac App Store client with Apple in-app purchase; paid access is cross-platform                                                            |
| [Microsoft Outlook](https://apps.apple.com/us/app/microsoft-outlook/id985367838?mt=12)        |               Microsoft 365 Personal $99.99; Family $129.99 | Native Mac App Store client with Apple in-app purchase; the core personal-account client is free and the paid product is a broader suite         |
| [Spike](https://apps.apple.com/us/app/spike-ai-email-team-chat/id707452888)                   |                                Pro $71.99; Ultimate $143.99 | Mac-capable App Store client with Apple in-app purchase; broader team and hosted-service features make it less directly comparable               |
| [Superhuman Mail](https://help.superhuman.com/hc/en-us/articles/46178817646861-Pricing-Plans) |                                 Starter $300; Business $396 | Externally billed premium email service; its full desktop app is distributed directly rather than through the Mac App Store                      |
| [Polymail](https://help.polymail.io/help/polymail-premium-email-tool)                         |                                                Premium $288 | Externally billed account service; its Apple Store listing is an iPad app that can run on Apple-silicon Macs, not a native Mac App Store release |
| [Missive](https://missiveapp.com/pricing)                                                     |       Starter $168; Productive $288; Business $432 per user | Externally billed web and desktop team-email service                                                                                             |
| [Front](https://front.com/pricing)                                                            | Starter $300; Professional $780; Enterprise $1,260 per seat | Externally billed customer-operations and shared-inbox platform, not a personal local email client                                               |

The closest native Mac App Store comparison set is Canary, Airmail, Mailbird,
Spark, Outlook, and Spike. Every paid member of that set exposes Apple in-app
purchase. This establishes in-app purchase as a normal Store expectation, not
evidence that the Store will discover or convert Tecotype.

Within that set, most annual offers fall between roughly $35 and $144. Spark Pro
at $199 is the clear recurring-plan exception. Prices above $150 are established
more broadly, but concentrate in AI-heavy, sales, collaboration, and shared-inbox
services: Superhuman, Polymail Premium, Missive, and Front. Their prices do not
by themselves validate €149/year for a local-first individual client.

## Purchase channels

Tecotype sells the Individual plan through two independent channels:

| Purchase | Included applications |
| --- | --- |
| Mac App Store | Mac App Store build on macOS only |
| Tecotype website | Direct macOS, Windows, and Linux builds |

Both use the same €15 monthly and €149 annual base price. The mail capabilities
on macOS should remain equivalent, but a purchase from one channel does not
unlock the other:

- Website customers on Mac install the direct build.
- App Store customers use the Store build.
- Do not connect Apple purchases to Windows or Linux through a Tecotype
  entitlement service.
- State the platform scope before purchase. Use `Mac subscription` in the Store
  and `Desktop subscription: Mac, Windows, and Linux` on the website.

This split preserves App Store trust without requiring Apple and Tecotype
billing to share accounts, trials, subscription state, or cross-platform
entitlements.

## Plan structure

The monthly and annual options are billing intervals for the same Individual
plan within each purchase channel. The billing interval does not change the
product or feature set.

Do not create feature differences between the monthly and annual options. The
annual option earns preference through its lower total price, not by withholding
product capability from monthly customers. The channel-specific platform
licence is a distribution boundary, not an annual-versus-monthly feature tier.

## Trial

The working launch offer is one free month followed by the selected monthly or
annual subscription:

- Use the same ordinary trial length and capabilities for Apple and website
  checkout.
- In the Mac App Store, configure a free one-month introductory offer for both
  products in the same subscription group.
- Say `One month free`, not `30 days free`; Apple's one-month introductory
  period can contain 28 to 31 days.
- Use a payment-authorized trial. Apple handles authorization for IAP; website
  checkout collects a payment method before its trial starts.
- Show the full renewal price and interval before confirmation.
- Show whether the trial covers the Mac App Store build or the three direct
  desktop builds.

Apple and website trial eligibility are independent. Do not build identity
matching between the channels merely to prevent a person from evaluating both
editions.

For a Store affiliate experiment, a creator-specific paid offer code may reduce
the first annual period to €99, or the selected localized equivalent. That
pay-up-front offer replaces the free month, then renews at the ordinary annual
price unless cancelled. It is an acquisition experiment, not the public base
price.

The complete channel, offer-code, trial, and subscription-management decision
is in [Mac App Store distribution](./mac-app-store-distribution.md).

## Business billing

The website is the business-billing route, even when the buyer needs only one
Individual subscription:

- Website checkout should accept company name, billing address, and VAT number
  where applicable.
- The payment and tax provider should issue the corresponding Tecotype invoice.
- The Mac App Store purchaser receives Apple's receipt. Tecotype cannot add
  company or VAT fields to Apple's individual in-app purchase checkout.
- Apple Business does not turn the Individual in-app subscription into a
  centrally purchased or assigned business licence.

Team seats, purchase orders, and enterprise contracts remain undecided. Do not
imply that the Individual website checkout already provides them.

## Future market extension

[Front](https://front.com/), [Missive](https://missiveapp.com/), and
[Help Scout](https://www.helpscout.com/) establish a higher-value adjacent
market around shared inboxes, support automation, internal collaboration,
routing, and customer operations.

That market is a possible extension after Tecotype proves the individual
client. It is not part of the current €149 Individual promise and must not be
used to rationalize today's price. A future team product would need its own
customer evidence, pricing, server and privacy architecture, and acquisition
plan.

## Presentation principles

- Show the annual option first.
- State the annual total directly.
- Keep the monthly option visible as a straightforward alternative.
- Use euros as the canonical price in public positioning.
- Keep pricing visually restrained, with one plan and no comparison-table
  theatre.
- Do not use crossed-out prices, countdowns, or false scarcity.

## Decisions not made here

This document does not decide:

- Whether Tecotype will have a permanent free plan.
- Team, support-operations, business, education, or regional pricing.
- Refund and cancellation policy.

Billing, Store distribution, and direct desktop licensing are decisions, not
shipped functionality. See
[Mac App Store distribution](./mac-app-store-distribution.md).

Those decisions should be recorded when they are made rather than inferred from
the Individual price.
