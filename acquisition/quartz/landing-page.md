# Landing-page research

Current URL: `https://www.quartzmail.ai/`

Captured: **2026-07-17**

Context: **rendered desktop page, logged out**

Capture geography: **uncontrolled browser egress; no location override**

Historical comparison: **May 23 private beta and June 17 public launch**

## Current page

### Observed message and offer

| Page element | Copy or behavior |
| --- | --- |
| Status | “MAC · GMAIL — PUBLIC BETA” |
| Hero | “Email built for focus, powered by local AI.” |
| Supporting copy | Important messages get room, AI drafts sound like the user, and mail is not shared with AI providers |
| Primary CTA | “Download Quartz for Mac” |
| CTA destination | `/download`, a 307 redirect to a public Apple Silicon `.dmg` |
| Secondary CTA | “Watch the demo,” opening an embedded YouTube Privacy-Enhanced Mode video |
| Focus mechanism | Five learned importance levels: Important, Inbox, FYI, Icebox, and Noise |
| Privacy mechanism | Local classification and drafting on Apple Silicon |
| Proof | CASA Tier 2 claim, product screenshots, 48-second demo, and Product Hunt badge |
| Offer | “Quartz is free for beta users” |
| Homepage form | None |
| Visible price or future price | None |
| Supported provider | Gmail |
| Visible platform | Mac; Apple Silicon is stated in the privacy section |

The page asks for a direct download rather than an account, email address, demo
booking, or checkout. It does not state the 15.6 MB installer size, the model
download described by a maker as roughly 4 GB, the referenced model file's
4,977,171,584-byte size, a macOS minimum version, or the mandatory beta
analytics described in the privacy policy.

### Customer and positioning hypothesis

**Observed:** The page emphasizes protecting focus, reducing inbox noise,
private on-device classification, and drafts that imitate the user's voice.

**Inferred:** The likely customer is an email-heavy Apple Silicon Mac user with
a Gmail account who receives enough low-value mail to accept automated
importance sorting. The page's examples and language suggest a professional or
founder rather than a casual consumer, but no role is named.

**Unobservable:** Which audience downloads, connects Gmail, reaches first value,
keeps using Quartz, or would pay.

The current message hierarchy is:

1. Focus and protection of attention.
2. Local AI as the mechanism and privacy proof.
3. Personalized drafting.
4. Security certification and encrypted local storage.

This overlaps with Tecotype's focus and local-processing territory, but the
products lead differently. Quartz leads with automated categorization and
drafting. Tecotype can currently substantiate keyboard operation, Gmail plus
generic IMAP, local lexical search, optional on-device Better search, Split
Inboxes, and reminders. It should not imply that it ships Quartz-like drafting
or automatic importance classification.

## Metadata and indexability

| Field | Current value |
| --- | --- |
| Title | `Quartz | AI-native email` |
| Description | Important messages get room, AI drafts sound like the user, and emails stay private |
| Canonical | `https://quartzmail.ai` |
| Language | `en` |
| Robots | `index, follow` |
| Keywords meta | Email client, AI email, private email, on-device AI, Mac email, Gmail, smart inbox, and categorization terms |
| Open Graph / Twitter | “Quartz \| AI-native email” with a 1200 × 630 image |
| JSON-LD | `SoftwareApplication`, macOS, `BusinessApplication`, price 0 USD |
| `hreflang` | None found |
| Sitemap | Homepage, privacy, terms, and contact only |

The title names email but not Mac or Gmail. The hero names focus and local AI
but not “email client.” Search engines still rank the page first for `quartz
email client`, while the site has almost no non-brand visibility. The metadata
may contribute to relevance, but the available evidence does not isolate a
cause.

The sitemap exposes no comparison pages, use-case pages, changelog, blog, or
other repeatable search-content program on the Quartz domain.

## Measurement and technology

| Surface | Observed evidence | Boundary |
| --- | --- | --- |
| Framework and hosting | Next.js assets and Vercel response headers | Describes the site stack, not acquisition performance |
| Site analytics | PostHog loaded through first-party-looking `/ingest/` paths | Proves instrumentation capability, not useful events or attribution |
| Session replay and surveys | PostHog recorder, dead-click, survey, and web-vitals assets loaded | Installed capabilities; their active use and sampling are unknown |
| Product Hunt inbound | Product Hunt links to `?ref=producthunt` | Source-shaped destination, not a visit or activation |
| Other referrals | Several indexed pages use `ref` or UTM destinations | Parameters may be added by the referring platform |
| Download route | Stable `/download` redirect to a versioned Google Cloud Storage object | Direct access and version can be observed; completed downloads cannot |
| Homepage form | None | There is no current website lead-capture step |
| Visible consent surface | None in the captured visit | Does not establish legal compliance or all geographic behavior |

No visible signatures were found in the rendered visit for Google Analytics,
Google Tag Manager, Meta, LinkedIn, Reddit, Hotjar, FullStory, Clarity, HubSpot,
Intercom, Optimizely, or VWO. This is a one-visit client-side observation, not
proof that Quartz never used those services or has no server-side measurement.

## Privacy claim boundary

The homepage says:

- “Your emails stay private, never shared with AI providers.”
- “Processed on this device. Your mail is never uploaded.”
- “We can't read your mail. Neither can our servers, because there are none.”
- “End-to-end encrypted.”

The [privacy policy](https://www.quartzmail.ai/privacy) gives the necessary
qualifications:

- Mail, attachments, labels, and metadata are cached in a local app store.
- On-device AI is the default.
- Users may optionally enable a third-party AI provider and direct relevant
  message text to it.
- App analytics are mandatory during beta and are associated with the connected
  account's email address.
- PostHog receives environment and behavior events, but the policy says it does
  not receive mail content, correspondents, subjects, labels, attachments, or
  message metadata.
- Website analytics may use IP-derived approximate location.

The maker's [technical case
study](https://datarockets.com/case-studies/quartz-mail-ai/) describes SQLCipher
for the local database and Keychain-held keys. That is concrete encrypted-at-
rest evidence. The public phrase “end-to-end encrypted” is broader and may be
read as a statement about message transport or provider storage, which the page
does not establish.

No Quartz-specific public certificate or registry entry was located during
this research. The CASA statement should therefore be treated as a first-party
claim whose assurance level is described by the [App Defense Alliance tier
framework](https://appdefensealliance.dev/casa/casa-tiering), not as an
independently verified acquisition result.

For Tecotype, this is a reason to keep claims narrower than the architecture:
local working copy, local search, and optional on-device Better search are
defensible. Encrypted mailbox, end-to-end encrypted mail, no servers, and “mail
never leaves the device” are not.

## Page changes

| Element | May 23 private beta | June 17 launch | Current page | Interpretation |
| --- | --- | --- | --- | --- |
| Platform/status | Mac, iOS, Gmail; private beta | Mac, Gmail; public beta | Mac, Gmail; public beta | The public promise narrowed to the shipped Mac surface |
| Hero | “Email, that knows what deserves your attention.” | Same | “Email built for focus, powered by local AI.” | The headline became more direct and technology-explicit |
| Offer | Email waitlist; invitations in small batches | Direct Mac download; free beta | Direct Mac download; free beta | Access friction was removed |
| Launch surface | Archived URL carried `ref=betalist` | Product Hunt banner and CTA | Product Hunt badges; no launch banner | Prelaunch directory capture gave way to launch proof |
| Secondary CTA | “Learn more” | “Learn more” | “Watch the demo” | Product proof became more prominent |
| Privacy proof | Local AI and encryption claims | Added CASA Tier 2 | CASA Tier 2 remains | Certification became a persistent trust asset |
| Product visual | Animated/synthetic inbox examples | Updated product screenshot and compose example | Same core proof | The page moved toward showing the current app |

Sources: [archived BetaList
listing](https://web.archive.org/web/20260523204739/https://betalist.com/startups/quartz),
[May 23
archive](https://web.archive.org/web/20260523204711/https://www.quartzmail.ai/?ref=betalist),
[June 17
archive](https://web.archive.org/web/20260617072126/https://www.quartzmail.ai/),
and the [current homepage](https://www.quartzmail.ai/).

The current page does not prove that “local AI” outperformed the earlier
attention-led headline. A changed message is an experiment or revision, not a
result.

## What this tells us about acquisition

- At its June 17 public launch, Quartz replaced the waitlist with a direct,
  versioned download.
- The page continues the exact Product Hunt promise: focus, Mac, local AI, and
  Gmail.
- Product screenshots, a short demo, certification, and maker explanations
  provide more proof than a feature checklist alone.
- The current page removes the email-capture fallback, so ineligible visitors
  have no visible lower-commitment next step.
- Material setup facts sit after the download or in legal/community pages.
  Tecotype's more explicit resource-cost disclosure is a candidate trust
  distinction to validate with users.
- A four-URL sitemap and negligible non-brand rankings indicate a launch page,
  not a search acquisition system.
