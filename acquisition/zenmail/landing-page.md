# Landing page

Captured: **2026-07-17**

Primary surface: [usezenmail.com](https://usezenmail.com/)

Market: **US-English**

Inspection mode: **desktop-oriented public HTML, metadata, scripts, legal
pages, CTA code, and image assets; no fixed rendered viewport was available**

Currentness: **the page appeared current on the capture date, matched the
20-URL sitemap and 15-article newsroom, and still offered only a private-beta
waitlist**

The current page is a product-shaped private-beta page. It shows a concrete
Mac inbox image, explains a small feature set, and repeats an email waitlist.
It does not expose a download, account flow, price, or checkout.

## Page structure

| Section | Observed message | Acquisition job |
| --- | --- | --- |
| Navigation | Features, Privacy, About, Newsroom, “Get early access” | Anchors to proof and the same waitlist |
| Hero | “The best Gmail client for Mac.” | Own the product/category phrase |
| Hero support | “Blazingly fast. Featherlight. Keyboard-first. The Mac email client that gets out of your way.” | Performance and restraint wedge |
| Hero CTA | Email field, “Get early access,” macOS 26+ | Capture demand without public access |
| Product image | Three-pane Mac inbox with Gmail-like labels, category tabs, shortcut-labelled actions, and thread view | Make the beta tangible |
| Feature grid | Screener, Smart Snooze, shortcuts, on-device AI, multi-account, Zen Mode | Convert broad promise into workflows |
| Privacy | “The most private email client on Mac,” CASA Tier 2 badge, no email backend, local database, Keychain, no app telemetry | Reduce Gmail OAuth and data-handling anxiety |
| FAQ | Beta availability and free-now/paid-later framing | Set access and price expectations |
| Closing CTA | “Get early access. We’re in private beta. Be first.” | Repeat the same email conversion |

The screenshot is a first-party product visual, not proof that the depicted
features are available or stable in the private beta.

## Feature claims

The page presents:

- an Inbox Screener that holds unknown senders for approve/deny decisions;
- Smart Snooze with natural-language times;
- a shortcut for every major action;
- on-device AI that reads and tags noise on the Mac;
- multiple Gmail accounts;
- Zen Mode, which processes one email at a time and counts progress.

These are observed page claims. No public demo, help center, release notes, or
installer was available to verify the complete workflow.

## Positioning mechanics

The page uses three layers:

1. **Category ownership:** “best Gmail client for Mac.”
2. **Immediate feel:** speed, low weight, keyboard control, and absence of
   bloat.
3. **System-level outcome:** keep unknown senders out, snooze naturally, and
   reach calm through one-message-at-a-time triage.

That is clearer than a feature inventory. Its weakness is proof: “best,”
“blazingly fast,” “most private,” and performance comparisons are not
supported by public test methodology.

## Metadata and discoverability

Observed homepage metadata:

| Field | Value |
| --- | --- |
| Title | `ZenMail — The best Gmail client for Mac` |
| Description | `A blazing fast, keyboard-first native Mac email client for Gmail. Built with SwiftUI and a native Swift mail engine. Local-first, lightweight, and works offline.` |
| Canonical | `https://usezenmail.com/` |
| Robots | Index/follow with unrestricted snippets and image/video previews |
| Open Graph/Twitter | Same product framing and hero image |
| Language | English / `en-US` in structured data |
| Hreflang | None observed |
| Sitemap | `https://usezenmail.com/sitemap.xml` |
| RSS declaration | `https://usezenmail.com/blog/rss.xml` |

The RSS URL is advertised in page markup, but repeated direct retrieval did
not return content during this pass. It should not be counted as a working
distribution channel without a successful response.

[Robots.txt](https://usezenmail.com/robots.txt) allows normal search crawlers
and explicitly allows many AI/search-assistant crawlers, including OpenAI,
Anthropic, Perplexity, Google-Extended, Applebot-Extended, Meta, ByteDance,
DuckAssist, Amazon, Mistral, Cohere, Diffbot, and CCBot. `/api/` is disallowed.
This is evidence of deliberate indexability, not evidence of AI referrals.

## Architecture and claim consistency

The public site describes at least two incompatible implementations:

| Surface | Public claim |
| --- | --- |
| Current homepage metadata and structured data | SwiftUI + AppKit, native Swift mail engine, about 150 MB of memory, WebKit only for sanitized message bodies |
| [Native vs. Electron](https://usezenmail.com/blog/native-vs-electron) | Rust + Tauri + WKWebView, under-15-MB binary, target cold start under 100 ms |
| [Why we built ZenMail](https://usezenmail.com/blog/why-we-built-zenmail) | Rust/Tauri and encrypted SQLite |
| [CASA article](https://usezenmail.com/blog/casa-tier-2-verification) | Native Rust, WKWebView, encrypted SQLite |
| Current homepage privacy section | “Protected local database”; files restricted to the macOS account |
| [Privacy policy](https://usezenmail.com/privacy), [About](https://usezenmail.com/about), and articles | Encrypted local database |

A product rewrite is one possible explanation, but it is an inference. The
site does not publish a migration note or dated specification. Acquisition
copy should not merge these claims or treat either stack as independently
verified. The 150-MB memory claim and under-15-MB binary claim are different
measurements, not a contradiction; neither has a public test method.

## Privacy and trust surface

The homepage says:

- ZenMail has no backend for email;
- inbox data exists only on the device and can work offline;
- local files are restricted to the macOS account;
- Gmail credentials are stored in Keychain;
- the app has no telemetry;
- Gmail permissions are minimized;
- ZenMail is a paid app, so it need not monetize user data;
- it is “CASA Tier 2 Verified.”

The [privacy policy](https://usezenmail.com/privacy), effective April 12, 2026,
adds:

- waitlist addresses are stored in a private Notion database;
- purchases may be handled by Polar;
- the website uses PostHog for pageviews, clicks, referrer, and device/browser
  metadata with IP anonymization;
- the app itself does not send telemetry, mail content, contacts, or
  credentials;
- Gmail tokens are stored in Keychain and mail is stored locally;
- support messages and purchase/license data may be retained.

The same policy section names PostHog as website analytics and then says
ZenMail does not use “analytics platforms.” That wording is internally
inconsistent even before considering the more detailed waitlist
instrumentation below.

The policy is first-party disclosure, not an audit. The [CASA
article](https://usezenmail.com/blog/casa-tier-2-verification) says an
App Defense Alliance-authorized lab assessed the app. No assessor name,
certificate, report, or registry entry is linked on the captured page, so the
badge was not independently verified.

The [terms](https://usezenmail.com/terms), also effective April 12, identify the
product only as “ZenMail,” describe an early-access Gmail-only beta, permit
features and pricing to change, mention possible Polar licensing, and choose
Israeli law and Tel Aviv courts. The [About page](https://usezenmail.com/about)
says it is an independent project built by one person. Neither page names the
developer or a legal entity.

## Waitlist implementation

The two visible forms use the same public client-side path:

```text
POST /api/waitlist
Content-Type: application/json
Body: { email, website }
Headers: x-posthog-distinct-id, x-posthog-session-id
```

`website` is a honeypot field. Before the network request, the bundle captures
`waitlist_signup_submitted` in PostHog and sends a parallel event to
`/api/event`. On success it identifies the visitor with the submitted email,
captures a success event that includes the email, and shows:

> You’re on the list. We’ll be in touch.

No address was submitted in this research.

The policy describes PostHog in terms of pageviews, click events, referrer,
and device/browser metadata. The client code additionally passes the waitlist
email as an event property and uses it for PostHog identification. This report
does not infer legality or server-side retention, but the public policy wording
is narrower than the observed client behavior.

## Analytics wiring

Observed PostHog configuration:

- public project key beginning `phc_…` (not reproduced because it adds no
  acquisition evidence);
- proxy host `/ingest` and US PostHog interface host;
- person profiles created for identified visitors only;
- automatic pageview capture disabled, with pageviews captured explicitly by
  the page layout;
- page-leave and exception capture enabled;
- first-party `/api/event` mirror for named events.

This proves the site can record a waitlist step. It does not prove events are
delivered, reconciled, used in decisions, or connected to invitation and
activation.

## Landing-page verdict

What is strong:

- one audience, one platform, one provider, and one conversion;
- a concrete visual and a compact workflow story;
- product, privacy, legal, and editorial surfaces are all indexable;
- the form has explicit submission/success instrumentation.

What is weak or risky:

- the highest-impact comparative claims lack public substantiation;
- technical and storage claims conflict across live pages;
- operator identity is unusually opaque for a Gmail OAuth product;
- CASA proof cannot be followed to an external artifact;
- the privacy wording does not fully describe the client-observed use of the
  waitlist email in PostHog;
- the public path does not let a visitor try, download, or buy the product.

The page may generate waitlist demand. Public evidence cannot show whether it
generates qualified, activated, or retained users.
