# Landing-page research

Current URL: `https://www.carbonmail.app/`

Captured: **2026-07-17**

Context: **rendered desktop page, logged out, 1280 × 720 viewport**

Capture geography: **uncontrolled browser egress; no location override**

Historical comparison: **January waitlist and beta launch**

## Current page

### Observed message and offer

| Page element | Copy or behavior |
| --- | --- |
| Hero | “The only resource you can't buy back.” |
| Product description | “The high-performance email client for those who value their time” |
| Mechanism | “100% on-device intelligence” filters inbox noise |
| Emotional outcome | Finish the day, go home, and reach “peace” through zero unread messages |
| Primary CTA | “Get Started,” linking to `/login` |
| Closing CTA | “Connect Gmail,” also linking to `/login` |
| Supported provider | Gmail |
| Delivery | Browser application; JSON-LD says `Web Browser` |
| Current offer | Free; optional paid power-user features may come later |
| Future platform promise | Android and iOS companions “coming late 2026” |
| Homepage form | None |
| Visible price, trial, or checkout | None |

The page leads with time pressure and the promise of finishing email rather
than with privacy. It then presents four task categories, local writing help,
keyboard operation, search, security checks, organization, and composing as
proof.

The page makes a large number of feature claims but renders no product
screenshot, video, iframe, testimonial, review, customer logo, or benchmark.
Its only direct product proof before account connection is prose and decorative
icons. JSON-LD references `/screenshot.png`, but that image is not present in
the rendered page.

### Customer and positioning hypothesis

**Observed:** Carbon says it is for people who value their time and want to be
done with email. The page promises automatic sorting into Decide, Act, Respond,
and Review; summaries and writing assistance; keyboard shortcuts; tracking and
phishing protection; tasks; and a responsive interface.

**Inferred:** The likely user is an email-heavy Gmail professional attracted to
automation, inbox zero, and the idea of local intelligence. January founder
comments named the “average corporate email user,” but the current page does
not retain that role or company context.

**Unobservable:** Which claims are complete in the current beta, who connects
Gmail, who reaches first value, who returns the next morning, or who would pay.

The current message hierarchy is:

1. Time recovery and finishing the workday.
2. Automated reduction of inbox decisions.
3. On-device intelligence and privacy.
4. A broad premium feature set.
5. Free access.

This overlaps with Tecotype's calm and local-processing territory, but the
emotional contract differs. Carbon dramatizes time loss, promises to give a
workday back, and calls itself high performance. Tecotype's current position is
calm control proved by keyboard operation, Gmail plus generic IMAP, local
search, optional on-device Better search, Split Inbox capability, and
reminders. Tecotype should not imply that it ships Carbon-like automatic
classification or generative writing.

## Metadata and indexability

| Field | Current value |
| --- | --- |
| Title | `Carbon Mail – Email Client with Local AI \| Zero Tracking` |
| Description | `Turn 200 emails into 12 that matter. Local AI filters noise in your browser. 100% private, zero tracking. Works with Gmail.` |
| Canonical | `https://www.carbonmail.app/` |
| Language | `en` |
| Robots | `index, follow` |
| Keywords meta | Brand, local/on-device AI, private email, Gmail alternative, inbox zero, Superhuman, HEY, and productivity terms |
| Open Graph | “Carbon Mail – Email That Doesn't Waste Your Time” |
| Twitter | `@carbonmail`, with local-AI and zero-tracking copy |
| JSON-LD | `SoftwareApplication`, web browser, business application, 0 USD |
| `hreflang` | None found |
| Sitemap | Homepage only |

The sitemap reports one URL with `lastmod` of
`2026-01-27T20:47:59.343Z`, shortly after the founders' January 27 launch
posts. It exposes no pricing, privacy, terms, blog, comparison, help, or
use-case page. The robots file allows the public site and blocks inbox,
settings, API, connect, authentication, and Next.js paths.

The single-page structure supports brand capture but not a repeatable
non-brand search program. DataForSEO Labs returned no ranked-keyword or
relevant-page items for the US-English snapshot; see [traffic.md](./traffic.md).

## Measurement and technology

| Surface | Observed evidence | Boundary |
| --- | --- | --- |
| Framework and hosting | Next.js assets and Vercel response headers | Site stack, not acquisition performance |
| Site analytics | Vercel Web Analytics script | Installed measurement capability, not useful events or attribution |
| CTA attribution | All homepage CTAs use untagged `/login` links | Referrer or analytics may still be available |
| OAuth implementation | Public client bundle uses Supabase Google OAuth | Static implementation evidence, not an architecture audit |
| Homepage form | None | No current website lead-capture fallback |
| Visible consent surface | None in the captured visit | One geography and one visit only |

No visible signatures were found in the rendered visit for Google Analytics,
Google Tag Manager, Meta, LinkedIn, Reddit, PostHog, Hotjar, FullStory,
Microsoft Clarity, HubSpot, Intercom, Optimizely, or VWO. This does not rule out
server-side, consent-gated, geographically conditional, or historical use.

The homepage set no cookie in the captured HTTP response and showed no consent
interface. Vercel Analytics can still measure without a conventional
third-party advertising pixel.

## Claim and trust boundary

### Privacy

The homepage says:

- intelligence runs completely on the device;
- Carbon “technically cannot” see emails;
- data never leaves the user's hardware; and
- Carbon is a lens for an existing Gmail account.

The login page says Carbon accesses “only” email metadata for labeling and
never stores email content on its servers. Public client code requests Google's
`gmail.readonly`, `gmail.send`, and `gmail.modify` scopes. It also checks a
Supabase table named `user_tokens` for an `access_token`.

Those observations do not prove that Carbon's operators read or store message
content. They do show that the literal claims “data never leaves your
hardware” and “we technically cannot see your emails” need qualification:

- the mailbox already resides with Gmail;
- the requested scopes permit reading message content, modifying mail, and
  sending mail; and
- an OAuth access token is represented in a hosted database path.

Tecotype should keep its narrower boundary: mail still communicates with the
provider, while Tecotype's local search and optional Better search do not add a
cloud AI processor.

### Quantitative and social proof

The page says users lose 11 hours per week to email, decision fatigue starts
after two hours, Carbon gives that workday back, and “many” people have found
the calm side of email. No citation, benchmark, cohort, user count, or
before-and-after study is linked.

The 11-hour figure resembles a common extrapolation from an older claim that
knowledge workers spend 28% of the workweek on email. That does not establish
that Carbon recovers the time. The two-hour fatigue threshold was not traced to
a relevant primary source.

January founder posts described only a handful of mostly friends-and-family
testers. The current word “many” is therefore unquantified, not verified social
proof.

### Product and platform proof

The current feature list is substantially broader than the January founder
description of local categorization. It remains marketing copy because the
Gmail authorization path was not completed.

The page also says the interface looks right on phone and tablet while saying
mobile companions are planned for late 2026. A responsive web application and
a native mobile companion could both make those statements true, but the
difference is not explained.

The footer's only legal link, “Privacy,” returned HTTP 404 on the capture date.
No terms or operator-contact link was visible. The footer label “Carbon Inc.”
was not independently verified as a legal entity.

## Visual and voice observations

The page uses large Playfair-style serif headlines, restrained black and cream
colors, blurred background gradients, rounded feature panels, animated entry
effects, and decorative icons. It feels editorial and polished, but the
animation and feature-card density are more expressive than Tecotype's
text-led, stable visual position.

The copy relies on pressure and performance:

- “The only resource you can't buy back.”
- “11 Hours.”
- “We give that day back to you.”
- “High-performance.”
- “Imagine ending your day with zero unread messages.”

Tecotype's positioning explicitly avoids dramatizing inbox pain, unverified
time-saved claims, performance theatre, and inbox-zero pressure. Carbon is
therefore more useful as a contrast than as a copy model.

## What this tells us about acquisition

- Carbon's homepage is a conversion page for existing awareness, not a broad
  discovery system.
- Metadata targets several category terms, but the site has no supporting
  content or modeled non-brand footprint.
- The “lens for Gmail” language addresses switching resistance identified by
  the founders, while the product still asks the user to adopt another inbox.
- Broad claims and a free CTA reduce explanation and price friction but provide
  little product proof.
- A broken privacy link and unverified-app warning weaken the exact trust
  promise the page emphasizes.
- Tecotype can differentiate with a precise product demonstration and factual
  boundaries rather than a longer feature list.
