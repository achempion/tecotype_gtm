# Locker landing-page research

Capture date: **2026-07-17**

URL: [https://www.inbox.locker/](https://www.inbox.locker/)

Rendered capture: **desktop in-app browser, 892 × 1033 CSS pixels; no disk
image fetched and no account or mailbox authorization**

Scope boundary: the page describes more functionality than the latest public
release notes. This report treats [v0.3.0](https://github.com/newtophilly/locker-releases/releases/tag/v0.3.0)
as the public shipped boundary and
[v0.4.0](https://www.inbox.locker/whats-new) as in testing.

## Technical surface

### Hosting and framework

The live response showed:

- Next.js-rendered markup and first-party `/_next/` chunks.
- Vercel response headers.
- A prerendered homepage.
- No visible cookie or tracking-consent interface.

The rendered page and retrieved markup exposed no recognizable client-side
analytics, ad pixel, session-replay, A/B-testing, CRM, chat, or affiliate
script. The script set consisted of first-party Next.js assets.

That observation does not rule out server logs, server-side measurement,
checkout-provider measurement, consent-conditional code, or scripts delivered
to another geography.

### Metadata

| Field | Observed value |
| --- | --- |
| HTML language | `en` |
| Title | `Locker — A private AI inbox that runs on your Mac` |
| Description | `Locker is a private AI inbox for Mac. It sorts, answers, and protects your email — and the AI runs on your Mac's own chip. Nothing leaves your device.` |
| Open Graph title | Same as page title |
| Open Graph description | Same as meta description |
| Open Graph URL | `https://www.inbox.locker` |
| Open Graph site / locale / type | `Locker` / `en_US` / `website` |
| Twitter card | `summary_large_image` |
| Twitter title / description | Same product title and description |
| Favicon | 256 × 256 ICO |

No canonical link, `hreflang`, app link, JSON-LD structured data, or Open Graph
image was found in the captured homepage markup. No page-level `robots` meta
directive was present.

The public [`robots.txt`](https://www.inbox.locker/robots.txt) allows the site
and excludes `/api/`, `/admin`, `/welcome`, and `/design`. The public
[`sitemap.xml`](https://www.inbox.locker/sitemap.xml) lists the homepage,
changelog, privacy, terms, and refunds pages.

### Public actions

| Action | Destination | Source tagging |
| --- | --- | --- |
| Header `Download` | Latest `Locker.dmg` in `newtophilly/locker-releases` | None |
| Hero `Download for Mac` | Same latest disk image | None |
| `Get Locker — $39.99 →` | `/api/license/checkout?plan=current`, then Polar checkout | No visible acquisition-source parameter |
| `Want to test? Message Nathan →` | Pre-filled `mailto:` message to the maker | None |
| Footer links | Changelog, privacy, terms, refunds | None |

There is no email form on the current homepage. An earlier indexed page state
used a one-time launch-notification form; see [history.md](./history.md).

## Observed message

### Hero

The page opens with:

> 100% on your Mac · no cloud · no account

> Your inbox. Your Mac. Nobody else's.

It describes “a real email app with an AI that sorts, answers, and defends your
inbox” on the Mac's chip, followed by a direct download.

The adjacent status line says:

> Apple Silicon · macOS 14+ · auto-updates · 10 lifetime spots at $39.99

### Product demonstrations

The page shows:

- A command-bar example for finding, archiving, labeling, and clearing mail.
- A meaning-search example in which `baby stuff` retrieves messages without
  that keyword.
- Cards for important notifications, rules, sender screening, phishing
  detection, tracking-pixel blocking, a daily brief, drafted replies,
  subscription detection, cleanup, and translation.
- A direct comparison with cloud AI inboxes.
- Gmail and IMAP connection plus an Apple Mail path for some managed work
  accounts.
- Approval before replies, archives, and unsubscribes.

The product screenshot and UI examples are demonstrations. They are not
evidence that every depicted capability is present in the downloadable build.

### Offer

The current offer says:

- First 10 customers: $39.99 lifetime.
- Next 50 customers: $70 lifetime.
- After those 60: $129 for four years of updates.
- The installed app keeps working after the update period.
- No monthly subscription.

At capture, the dynamic card showed:

- `Founder lifetime — $39.99 · 10 of 10 left`.
- `All free keys claimed`.
- Five free keys marked `Taken`.

The [terms](https://www.inbox.locker/terms) make the license personal and
non-transferable. The [refund policy](https://www.inbox.locker/refunds) says
sales are final except where law requires otherwise and explicitly frames the
public download as a chance to try before buying.

### Trust material

Observed trust material includes:

- On-device and no-telemetry explanations.
- Direct provider and Apple Mail connection details.
- A visible approval promise before outgoing actions.
- A product screenshot and concrete search example.
- A public changelog.
- Public GitHub release metadata, publisher-authored signing/notarization
  claims, and GitHub-reported SHA-256 digests.
- Privacy, terms, and refund pages.
- Polar named as merchant of record.

The page showed no customer testimonial, customer logo, review score,
independent audit, active-user count, or benchmark.

## Customer and positioning hypothesis

| Question | Evidence | Classification |
| --- | --- | --- |
| Who is it for? | Apple Silicon Mac users who want local AI, Gmail/IMAP access, and possibly a work mailbox through Apple Mail | Observed platform; inferred audience |
| What job leads them here? | Search, triage, reply, screen senders, reduce notifications, and automate selected inbox work | Observed promise |
| What is the lead benefit? | Private intelligent email behavior without a vendor cloud mailbox | Observed |
| What is the mechanism? | On-device model, direct provider connection, local app, and approval before actions | Observed claim |
| What is the category? | Private AI email client for Mac | Observed metadata |
| What is the emotional angle? | Ownership, defense, privacy, anti-cloud control, and price relief | Inferred from observed copy |
| What supports the promise? | UI demonstrations, changelog, public release metadata and asset listing, policies, and technical detail | Observed |
| What is the offer? | Free download plus a staged one-time license | Observed |
| What action is requested? | Download first, buy separately, or contact the maker to test | Observed |
| What happens after install? | License activation and mailbox connection | Partly observed in public instructions; actual completion unobservable |

## Claim boundary and internal contradiction

The current [What's New](https://www.inbox.locker/whats-new) page labels
v0.4.0:

> Next release · in testing

Its v0.4 list includes work-account connection through Apple Mail,
attachments, reply-all and forwarding, smart notifications, custom rules,
reminders, and per-account inboxes. Several of those ideas appear on the
homepage under “Everything else it does” without an in-testing label.

The latest downloadable release is v0.3.0. Its public notes place meaning-based
search and automatic port selection inside the publisher's shipped boundary,
while v0.2.0 places automatic updates, the command bar, Sent, and several fixes
inside that boundary. The public artifacts do not establish every homepage
card, including sender screening, phishing detection, pixel blocking,
subscription detection, and translation.

The privacy copy is also more precise than the hero. It says the app still
connects to the user's mail provider, update service, and license-validation
service. It separately says an optional cloud-AI task would send selected text
to the provider the user chooses.

Accordingly:

- The homepage statements are observed marketing claims.
- v0.1.0–v0.3.0 release notes are the publisher's public shipped evidence;
  their feature behavior was not independently tested.
- v0.4.0 is observed in-testing work.
- The repository description and v0.1.0/v0.2.0 release text claim signing and
  notarization; the disk image was not fetched, so those publisher-authored
  claims were not independently verified.
- Post-install behavior and every unsupported homepage card remain
  unverified.

## Acquisition implications

- The page makes trial unusually easy by placing a public disk-image link
  before the paywall.
- The payment CTA is measurable at Polar, but no source parameter survives
  from the homepage into the visible endpoint.
- The price ladder and remaining-count display create urgency that conflicts
  with Tecotype's calm positioning.
- The product demonstration is specific, but the lack of a current-feature
  label makes the proof less trustworthy.
- Tecotype can adapt the concrete demonstration and download clarity, but
  should publish a release-accurate capability boundary and a calmer,
  source-attributed path.
