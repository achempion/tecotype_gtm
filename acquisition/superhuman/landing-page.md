# Superhuman Mail landing-page evidence

Research date: **2026-07-17**

Primary URL: [Superhuman Mail](https://superhuman.com/products/mail)

Market: **US-English public web**

## Inspection mode and boundary

The current public HTML, metadata, linked public scripts, public search
extracts, unauthenticated page responses, and rendered DOM were inspected. The
live page was rendered in the in-app browser to verify its visible headline,
section sequence, repeated `Get Started` controls, Pricing route, footer
Download route, and loaded script hosts. Responsive variants, animation,
post-click behavior, and consent-gated or regional behavior remain unverified.

No Superhuman client, browser extension, installer, or app package was
downloaded, opened, installed, or inspected. No form was submitted and no
account, OAuth grant, trial, or checkout was started.

## Current page

| Field | Observed value |
| --- | --- |
| Title | `Superhuman Mail | The most productive email app ever made` |
| Description | `Collaborate faster and get more done with AI-native email. Save 4 hours every week with Superhuman Mail` |
| Canonical | `https://superhuman.com/products/mail` |
| Language | `en-US` |
| Generator | Framer |
| HTML publication marker | Published and optimized **2026-07-10**; this is a build marker, not proof the page or message first appeared then |
| Primary hero | “Save 4 hours every week with Superhuman Mail” |
| Supporting copy | “Superhuman Mail is the most productive email app ever made. Collaborate faster and get more done with AI-native email.” |
| Primary CTA | `Get Started` |
| Other visible routes | Pricing, Love, Talk to Sales where present, and Download in the footer |

The text is also visible in the current
[public page response](https://superhuman.com/products/mail). The separate
[professional-email page](https://superhuman.com/email) uses “Write
professional email replies in seconds” and a `Get Started for Free` CTA. That
difference matters: it shows multiple acquisition pages and does not establish
a universal free Mail trial.

## Audience and positioning

| Question | Evidence | Assessment |
| --- | --- | --- |
| Who is it for? | “High-performing teams,” professionals, managers, sales and customer-facing roles, and people for whom responsiveness affects outcomes | **Observed** on Mail and pricing pages |
| What creates demand? | Late replies, blocked teams, missed deals or goals, high email volume, and a sense that email consumes the day | **Observed** problem framing |
| What is promised? | Four hours saved each week, twice-as-fast processing, faster replies, and fewer dropped responsibilities | **Observed first-party claims**; methodology was not independently audited |
| Why this product? | Keyboard speed, Split Inbox, reminders, AI writing/search/automation, calendar, CRM, and team collaboration | **Observed mechanism** |
| Emotional angle | Performance, mastery, responsiveness, achievement, and the status of being ahead | **Inferred from repeated copy and proof** |
| Proof | Customer quotations and logos, quantified time/response claims, feature demonstrations, and a first-party claim that teams save more than 15 million hours annually | **Observed first-party proof**; customer and study definitions are not public on this page |
| Requested action | Start signup, inspect pricing, or talk to sales | **Observed** |

The page contains some relief language, but its dominant contract is
performance: move faster, stay responsive, and achieve more. That is close to
Tecotype in keyboard efficiency but different from Tecotype's intended
equanimity—calm, clarity, and control without status pressure.

## Message architecture

The current page follows a consistent sequence:

```text
Quantified outcome: save four hours each week
→ category claim: most productive email app
→ costly email failures: late replies and blocked work
→ mechanisms: speed, AI, collaboration, calendar, sales workflows
→ customer and team proof
→ repeated Get Started CTA
```

The strongest aspect is continuity. The same productivity outcome appears in
the title, description, hero, feature sections, current Product Hunt listing,
pricing, and public professional-email page. The weakness is evidentiary:
“twice as fast,” “12 hours faster,” “2x emails responded to,” and “4+ hours”
are Superhuman's claims, not measurements reproduced by this research.

## Public CTA and attribution behavior

The public `Get Started` component routes to `/signup`. Its script preserves a
broad set of acquisition fields, including:

- UTM source, medium, campaign, term, creative, and content;
- `gclid`, `fbclid`, and `msclkid`;
- campaign and ad identifiers;
- Impact fields such as `irpid` and `irgwc`;
- Dub identifiers;
- promo codes; and
- referral email and referral-code fields.

The component also emits a `link_click` event. This is strong evidence that the
site is designed to carry source context into signup. It is not evidence that
the fields are complete downstream, that reporting is accurate, or that any
particular source converts.

The public page code also contained a LaunchDarkly experiment named
`external-checkout-redesign-experiment`. On `/products/mail`, the test can
route qualifying non-paid traffic to `/mail` while preserving the query string
and referrer. The code distinguishes paid traffic using UTMs, referrers,
`msclkid`, Impact fields, and promo codes. This indicates active landing-path
experimentation rather than one static funnel.

## Publicly visible measurement technology

| Technology | Public identifier or behavior | What it supports | What it does not prove |
| --- | --- | --- | --- |
| Google Tag Manager | `GTM-PF3NX8X` | Central tag management | Which tags fire after consent or produce useful attribution |
| LaunchDarkly | Checkout/landing experiment flag | A/B or rollout control | Experiment exposure, allocation, or outcome |
| Dub | Public analytics script and `dub_id` handling | Link and campaign attribution | Referral volume or conversion |
| Reddit | Pixel `a2_hchvudzz7lmg`, `PageVisit` event | Reddit measurement/retargeting capability | Current spend or return |
| LinkedIn Insight | Partner ID `3213932` | LinkedIn measurement/retargeting capability | Active campaigns or return |
| Impact.com | UTT ID `A6052161-35a5-43f1-815e-1b952086565a1` and Impact parameters | Partner/affiliate attribution capability | Which partners are active or productive |
| Podscribe | Advertiser `superhumanmail` | Podcast attribution capability | Which shows ran, spend, or conversions |
| G2 | Attribution conversion ID `1007433` | Review/directory attribution capability | Incremental acquisition |
| First-party metrics | Writes to `mail.superhuman.com/~backend/v3/metrics.write` | Site event collection | Event definitions, completeness, or retention linkage |
| Transcend | Cookie Preferences control | Consent-choice interface | Rendered consent state in this capture |

The HTML also creates an anonymous first-party `web-device` cookie with a
one-year lifetime. Facebook administration metadata was present, but the
static Mail page did not provide enough evidence to report an active Meta pixel.
The rendered US-English page exposed script hosts associated with Google,
LinkedIn, Meta, Taboola, Impact, Reddit, Dub, G2, Pardot, Framer, and
Superhuman-controlled collection. This verifies delivery of those page
elements, not that each integration emitted data or represented an active
campaign. No visible cookie-choice control appeared in that rendered state.
Server-side, consent-gated, regional, or later-loaded measurement remains
possible.

## Platform and claim boundaries

The [public professional-email page](https://superhuman.com/email) says Mail is
available on the web through a Chrome extension, through native Mac and
Windows apps, and on iOS and Android. The 2024
[platform announcement](https://blog.superhuman.com/superhuman-now-works-wherever-you-do/)
describes the same Gmail/Outlook and device matrix. These are first-party
availability statements only; this research did not obtain or test any client.

The same page says user data is not used to train AI models unless explicit
consent is given and cites SOC 2 Type 2 and GDPR. Those statements were
recorded, not independently audited. Current public scripts also show extensive
marketing measurement, so product-content handling and website-acquisition
tracking should be evaluated as distinct data paths.

## Landing-page conclusion

Superhuman has a mature conversion surface: one quantified promise, repeated
proof, team-specific mechanisms, source-preserving CTAs, several attribution
vendors, and a visible landing-path experiment. The page strongly supports the
hypothesis that paid, partner, review, podcast, and referral channels are
measured. It cannot show which channel is efficient or whether the current
signup reaches activated, retained Mail use.
