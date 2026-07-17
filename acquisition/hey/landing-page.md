# HEY landing page

Captured **2026-07-17** from
[https://www.hey.com/](https://www.hey.com/) in a rendered desktop browser.
The page appeared current: it included HEY Calendar, the current 30-day trial,
and current pricing links.

## Message

The rendered lead was:

> We finally fixed your email + calendar!

The page then argues that Gmail, Outlook, Yahoo, and Apple let email decline,
before presenting HEY as a complete rethinking. Its own current social proof is
that [“tens of thousands” have switched](https://www.hey.com/), followed by
testimonials and product demonstrations.

| Question | Evidence | Assessment |
| --- | --- | --- |
| Who is it for? | Individuals willing to replace their provider, plus custom-domain teams and families on separate offers | **Observed**, with willingness to switch inferred |
| Trigger | Unwanted senders, mixed email types, tracking, notifications, and the obligation of inbox zero | **Observed** |
| Promise | A fresh email and calendar service that restores control and pleasure | **Observed** |
| Mechanism | Screener, Imbox, Feed, Paper Trail, Reply Later, selective notifications, tracking protection, and integrated calendar | **Observed** |
| Emotional angle | Control, independence, privacy, delight, and relief from obligation | **Observed** |
| Proof | Named mechanisms, images, a 37-minute walkthrough, testimonials, founder explanation, and an undefined switch count | **Observed**; outcome proof is limited |
| Offer | 30 days free without a card; $99/year afterward | **Observed** |
| Requested action | “Try HEY free,” leading to `https://app.hey.com/sign_up` | **Observed** |

The [HEY Way](https://www.hey.com/the-hey-way/) is a manifesto rather than a
feature list. It rejects inbox zero, universal sender access, unread counts,
notifications by default, advertising, and cloud-provider complacency. It also
explicitly says “HI not AI.” That gives the product a legible enemy and a
coherent philosophy, but it also narrows the audience to people willing to
adopt HEY's rules.

## Demonstration and education

The [How HEY works](https://www.hey.com/how-it-works/) page names the operating
model before asking for commitment. It includes:

- a **37-minute** founder-led walkthrough;
- the first-sender Yes/No decision;
- the Imbox, Feed, and Paper Trail;
- Reply Later and Focus & Reply; and
- explanatory images for the workflows.

This is useful conversion material because the product is intentionally
unfamiliar. It reduces conceptual uncertainty, although it cannot prove that a
specific user will prefer the behavior after switching.

## Technical evidence

Rendered-page inspection found:

- title: `HEY — A delightfully fresh take on email + calendar, from 37signals`;
- canonical homepage URL: `https://www.hey.com/`;
- primary CTAs to `https://app.hey.com/sign_up`;
- a module script at `/assets/js/script.js?v=1.0.1`;
- a same-origin Plausible script at `/js/script.outbound-links.js` with
  `data-domain="www.hey.com"`; and
- a newsletter form posting to Mailchimp.

The public tracking helper emits a Plausible `signup_start` event for elements
marked `data-track-signup`. It also carries public source parameters such as
`source`, `utm`, `ref`, `referrer`, and `utm_source` into signup destinations.
That proves landing-to-signup measurement capability. It does not prove that
HEY connects those identifiers to activation, payment, or renewal.

No Google, Meta, Hotjar, or session-replay marker was observed in the rendered
homepage. No consent dialog was visible in the captured session. Either absence
could be conditional on geography, consent, browser state, server-side
instrumentation, or later changes.

## Claim discipline

The page's strongest numerical statements need separate interpretations:

- “Tens of thousands” is a first-party switch claim without date or cohort
  definition.
- “More than 150,000” refers to the 37signals/HEY newsletter audience, not
  HEY users.
- Testimonials establish that named people expressed enthusiasm, not the
  conversion or retention rate of their audiences.
- Platform availability on Web, Mac, Windows, Linux, iOS, and Android is a
  first-party distribution claim. This research did not obtain or test any app.

## What Tecotype can learn

HEY makes abstract positioning testable through product nouns: Screener,
Imbox, Feed, Paper Trail, and Reply Later. Tecotype should likewise show a
shipped mechanism, such as a real cross-language search result or a complete
keyboard triage sequence, rather than leading with a list of qualities.

The tone should not be copied. HEY uses conflict, superlatives, and categorical
claims. Tecotype's position is calm control, so a quieter demonstration with
precise limitations would be more credible and more consistent.
