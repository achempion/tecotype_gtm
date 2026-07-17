# Landing-page research

Research date: **2026-07-17**

Current page: [velomail.app](https://velomail.app/)

Inspection mode: **rendered desktop capture at 1280 × 720 CSS pixels and device-pixel ratio 2, plus public HTML, bundle, metadata, and destination inspection**

No CTA was clicked in the rendered session. Public link destinations were established from the page source. No consent banner was visible in the capture.

## Current above-the-fold offer

Observed:

- eyebrow: **“Open source desktop email client”**;
- hero: **“The email client you’d build for yourself”**;
- subhead: **“Keyboard-first, AI-powered, and completely private. Free forever because it’s open source.”**;
- primary CTA: **“Download for Free”**;
- secondary CTA: **“View on GitHub”**;
- header CTA: **“Download”**;
- platforms named: Windows, macOS, and Linux.

All three acquisition actions lead to GitHub:

| Action | Destination | Implication |
| --- | --- | --- |
| Download for Free | `github.com/avihaymenahem/velo/releases` | User must choose among release entries and assets |
| Header Download | Same releases page | No platform-specific routing |
| View on GitHub | Repository root | Strong contributor/source path, weak product activation path |

There is no email capture, waitlist, pricing, account, checkout, app-store route, or platform chooser on the landing page. Contact is a `mailto:` link to `info@velomail.app`.

## Message architecture

The page combines five ideas:

```text
ownership: “you’d build for yourself”
+ workflow: keyboard-first
+ feature breadth: AI and 130+ features
+ trust: local-first, no tracking, open source
+ economics: free forever
```

This is memorable but not narrow. It asks one hero to sell a workflow, an AI layer, a privacy model, an open-source project, and free cross-platform distribution.

The feature sections include:

- **Keyboard-first:** 30+ shortcuts, two-key sequences, command palette, customization;
- **AI on your terms:** Claude, GPT, or Gemini with the user’s API key; summaries, smart replies, and categorization;
- **Local-first privacy:** local SQLite, no tracking or analytics, phishing detection, and AES-256 language;
- split inbox categories;
- Gmail, Outlook, Yahoo, iCloud, Fastmail, and generic IMAP/SMTP;
- snooze, scheduled send, undo send, notifications, Calendar, filters, newsletter bundles, tasks, themes, and composer features;
- Apache 2.0 source and “free forever.”

The current repository contains source and documentation corresponding to many of these categories. That establishes source presence, not that the research launched and validated each interaction.

## Claim audit

| Public claim | Public evidence | Assessment |
| --- | --- | --- |
| Open source | Public repository and current Apache-2.0 license | Supported |
| Free forever | Site and structured data report price `0 USD`; no paid path observed | Current offer supported; “forever” cannot be verified |
| Windows, macOS, Linux | Current release exposes installers/packages for all three | Distribution formats supported; install quality untested |
| Keyboard-first | Public shortcut documentation and source | Source-supported; usability untested |
| Gmail and IMAP providers | README, source tree, and release history | Source-supported; connection and sync untested |
| No Velo cloud/backend | Security document says there are no Velo-operated backend servers | First-party architecture claim; no runtime network audit |
| No tracking or analytics | Site bundle contained no recognizable GA, GTM, PostHog, Segment, Mixpanel, or similar product tracker | Supported for inspected site assets only; client runtime, server logs, and conditional behavior remain unverified |
| “Your data never leaves your machine” | AI feature sends selected content to Anthropic, OpenAI, Google, GitHub Models, or configured local endpoints | Contradicted when cloud AI is used |
| “Completely private” | Email-provider connections are required; cloud AI can receive content; local mail database is intentionally not encrypted at rest | Too absolute |
| AES-256 | Tokens and IMAP/app passwords are documented as AES-256-GCM encrypted | Narrowly supported for credentials; not whole-mailbox encryption |
| “No cloud” / “no cloud dependency” | Email service is necessarily remote and optional AI can be remote | Misleading unless explicitly limited to “no Velo-operated cloud” |
| “Ready in two minutes” | Gmail setup requires the user to create OAuth credentials in Google Cloud and enable Gmail and Calendar APIs | Unsubstantiated for the principal Gmail path |

The most material trust issue is adjacency: the page places “Your data never leaves your machine” inside the cloud-AI description. Velo’s own [security policy](https://github.com/avihaymenahem/velo/blob/main/SECURITY.md) says API keys and requests go directly to the chosen providers over HTTPS. Direct-to-provider is materially different from on-device.

The same policy says the local SQLite mail database **is not encrypted at rest by design**; operating-system file protection is the boundary. The page’s AES-256 badge can therefore be read more broadly than the documented design supports.

## Metadata and technical surface

Observed in current public HTML:

| Field | Value |
| --- | --- |
| Title | `Velo — The email client you'd build for yourself` |
| Description | `Free, open-source desktop email client. Keyboard-first, AI-powered, and completely private. Supports Gmail, Outlook, Yahoo, iCloud, and any IMAP provider. Available for Windows, macOS & Linux.` |
| Canonical | `https://velomail.app/` |
| Robots | `index, follow` |
| Language | `en` |
| Theme color | `#09090b` |
| Open Graph | title, description, site name, locale, and 1200 × 630 image |
| Twitter | `summary_large_image` |

Structured data includes:

- `SoftwareApplication`, with operating systems, `0 USD`, Apache license, GitHub releases download URL, and `softwareVersion: "1.0"`;
- `WebSite`;
- `FAQPage`.

The structured-data version conflicts with the current application manifest and latest release, both **0.4.21**. This may create false maturity and stale search metadata.

The page is a Vite/React single-page site served behind Cloudflare. Current assets include a React 19 bundle, first-party images, Google Fonts, and Cloudflare infrastructure. The inspected HTML and bundle exposed no recognizable source/campaign parameters, analytics events, experiments, or consent manager.

`robots.txt` allows all crawlers. The sitemap lists only the homepage and reports `lastmod` as **2026-02-13**, although public landing-source changes followed that date. This is a small currentness defect.

## Conversion and trust gaps

### 1. Generic download handoff

The primary CTA transfers the user from a polished product page to a developer-oriented release ledger. The page does not preserve source, message, platform, or intended installer.

### 2. Hidden Gmail prerequisite

The landing page says the app is ready quickly, while the README requires Gmail users to:

1. create a Google Cloud project;
2. enable Gmail API and Calendar API;
3. create OAuth credentials;
4. paste a client ID into Velo.

This is not ordinary consumer onboarding and is absent from the acquisition page.

### 3. Unsigned current macOS release

The exact [workflow run that built `velo-v0.4.21`](https://github.com/avihaymenahem/velo/actions/runs/22496174782):

- successfully checked whether Apple signing was configured;
- skipped certificate import;
- skipped all signed/notarized build steps;
- successfully ran **“Build and upload (unsigned)”**.

The current page gives no macOS warning before download. The principal launch thread includes one user’s “damaged and can’t be opened” report for an early build and a command-line workaround. That report is anecdotal, but the current unsigned workflow is direct first-party evidence.

### 4. Broken update manifest

The current application manifest configures:

`https://github.com/avihaymenahem/velo/releases/latest/download/latest.json`

On 2026-07-17 it redirected to the latest release and returned **404**. Source presence of an updater is therefore not evidence of a working update channel.

### 5. No public measurement bridge

No public surface connects:

```text
source → landing message → platform → release asset → install
→ mailbox connection → sync → first value → retained use
```

## What Tecotype should retain

- The self-directed ownership idea is stronger than the 130-feature inventory.
- Public technical proof can reduce “vaporware” skepticism.
- A direct-download CTA can be effective only after platform detection, signed distribution, update reliability, and source-to-activation measurement exist.
- Privacy copy should name the exact boundary: local storage, no Tecotype-operated processing where true, and explicit on-device versus provider-hosted behavior.
- A two-minute promise should be timed from a reproducible, ordinary-user first run—not inferred from source or developer setup.
