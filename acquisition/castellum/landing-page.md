# Castellum landing-page research

Capture date: **2026-07-17**

URL: [https://castellummail.com/](https://castellummail.com/)

Rendered capture: **desktop, 1280 × 720 CSS pixels at device-pixel ratio 2; no
download, account, mailbox authorization, form submission, or purchase**

Currentness: **the page appeared current and linked to
[v0.2.2](https://github.com/joanmarcriera/castellum-releases/releases/tag/v0.2.2),
the latest public release**

The release boundary matters. The page markets a usable Gmail-plus-IMAP
client, while the [v0.2.1 release
note](https://github.com/joanmarcriera/castellum-releases/releases/tag/v0.2.1)
says Google’s consent screen was still in testing mode and non-approved
addresses could be blocked. No later public note establishes general Google
authorization.

## Technical surface

### Hosting and page construction

Observed:

- Static HTML served by GitHub Pages.
- GitHub/Fastly response headers and a ten-minute cache policy.
- A single inline IntersectionObserver script for scroll-reveal effects.
- Google Fonts requests for Fraunces, Hanken Grotesk, and JetBrains Mono.
- One product screenshot loaded from the same site.
- No visible cookie or tracking-consent banner in the rendered capture.

The returned homepage exposed no recognizable:

- analytics or product-analytics script;
- advertising pixel;
- session replay;
- A/B testing platform;
- CRM, chat, or affiliate script;
- general source or UTM parameter on the download destination.

This one-time observation does not rule out GitHub/CDN logs, server-side
measurement, historical instrumentation, geographically conditional code, or
measurement inside the client.

### Metadata and indexability

| Field | Observed value |
| --- | --- |
| HTML language | `en` |
| Title | `Castellum — Command your inbox` |
| Description | `Castellum is a private, AI-powered email client for macOS. Built for managers who run projects out of their inbox — local AI, keyboard-first, your data never leaves your Mac.` |
| Open Graph type | `website` |
| Open Graph title | Same as page title |
| Open Graph description | Shorter private/local-AI description |
| Open Graph URL | `https://castellummail.com` |
| Open Graph image | `https://castellummail.com/icon.png` |
| Twitter card | `summary_large_image` |
| Canonical link | Not found |
| Page-level robots meta | Not found |
| JSON-LD | Not found |
| `hreflang` | Not found |
| App-link metadata | Not found |
| `robots.txt` | GitHub Pages 404 |
| `sitemap.xml` | GitHub Pages 404 |

The page is indexable by default, but it omits normal canonical and discovery
files. Search has nevertheless indexed the homepage in the Labs snapshot.

### Public actions

| Action | Destination | Visible source tagging |
| --- | --- | --- |
| Header `Download` | `#download` on the same page | None |
| Hero `Download for Mac` | `#download` on the same page | None |
| `See what's inside` | `#features` | None |
| Final `Download for Mac` | Latest `Castellum-arm64.dmg` GitHub asset | None |
| `SHA-256 checksum` | Latest GitHub release page | None |
| Ollama setup link | `ollama.com/download` | None |
| `Releases` | Public GitHub releases page | None |
| `Found a bug?` | Public GitHub issues page or in-app prefilled issue | None visible on the site |
| Legal links | Privacy, Terms, Google Limited-Use | None |

No waitlist, newsletter, account form, checkout, or consultation form is
present. The hero and navigation only scroll to the final direct-download
link.

## Rendered hierarchy

At 1280 × 720:

- a dark navy-and-gold castle theme dominates;
- a serif hero and castle medallion carry the brand;
- the primary visible action is `Download for Mac`;
- “Free in early access,” Apple notarization, and Apple Silicon sit directly
  under the CTA;
- no consent interface or competing conversion surface is visible;
- the product screenshot and feature sections continue below the first view.

The visual system makes the “fortress” metaphor easy to remember. It also
spends substantial space on theme before independently proving use or
adoption. That is a positioning observation, not a conversion judgment.

## Observed message

### Hero

The page opens with:

> Command your inbox like a fortress.

It defines Castellum as:

> a private, AI-powered email client for managers who run projects out of
> their inbox

The proof line combines:

- local AI;
- keyboard-first interaction;
- the statement that mail never leaves the Mac.

The immediate offer is:

- free during early access;
- macOS 12 or newer;
- Apple Silicon M1–M4;
- claimed signed and notarized;
- a disk image described as about 114 MB.

### Product mechanism

The page presents:

- **Active Work:** a kanban-like view for follow-ups and overdue replies.
- **Local AI:** summaries, triage, and draft replies through Ollama.
- **Gmail:** one-click Google sign-in.
- **IMAP/SMTP:** guided setup for 31 named providers plus autoconfig fallback.
- **Keyboard use:** `j`/`k`, `/`, and a command palette.
- **Project context:** project spaces, notes, contacts, calendar, and
  meeting-prep summaries.
- **Local storage:** mail and notes in SQLite on the Mac.

The screenshot visually supports the inbox, Active Work, Projects, Contacts,
and Smart Mailboxes story. It is a product demonstration, not independent
evidence that every shown workflow works for a newly connected mailbox.

### Local-AI setup

The page makes the dependency unusually explicit:

1. Install and open Ollama.
2. Let Castellum detect the local service.
3. Select `Install recommended model`.

It names `llama3.2`, says 16 GB or more is comfortable, and says the app shows
download progress. The dependency can reduce cloud-AI concern while adding a
second install and a model download before AI value.

Neither Ollama nor the model was downloaded or installed.

### Provider breadth

The page lists 31 provider presets, emphasizes Europe, and says thousands more
domains use Thunderbird autoconfig. This is first-party compatibility copy.

One important qualification is visible only in the release notes:
v0.2.2 names **Proton (Bridge)**, while the homepage chip says only “Proton
Mail.” Proton’s own [IMAP/SMTP
documentation](https://proton.me/support/imap-smtp-and-pop3-setup) says Bridge
is required for normal desktop-client IMAP access and is available on paid
plans. That does not disprove Castellum compatibility; it makes the unqualified
chip incomplete.

## Offer and proof

### Offer

Observed:

- direct public download;
- no Castellum account, email form, or card before the asset link;
- no visible trial clock;
- free during early access;
- homepage promise that an installed build keeps working if paid plans arrive;
- no current price or checkout.

The [Terms](https://castellummail.com/terms) say a personal,
non-transferable early-access license is free and future paid licensing may be
introduced. The [Privacy Policy](https://castellummail.com/privacy) already
names Lemon Squeezy, self-hosted n8n, and self-hosted EspoCRM for future
purchase/license data. Those policy statements are preparation for a future
commercial path, not evidence that payment is available now.

### Trust material

Observed first-party proof includes:

- a concrete audience and workflow;
- a product screenshot;
- public release notes;
- public asset sizes and SHA-256 digests;
- update-manifest assets;
- local-storage and AI data-flow explanations;
- privacy, terms, and Google Limited-Use pages;
- the provider’s legal identity and contact.

Not observed:

- a customer testimonial or logo;
- a review, rating, or press citation;
- an active-user or customer count;
- an independent security review;
- a public Google verification result;
- an independent signing/notarization check;
- a benchmark or activation result.

## Customer and positioning hypothesis

| Question | Evidence-based answer | Classification |
| --- | --- | --- |
| Who is it for? | Apple Silicon Mac managers who coordinate projects through email and value local processing | Observed audience and platform |
| What job leads them here? | Turn email threads into tracked follow-ups, meeting preparation, projects, and replies | Observed promise |
| What is the lead benefit? | One private command center for mail and the work around it | Observed |
| Why this product? | Local Ollama AI, keyboard workflows, project context, Gmail plus broad IMAP | Observed mechanism |
| What is the category? | Private AI email client for macOS | Observed metadata |
| Emotional angle | Control, defense, ownership, competence, and calm | Inferred from observed castle and command language |
| What supports the promise? | Screenshot, technical specificity, release ledger, policies, and direct build | Observed first-party proof |
| What is the offer? | Free early-access disk image with future paid licensing left open | Observed |
| What action is requested? | Download the Mac client | Observed |
| What happens after download? | Explore sample data, skip, or connect Gmail/IMAP; actual order and completion remain untested | Public release-note evidence plus unknown behavior |

The audience is precise at the role level but broad at the product level:
email, projects, contacts, calendar, AI triage, meeting prep, and drafts all
compete to define first value. Actual customer composition and the strongest
job are unobservable.

## Claim boundary

### Gmail availability

The homepage says:

> Sign in with Google instantly.

The [v0.2.1 release
note](https://github.com/joanmarcriera/castellum-releases/releases/tag/v0.2.1)
says the earlier token exchange failed because a client secret was missing and
that, after the fix, people could still see:

> Access blocked: … developer-approved testers

because the Google consent screen was in testing mode. The July 17
[legal-pages commit](https://github.com/joanmarcriera/castellum-releases/commit/dfdc499d5d23261789586fb76627cf125da627a3)
says those pages were published to support Google OAuth verification. No
public release note says general access was approved afterward.

The current privacy page lists `gmail.readonly`, `gmail.modify`, and
`gmail.send`. Google’s current [scope
documentation](https://developers.google.com/workspace/gmail/api/auth/scopes)
classifies `gmail.readonly` and `gmail.modify` as restricted scopes requiring
restricted-scope verification for public use. Castellum’s verification and
security-assessment status is unobservable.

### Privacy shorthand

“Your mail never leaves your Mac” is too broad as a complete email data-flow
statement:

- mail still synchronizes with and sends through the chosen email provider;
- OAuth and IMAP credentials communicate with those providers;
- the website loads Google Fonts;
- update checks reach GitHub;
- optional cloud AI can send selected content to a chosen provider;
- future purchase/license handling involves the named processors.

The privacy policy states the narrower defensible claim: Castellum operates no
cloud server that receives mailbox content, and local AI is the default. It
also says optional cloud AI is off by default and user-enabled.

The homepage FAQ contains a likely copy error:

> Nothing is sent to us or any cloud AI unless you explicitly turn that off.

Taken literally, turning privacy off is the condition for no transmission.
The surrounding page and policy indicate the intended word was likely “on.”
This report preserves the text and does not silently repair it.

### Provider, AI, and release claims

- v0.2.2 release notes support the existence of guided provider configuration,
  but connection success across all providers was not tested.
- Microsoft 365 one-click sign-in is explicitly future work; Outlook is
  presented as manual IMAP today.
- The public page and releases claim signing and notarization. GitHub exposes
  asset digests, but the binary was not downloaded, so Gatekeeper acceptance,
  signature identity, and notarization were not independently verified.
- Ollama detection, model installation, summaries, triage, drafts, project
  linking, and calendar behavior were not run.
- GitHub asset counts establish requests, not successful installs or useful
  mail work.

## Acquisition implications

- The role-specific headline is repeatable and easy to qualify.
- The direct download removes pre-install account and payment friction.
- No visible source parameter connects a channel to the GitHub asset, and
  GitHub’s counter stops at an unqualified request.
- The manager message is stronger than the broad private-AI category, but the
  page still offers many potential first-value jobs.
- Public access preceded a clean launch build and generally available Gmail
  authorization.
- Trust is weakened when absolute privacy and compatibility copy needs policy
  or release-note qualification.
- Tecotype should adapt the audience discipline, concrete product screenshot,
  and dependency disclosure. It should publish only release-accurate provider,
  privacy, distribution, and feature claims after its own release gate.
