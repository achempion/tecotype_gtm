# Airo Mail landing-page research

Captured: **2026-07-17**

URL: [https://www.airo.email/](https://www.airo.email/)

Two public states were observed. The initially captured/indexed HTML exposed a
solo-founder message, Plate, a no-sign-in demo, and a founder-oriented offer. A
later direct current fetch of the same URL exposed a mobile-consumer message,
AutoFile, Agenda, packages, trips, unified inbox, Personal/Pro/Business tiers,
and no visible demo text. Both were server-rendered enough to inspect without
interaction.

The difference may reflect a rapid deployment, cache, geography, conditional
delivery, or an experiment. No evidence establishes which is canonical or how
visitors are assigned. A live interactive session was unavailable, so motion,
cookie state, pricing toggles, and the demo were not exercised.

## Metadata and technical surface

| Field | Observed value |
| --- | --- |
| Captured/indexed title | `Airo Mail - The Email App That Files, Tracks, and Follows Up \| Airo \| Airo Mail` |
| Direct-fetch title | `Airo Mail - AI-Powered Email App for iPhone & Android \| Airo \| Airo Mail` |
| Shared description themes | AI organization, AutoFile suggestions, 14-day trial, iOS, Android, and web |
| Canonical | `https://www.airo.email` |
| Language | English |
| Robots | `index, follow` with extended Google preview directives |
| Open Graph / X | 1200×630 image; `@charles_at_airo` as site and creator |
| Framework | Next.js with Nextra-style content routing; Vercel identified in backlink metadata |
| Consent | CookieYes script present |

The pages contain Product and FAQ structured data. The direct annual state
showed Personal at $8/month and Pro at $25/month billed annually, plus Business
custom. Captured structured offer data included a $30 Pro price, consistent
with a possible monthly state but not manually toggled.

## Measurement capability

The initial HTML exposed:

- Google Analytics `G-444ECLB9MY`;
- Google Tag Manager `GTM-NXT2NSM7`;
- a `PostHogProvider` bundle; and
- components named `CookieGatedAnalytics` behind CookieYes.

This demonstrates a mature measurement surface for an early product. It does
not show which events are configured, whether consent was granted, whether
server-side events exist, or whether original source survives to payment.

## Captured founder-variant message map

| Question | Evidence | Classification |
| --- | --- | --- |
| Who is it for? | “Superpowered email for solo founders” | **Observed in one captured/indexed variant** |
| Trigger | One person handles customer, lead, investor, sales, support, and company mail | **Observed** |
| Promise | Every important email arrives with the next reply, task, or follow-up surfaced | **Observed** |
| Mechanism | Plate surfaces actions; AutoFile proposes actions for the rest | **Observed publisher claim** |
| Emotional angle | Nothing important falls through; founder gets back to building | **Observed** |
| Proof | Detailed simulated inbox, founder story, CASA claim, no-ads/data-sales claims | **Observed claims** |
| Offer | No-sign-in demo; 14 days free; no card; professional and team routes | **Observed in that variant** |
| Primary action | `Get started` to `app.airo.email` | **Observed destination, not followed** |
| Secondary action | `Try the live demo · no sign-in` to `demo.airo.email` | **Observed in that variant; destination not followed** |

The copy is unusually specific about the founder’s inbox: customers, leads,
investors, duplicate invoices, statements, login codes, and design follow-ups.
It makes a professional offer easier to understand than a generic AI feature
list would.

## Direct mobile-consumer variant

The later direct fetch led with:

> Email That Organizes Itself

Its supporting copy says Airo files messages, tracks packages, and builds a
daily agenda automatically. It presents:

- AutoFile;
- Agenda and open-loop tracking;
- natural-language search;
- package and trip extraction;
- multi-account Gmail;
- bulk unsubscribe;
- a web-app route;
- a 14-day no-card trial;
- Personal at $8/month billed annually;
- Pro at $25/month billed annually; and
- Business at a custom price.

No live-demo text was visible in this fetched state. It is broader and more
consumer/mobile-oriented than the founder variant while sharing the core
AutoFile/control mechanism.

## Demonstration architecture

The captured founder variant demonstrates two modes:

- **Plate:** shows a filtered queue and an explicit next action under each
  thread; and
- **AutoFile:** proposes archive, trash, star, or read actions in a batch that
  the user can approve or override.

This gives that variant's visitor a concrete model before the CTA. The
separate live-demo link appears to lower evaluation friction further, but it
was not opened or interacted with and was not visible in the later direct
fetch.

## Founder narrative

On [Our Story](https://www.airo.email/our_story), Charles Guo says he spent ten
years at Google and Airbnb, worked on G Suite, and spent almost two years on
Airo. He connects the product to repetitive filing decisions, family ADHD,
his own likely ADHD, and a “Guitar Hero” review interaction.

This story is memorable and explains the mechanism. It intersects differently
with the mobile-consumer and solo-founder variants, so a visitor may understand
“who it is for” differently depending on the public state served.

## Trust and privacy positioning

The homepage says:

- no ads and no data sales;
- encryption in transit and at rest;
- CASA Tier 2 certification;
- AI vendors do not train on the data; and
- most Gmail data stays on the device.

The more precise [Security & Data Handling](https://www.airo.email/security)
page says Airo’s backend fetches and stores message bodies while the account is
active, generates embeddings, and runs classification through Google Vertex
AI. It explicitly says Airo is not end-to-end encrypted.

The security page is a strong trust asset because it names retention,
subprocessors, access controls, and deletion behavior. The homepage phrase
“most Gmail data stays on your device” is difficult to reconcile at a glance
with active server-side message storage and should be read with the detailed
page, not as a local-only claim.

## Public variant and offer inconsistencies

- Direct homepage: mobile-consumer framing; Personal $8/month and Pro
  $25/month billed annually; Business custom; no visible live demo.
- Captured/indexed homepage: solo-founder framing, Plate, and a no-sign-in
  demo.
- Captured structured offer: $30 Pro, likely monthly but not toggled.
- US App Store: $9.99 Personal and $29.99 Pro monthly, with $96 and $300 annual
  in-app purchases.

Channel, caching, experiment assignment, or timing may explain the variation.
They can still create audience, demo, and price uncertainty during evaluation.

## What remains unobservable

- Actual visitor segment and traffic source.
- Which visitor receives which homepage state and why.
- Cookie acceptance and event firing.
- Live-demo visibility, starts, and completion.
- CTA clicks, trials, Gmail connection, first Plate/AutoFile value, payment,
  and renewal.
- Whether the high-price message improves qualification or suppresses demand.

Technical request boundaries are in [requests.md](./requests.md).
