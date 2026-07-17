# Epistles landing page

Captured: **2026-07-17**

Primary URL: [https://epistles.com/](https://epistles.com/)

Rendered viewport: **1280 × 720 desktop**

Language: **English**

Page state: **current public launch page; the response was last modified on
2026-07-17 and linked to current distribution**

## Observed message

The page leads with:

- Eyebrow: “Multi-account mail without flattening the providers.”
- Headline: “One app for all your email accounts.”
- Primary CTA: “Download free.”
- Secondary CTA: “See pricing.”
- Offer line: free for up to two accounts on all eight claimed platforms, with
  no Epistles account needed to start.

The mechanism is unusually explicit:

- Gmail through the Gmail API.
- Microsoft 365 through an OWA path.
- Fastmail and compatible servers through JMAP.
- iCloud through IMAP, CalDAV, and CardDAV.
- Proton through its private API plus on-device OpenPGP.
- Other providers through IMAP and SMTP.
- Mail and search in a local SQLite store.
- A Cloud Vault for cross-device credential and preference sync, subject to
  documented carve-outs.

The page's emotional promise is calm consolidation without erasing account
identity: one application, provider-specific behavior, local search, and fewer
app switches.

## Customer and message hypothesis

| Question | Evidence | Classification |
| --- | --- | --- |
| Who is it for? | People using work, personal, school, custom-domain, self-hosted, or privacy-oriented accounts across several providers and devices | Observed, with segment breadth inferred |
| What triggers the search? | Switching between provider apps; losing labels, categories, identities, or protocol behavior in a lowest-common-denominator client | Observed |
| What is the promise? | One calmer client for all accounts, with on-device search and provider behavior intact | Observed |
| Why this product? | Native/provider-specific adapters, unusually broad platform coverage, local mail store, calendar and contacts, and Proton without Bridge | Observed claims |
| What is the emotional angle? | Calm, control, portability, technical honesty, and freedom from provider lock-in | Observed and inferred |
| What supports the claim? | Product screenshots, detailed security pages, current artifacts, app-store listings, a claimed CASA assessment, and a public changelog | Observed; assessment result itself not independently obtained |
| What is the offer? | Two-account free tier; $35/year Pro trial; $79/$99 capped lifetime offer | Observed |
| What action is requested? | Download free or inspect pricing, followed by a platform handoff | Observed |

## Page architecture

The current homepage moves through:

1. 1.0 launch banner and multi-account hero.
2. Provider-specific protocol explanations.
3. Desktop and mobile screenshots.
4. Apple Watch and Wear OS triage.
5. Local-storage and server-boundary explanation.
6. A claimed CASA Tier 2 assessment badge.
7. Platform list and direct download CTA.
8. Footer links to FAQ, comparisons, developers, pricing, changelog,
   security, promises, privacy, terms, support, and social profiles.

This structure serves three separate objections:

- **Will it connect my unusual account mix?**
- **Will it preserve how each provider works?**
- **Can I trust a new closed-source client with mailbox access?**

The last objection receives the most copy, but current first-party
documentation does not resolve it consistently.

## Technical and metadata evidence

### Standard metadata

Observed:

- Title: `Epistles Mail · One client for every email provider`
- Description: native, local-first support for Gmail, Outlook, Fastmail/JMAP,
  iCloud, Proton, and IMAP across desktop, mobile, web, and watches.
- Canonical: `https://epistles.com/`
- HTML language: `en`
- Complete Open Graph and Twitter card fields.
- Social handle: `@EpistlesMail`
- 1200 × 630 Open Graph image.
- HTTPS, HSTS, `frame-ancestors 'none'`, `X-Frame-Options: DENY`,
  `nosniff`, and a restrictive permissions policy.

The response identifies Cloudflare at the edge and includes Amazon S3-style
origin headers. That is an operating/hosting signal, not an acquisition result.

### Structured data

The homepage includes a JSON-LD graph for:

- `SoftwareApplication`
- `Organization`
- `WebSite`
- `WebPage`
- `FAQPage`

It describes providers, platforms, features, free and paid offers, social
profiles, and many purchase-adjacent questions. This is a deliberate
search-answer strategy.

There is also drift:

- The structured FAQ says the six main platforms were generally available in
  May 2026.
- The official changelog dates 1.0 general availability to July 8.
- The June 18 Wayback snapshot still described a private beta.

This may be stale schema rather than a false product state, but it means the
structured data is not a reliable chronology.

### Analytics and scripts

Observed on the marketing site:

- Google tag loader:
  `https://www.googletagmanager.com/gtag/js?id=G-M2WEJFCENR`
- Measurement ID: `G-M2WEJFCENR`
- A simple initializer that calls `gtag('config', 'G-M2WEJFCENR')`.
- First-party site JavaScript.

No advertising pixel, product analytics SDK, session replay, A/B test,
customer-chat widget, or affiliate script was identified in the captured
homepage source.

The content-security policy permits Cloudflare Insights, but permission in a
CSP is not proof that its beacon executed. A July 9 Privacy Guides commenter
reported seeing Cloudflare Insights; the July 17 static source directly
verified Google Analytics only.

The security page now distinguishes between:

- no claimed analytics or third-party crash reporter in the desktop/mobile
  apps; and
- Google Analytics on the marketing site.

That distinction is more precise than a blanket “no telemetry” claim. The
privacy policy's metadata still advertises “no telemetry,” while its body
allows service providers for analytics in general terms.

### Forms and consent

The current homepage contained:

- no form;
- no active waitlist input;
- no visible cookie or analytics consent interface in the captured desktop
  view; and
- a leftover `epistles:subscribe-url` metadata value pointing to
  `https://api.epistles.net/subscribe`.

The old private-beta page did contain waitlist forms and Cloudflare Turnstile.
The current metadata appears to be a remnant, not a visible acquisition route.

Installed analytics proves measurement capability, not useful attribution.
No public analytics output was available.

## CTA and attribution audit

| Surface | Destination | Visible parameters | Implication |
| --- | --- | --- | --- |
| Hero “Download free” | `/download/` | None | Marketing-site click can be measured by page analytics, but source is not carried visibly |
| “See pricing” | `/pricing/` | None | No visible campaign identity |
| Platform store links | Apple App Store and Google Play | No campaign parameters | Store installs cannot be attributed from the public URL |
| Direct packages | `repo.epistles.com` | No campaign parameters | Repository requests are not visibly tied to source |
| Annual upgrade | `app.epistles.com/upgrade?plan=annual` | Plan only | Product intent is specified, acquisition source is not |
| Lifetime upgrade | `app.epistles.com/upgrade?plan=bereans` | Plan only | Same attribution gap |
| Founder Reddit posts | Usually root homepage or plain waitlist link | No UTM/source tag observed | Publicly impossible to connect post to install or sale |

Cookies, referrers, server logs, or private app analytics could provide more
information. The public route itself does not demonstrate that they do.

## Search inventory

The public sitemap lists 25 URLs, including:

- the homepage;
- download, FAQ, security, promises, compare, watch, developers, changelog,
  support, privacy, and terms pages;
- a Linux page; and
- 12 alternative pages for Newton, Mimestream, Gmail, Outlook, Proton,
  Apple Mail, Fastmail, Spark, Superhuman, Canary, Thunderbird, and Mailbird.

Pricing is both disallowed in `robots.txt` and marked `noindex, nofollow`.
The Bereans lifetime page is also `noindex, nofollow`. The robots comment still
calls pricing “unreleased” even though the homepage now links it after launch.

This keeps conversion pages out of organic discovery while allowing comparison
and provider pages to rank. It may be deliberate, stale launch configuration,
or both; intent is unobservable.

## Trust evidence and claim boundaries

### What the current first-party pages support

The public product and security pages state:

- mail content is fetched between device and provider and stored locally;
- the local mail database relies on operating-system disk encryption rather
  than an Epistles database-encryption layer;
- the Cloud Vault encrypts IMAP passwords, JMAP session blobs, and similar
  credentials with a device-side key;
- the Epistles password reaches the server over TLS for bcrypt comparison;
- Gmail and Fastmail OAuth refresh tokens are a deliberate server-readable
  carve-out, encrypted with a backend-held key;
- server records can include account email, password hash, wrapped vault key,
  provider/account existence, sessions with IP and user agent, push tokens,
  preferences, support records, and opt-in outbound tracking metadata;
- the marketing site uses Google Analytics;
- backend error reporting uses Sentry; and
- the client source is proprietary and not public.

These qualifications are materially narrower than “nothing leaves the
device,” and the report uses the qualified model.

### CASA claim

The homepage says Epistles passed a CASA Tier 2 assessment by TAC Security.
The [App Defense Alliance assessor list](https://appdefensealliance.dev/casa/casa-assessors)
lists TAC Security as an authorized CASA assessor.
The captured homepage links to the general CASA page and displays a badge, but
not to an Epistles-specific letter or assessment report. A narrow public search
did not locate such an artifact.

Therefore:

- **Observed:** Epistles displays the assessment claim and badge.
- **Corroborated:** TAC Security is an authorized assessor.
- **Unverified:** the Epistles-specific scope, date, report, findings, and
  remediation.

### Current first-party conflicts

| Claim surface | Conflicting surface | Boundary |
| --- | --- | --- |
| Security-page introduction says claims map to code a reader can inspect, and names files described as open to read | The same page and developer page say the source is proprietary, closed, and not public | No public client source link or repository was found |
| Promises page says each clause is mirrored in Terms and readable code | Current Terms contain no funding, acquisition, lifetime refund, abandonment, or MIT source-release clause | Marketing promise is not evidenced in the linked Terms |
| Bereans page says the source-shutdown promise “is in our Terms” | Current Terms omit it and allow features to change or be discontinued | Contractual enforceability was not assessed; the textual mismatch is direct |
| Bereans page refers to no commits in a public client repo | Public founder GitHub profile lists four repositories but no Epistles client source; `repo.epistles.com` distributes binaries/packages | A private or differently owned repository may exist, but it is not the promised public client source |
| Google Play declares no collected or shared data | Privacy/security pages describe account, session, provider-token, push-token, support, and optional tracking processing | Store disclosure is developer supplied; the report does not infer motive |
| Developer page says the single chronological unified list is later-2026 work | Pricing, homepage schema, subreddit release note, and changelog describe a unified inbox as current | Shipped boundary cannot be established from copy alone; current changelog favors “shipped” |
| Security page uses future tense for some relay behavior | Homepage and changelog describe active push and server functions | Trust documentation contains stale states after general availability |

### Entity surfaces

- Website footer and Google Play: **Moriah LLC**
- US App Store seller/developer: **Netwarden LLC**
- Identified founder: **Thiago Vinhas**
- Website location statement: **Made in Texas**

This may reflect related entities or store-account history. It is recorded as
an identity-verification cost, not evidence of misconduct.

## Interpretation

The landing page is more technically specific than most early competitors and
turns provider behavior into a clear reason to care. It also overextends:
eight platforms, mail, calendar, contacts, watches, unusual provider adapters,
local storage, cloud credential sync, tracking, and security assurances all
arrive in one launch narrative.

That breadth attracts specialized users, but it raises the amount of proof
required. The current documentation conflicts are therefore not peripheral:
they sit inside the exact trust question the landing page asks a new user to
resolve.

## Evidence boundaries

Directly observed:

- rendered homepage and upgrade sign-in state;
- public HTML, metadata, JSON-LD, scripts, response headers, sitemap, and
  robots directives;
- current first-party trust, pricing, legal, and developer pages;
- first-party CASA claim and authorized-assessor list.

Not observed:

- actual marketing sessions or events;
- consent state in every region;
- app network traffic after mailbox connection;
- client or backend source;
- the Epistles-specific CASA artifact;
- conversions, activation, retention, revenue, or satisfaction.

The request ledger and source URLs are in [requests.md](./requests.md).
