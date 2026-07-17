# Landing-page research

Current URL: `https://tatem.com/`

Captured: **2026-07-17**

Context: **rendered desktop page, logged out**

Historical comparison: **August 2023 through 2024 email-waitlist pages**

The current page is still reachable, but it is a residual acquisition asset: Tatem’s changelog ends in September 2025 and its team joined Wander the following month. The historical pages are more useful for understanding what Tatem tried and changed.

## What changed

| Element | 2023–2024 email page | Current page | Interpretation |
| --- | --- | --- | --- |
| Offer | Request access / join the waitlist | “Get started” to Google signup | Controlled demand capture was replaced by self-serve access |
| Hero | “Intelligent,” then “Smart email built for speed” | “The email experience you’ve been waiting for” | Category-transformation language replaced a functional headline |
| Outcome | “Save 3 hours each week” | “Save hours each week” in metadata/closing copy | The prominent numeric claim was softened |
| Descriptor | Fast, intelligent, and beautiful | “Fast, beautiful, simple” | Intelligence/AI was removed from the three-part promise |
| AI | Tatem AI, autopilot, intelligent replies, and writing in the user’s voice | No prominent AI-companion section | The prominent AI message disappeared; feature status and performance are unknown |
| Core mechanisms | Split inbox, speed, search, keyboard shortcuts, editor, personalization, design, and security | Split inbox, speed, keyboard shortcuts, editor, design, and security remain; search is not a current homepage section | Speed, workflow, and visual experience were the durable position |
| Proof | Product demonstrations and claims | “Join 10,000+” plus demonstrations and claims | Aggregate social proof was added, but the population is undefined |
| CTA friction | Email form, wait, then controlled access | Separate app signup with Google | The public first step became immediate but still requires Google authorization |

Sources: [August 2023 archive](https://web.archive.org/web/20230808074401/https://tatem.com/), [November 2023 archive](https://web.archive.org/web/20231128162308/https://tatem.com/), [July 2024 archive](https://web.archive.org/web/20240704125059/https://tatem.com/), [pre-rebuild Webflow page](https://tatem.webflow.io/), and [current homepage](https://tatem.com/).

The changes are observed; their causes are not. Removed copy is not evidence that the message or feature failed.

## Current page

### Observed message and offer

| Page element | Copy or behavior |
| --- | --- |
| Status | “Now in early access.” |
| Social proof | “Join 10,000+ rethinking their email.” |
| Hero | “The email experience you’ve been waiting for.” |
| Descriptor | “Fast, beautiful, simple.” |
| CTA | “Get started” |
| CTA destination | `https://app.tatem.com/sign-up` |
| Split inbox | Prioritize important messages and focus on what matters |
| Speed | Claimed interactions below 50 ms |
| Editor | Docs-like formatting and faster writing |
| Keyboard | Shortcuts and command menu |
| Design | Minimal, customizable, and visually polished |
| Security | Claims that email, passwords, and payment information are not stored in Tatem’s database |
| Homepage lead form | None |
| Visible homepage price | None |

The page does not specify a profession, company size, operating system, migration path, or time to first value. It also does not explain the free plan or Google permissions beside the CTA.

The “10,000+” count is a first-party claim. A [Tatem careers page](https://tatem.com/careers/senior-fullstack-software-engineer/501f8a) previously called it organic signups, but no public source defines the product era, activity, or conversion represented by the number. It must not be treated as 10,000 active email users.

### Metadata

| Field | Current value |
| --- | --- |
| Title | `Experience email at its best - Tatem` |
| Description | `Make productivity your superpower. Get through your work faster and save hours each week.` |
| Canonical | `https://tatem.com` |
| Language | `en` |
| Robots | `index, follow` |
| Open Graph / Twitter | Branded title, description, and 1200 × 630 dynamic image |
| JSON-LD | None found |
| `hreflang` | None found |

The title says email but not “email client,” Gmail, browser, desktop, or a customer role. The description does not mention email. This makes the page broadly shareable but not strongly aligned with a specific non-brand query. It is a plausible relevance limitation, not a proven cause of the current rankings in [traffic.md](./traffic.md).

### Measurement and technology

| Surface | Observed evidence | Boundary |
| --- | --- | --- |
| Homepage | Google Analytics 4, measurement ID `G-58FCZEQWJ4` | Proves a tag is installed, not that useful acquisition events exist |
| Homepage | Next.js and Sanity | Describes the public site stack, not channel performance |
| Homepage | Plain signup URLs; no source parameter | The homepage link itself does not preserve visible source attribution |
| Signup page | A visible “Continue with Google” action | Establishes the first public account step only |
| Signup scripts | Segment-hosted Amplitude integration code | Shows app-side analytics capability, not specific events or data quality |
| 2023 archived email page | Google Analytics and Hotjar | Historical instrumentation, not current behavior |
| 2022 operations page | FullStory | Belongs to the earlier product era |

No visible current homepage signatures were found for Meta, LinkedIn, or Reddit ad pixels; Google Tag Manager; Mixpanel; PostHog; Hotjar; FullStory; Clarity; HubSpot; Intercom; Optimizely; or VWO. This is an observed absence from one rendered visit, not proof that Tatem never used them or had no server-side or bundled measurement.

## Customer and positioning hypothesis

**Observed:** The page emphasizes fast interaction, keyboard use, split inboxes, writing, visual polish, and security.

**Inferred:** The likely customer is an email-heavy, product-aware knowledge worker who values speed and good design. Small teams are a secondary possibility because the pricing and changelog mention workspaces and team billing, but the homepage does not lead with a team job.

**Unobservable:** Which audience actually signed up, activated, retained, or paid.

The durable positioning can be reconstructed as:

> A fast, visually polished email experience for people who want to move through work with less friction.

This is an inference, not Tatem’s own positioning statement.

The current angle ranks as:

1. Speed and productivity.
2. Aesthetic delight and modernity.
3. Focus and control.
4. Security reassurance.

Privacy is supporting proof, not the leading acquisition promise. Calm is not established as Tatem’s or Tecotype’s winning message; it remains one Tecotype hypothesis to test.

## What this tells us about acquisition

- Tatem kept speed, keyboard workflow, split inboxes, design, and security across major product changes. These are durable message themes, not proven acquisition winners.
- Tatem was featured on dedicated design-gallery pages. That proves placement, not why it was selected or whether qualified people visited.
- The move from a waitlist to direct signup removed visible access friction.
- The generic hero and metadata do not show a deliberate non-brand SEO landing-page program.
- The current CTA hides important offer and permission information until later. Tecotype should make its own platform, availability, next step, and relevant permissions explicit when its acquisition surface exists.

See [history.md](./history.md) for the full sequence and [funnel.md](./funnel.md) for each offer.
