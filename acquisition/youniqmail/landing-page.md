# YouniqMail landing-page research

Capture date: **2026-07-17**

URL: [https://youniqmail.com/](https://youniqmail.com/)

Rendered capture: **desktop in-app browser, 1280 × 720 CSS pixels, DPR 2;
logged out; no consent saved, form submitted, or artifact followed**

The page identifies the product as **Beta Phase**, version **v0.9.0**, dated
**13 July 2026**. Its main product screenshot is captioned **7 March 2026**, so
the hero and download state are current while the visual proof is older than
the release.

## First rendered state

The first load was blocked by a centered Borlabs **Privacy Preference** modal
over a dimmed hero.

- `Essential` was pre-checked and disabled.
- `Statistics` and `Marketing` were unchecked.
- Opening `Individual Preferences`, without changing or saving anything,
  showed Google Analytics under Statistics.
- LinkedIn Insight Tag, Reddit Pixel, and X Pixel appeared under Marketing.
- All four optional services displayed `Off`.

This proves a consent-gated measurement configuration and a blocking
first-visit experience. It does not prove that an optional service has ever
received data or that an advertising campaign is active.

## Technical surface

### Site operation

The live page exposed:

- WordPress.
- Elementor and Elementor Pro.
- The Hello Elementor theme.
- WP Rocket caching/minification.
- Rank Math SEO.
- Borlabs Cookie.
- Wordfence references in the essential consent group.
- Apache hosting; the privacy policy names All-Inkl as the host.

The response included:

- HSTS.
- `X-Frame-Options: SAMEORIGIN`.
- `X-Content-Type-Options: nosniff`.
- `Referrer-Policy: strict-origin-when-cross-origin`.
- A restrictive permissions policy.
- A Content Security Policy.

These headers are useful public trust signals. They are not an independent
security review of the desktop client.

### Metadata

| Field | Observed value |
| --- | --- |
| HTML language | `en-US` |
| Title | `YouniqMail - Customizable and Privacy-Safe Email Client` |
| Description | `YouniqMail isn't for everyone — it's for anyone who finally wants to adapt their inbox to their workstyle & workflow. New Email Client in Development.` |
| Canonical | `https://youniqmail.com/` |
| Robots meta | `index, follow` |
| Twitter account | `@YouniqMail` |
| Twitter card | `summary_large_image` |
| Structured data | Organization, WebSite, AboutPage, SearchAction |
| Structured publication date | 2025-07-13 |
| Structured modified date | 2026-04-17 |

The live response was modified on July 17 and advertises v0.9.0 from July 13,
so the structured `dateModified` is stale. The meta description also still
says “in development” while the visible page says public beta.

The structured `sameAs` array includes X, LinkedIn, and an older Reddit profile;
the visible footer instead links to the r/YouniqMail subreddit. This looks like
metadata maintenance lag, not evidence about acquisition performance.

### Consent and measurement configuration

| Service | Public identifier | Consent group | Rendered default |
| --- | --- | --- | --- |
| Google Analytics 4 | `G-RVH4G4D5NL` | Statistics | Off |
| Reddit Pixel | `a2_hpve6q7semni` | Marketing | Off |
| X Pixel | `qlk7q` | Marketing | Off |
| LinkedIn Insight Tag | Partner `8782385` | Marketing | Off |

The page sets Google consent-mode defaults and configures anonymized IP
handling for GA4. The public privacy policy also discusses other marketing and
site services, but Meta, Pinterest, and tawk.to were not independently observed
in the current rendered state or current Borlabs service list.

The Content Security Policy visibly allows Google/GA destinations. It did not
obviously allow every configured marketing-pixel domain. Whether all optional
pixels load correctly after consent was not tested because no preference was
saved.

### First-party download click measurement

Each of the six artifact links has a public `data-track-id`:

| Platform | Track ID |
| --- | --- |
| macOS Apple Silicon | `mac-download` |
| Windows | `windows-download` |
| Linux Debian AMD64 | `linux-amd-deb-download` |
| Linux Debian ARM64 | `linux-arm-deb-download` |
| Linux AppImage ARM64 | `linux-arm-appimage-download` |
| Linux AppImage x86_64 | `linux-x86-appimage-download` |

An inline handler posts the selected ID to:

```text
/wp-admin/admin-ajax.php
```

with:

```text
action=ebct_track_click
button_id=<public track ID>
```

No click was made. The code establishes platform-button measurement
capability, not a public download total or a unique-install count.

## Public actions

| Action | Destination | Friction | Source tagging |
| --- | --- | --- | --- |
| Header `Download` | Same-page `#download` section | None | None |
| macOS download | First-party ARM64 DMG | Direct artifact | Platform click ID only |
| Windows download | First-party EXE | Direct artifact | Platform click ID only |
| Four Linux downloads | First-party DEB or AppImage | Direct artifact | Platform click ID only |
| `Join feedback platform & development updates` | `feedback.youniqmail.com` | Public forum | None observed |
| `Get download` Brevo form | Email plus required newsletter/privacy checkbox | Optional beside direct links | Form context only |
| Newsletter form | Email plus required newsletter/privacy checkbox | Optional | Form context only |
| Feedback form | First-party survey | All substantive fields optional | None observed |

All six artifact links are public WordPress upload URLs. They do not contain a
referral source, campaign, or signed token. No artifact was fetched.

The page did not show:

- Public checksums.
- A signing or notarization statement.
- Store distribution.
- Public artifact-request counts.
- An account, license, or checkout requirement.

Direct download and two email forms coexist. A visitor can download without
using either form, but the redundant “get download” form preserves language
from the earlier gated funnel and may make that fact less obvious.

## Observed message

### Hero

The visible hero says:

> Your email (client). Your rules. Your privacy.

> No more compromises: the email client you control – customizable, private,
> modern.

The download section immediately identifies the product as a desktop email
client in beta and gives platform-specific artifacts.

### Core positioning

The page then leads with:

> YouniqMail isn't for everyone — it's for anyone who finally wants to adapt
> their inbox to their work style and workflow, without compromising your
> privacy

Its mechanism is:

- Direct connection from the device to the user's email provider.
- Local storage rather than a YouniqMail mailbox service.
- IMAP and SMTP, with current presets for Gmail, iCloud, Yahoo, GMX, WEB.DE,
  and others.
- A highly configurable interface and workflow.
- No YouniqMail cloud account.

The page correctly makes a parenthetical exception for the website and public
email-tool servers. Its shorter diagrams and slogans are less precise.

### Feature breadth

The current page claims:

- Tags and Apple/Spark-compatible flags.
- Notes attached to messages.
- Search and filters.
- Snooze.
- Attachment previews, resizing, and a separate attachment manager.
- Contact management.
- Automation rules.
- Trello, Asana, Notion, CalDAV, webhook, and shell-script integrations.
- Configurable keyboard shortcuts and presets.
- A dashboard with 18+ widgets and four presets.
- Experimental PGP, with S/MIME to follow.
- Phishing protection.
- Undo send, signatures, export/import, contact sync, block rules, local
  folders, BIMI, recipient intelligence, and other functions.

The public [v0.9.0 release note](https://feedback.youniqmail.com/d/53-beta-update-v090)
separately documents maker-published work on aliases, forgotten attachment
warnings, Markdown, spellcheck, local statistics, faster sync, database
cleanup, and extensive search improvements.

These are first-party product and release claims. No local artifact was
installed, and no independent feature or security audit was found.

One visible quality defect is that the **Phishing protection & detection**
description repeats the PGP/S/MIME paragraph rather than describing phishing
behavior.

## Offer

Observed:

- Public alpha and beta access is free.
- A “simple Freemium model” is promised.
- Premium is described as a subscription.
- The price will be announced later.
- A beta or early-bird discount is promised.

Unobserved:

- Free-versus-premium feature boundary.
- Billing interval other than the word subscription.
- Checkout.
- Trial after the beta.
- License delivery or validation.
- Refund policy for a future paid plan.
- Paid customer or revenue evidence.

The page asks for money rhetorically—“We just want your money and feedback”—
before it has a public price or payment path.

## Trust material

Observed trust material includes:

- A named founder and origin story.
- Direct-provider and local-database explanations.
- Provider and platform compatibility details.
- A long public changelog.
- A public feedback forum and feedback form.
- App-specific privacy, EULA, and terms pages.
- A current version and date.
- Concrete screenshots and feature examples.

The page showed no:

- Customer testimonial.
- Customer logo.
- Active-user count.
- Download count.
- Review score.
- Paid-customer count.
- Security audit.
- Public source repository.
- Benchmark.

One non-maker Reddit account self-reported testing the client on macOS and said
they would happily pay. That is a useful individual signal, not independently
verified use, page-level social proof, or a completed transaction.

## Customer and positioning hypothesis

| Question | Evidence | Classification |
| --- | --- | --- |
| Who is it for? | Desktop users on Windows, macOS, or Linux; founder says current users are mainly techies, power users, and privacy enthusiasts | Observed platform; first-party audience statement |
| What job leads them here? | Adapt the inbox to a personal workflow, manage several providers, search, organize, automate, and avoid a client vendor's mail cloud | Observed promise |
| What is the lead benefit? | Control through customization without a YouniqMail mailbox intermediary | Observed |
| What is the mechanism? | Local database, direct provider connection, broad settings, rules, and integrations | Observed claim |
| What is the category? | Customizable, privacy-safe, local-first desktop email client | Observed metadata and copy |
| What is the emotional angle? | Autonomy, privacy, ownership, flexibility, and resistance to forced workflows | Inferred from copy |
| What supports the promise? | Screenshots, feature catalogue, changelog, direct beta, and public feedback | Observed |
| What is the offer? | Free public beta now; future freemium subscription | Observed |
| What action is requested? | Download, optionally join Brevo updates, or give feedback | Observed |
| What happens after download? | Install and connect an existing account | Inferred from product model; unwalked |

## Privacy and legal claim boundary

### App versus marketing site

The [app privacy policy](https://youniqmail.com/app-privacy-policy/) says:

- The desktop app does not send data to the developer.
- Account and message data go only to the user's provider.
- IMAP, SMTP, Gmail, and iCloud credentials use the operating system's native
  secure storage.
- Messages, names, notes, tags, and attachments remain local.
- Logs are not sent to YouniqMail.

The current marketing site separately has consent management, GA4
configuration, optional marketing pixels, Brevo forms, and first-party
download-button counting. Therefore “zero tracking” is defensible only as an
app claim with a precise boundary, not as a description of every YouniqMail
surface.

### Conflicting public legal text

The [app EULA](https://youniqmail.com/app-eula/) includes boilerplate saying
the licensor may access or adjust downloaded content and personal information
and may periodically collect technical, device, and application data. That
conflicts with the app privacy policy and homepage.

The [app terms](https://youniqmail.com/app-terms-and-conditions/) mention app
stores, Google Play, user accounts, and user content even though the observed
distribution is direct desktop download without a YouniqMail account.

The app privacy policy also contains an “Android device” reference despite the
desktop-only platform statement. These look like unreconciled templates. They
are not proof that the client collects the described data, but they weaken the
public trust contract.

### Security verification

The homepage and external listings claim local encryption and no developer
server in the mail path. The public terms identify the app as proprietary and
prohibit reverse engineering. No public source code or independent security
assessment was observed.

Accordingly:

- Direct-provider architecture is an observed first-party claim.
- Public release notes establish maker-described features.
- Security and privacy behavior inside the binary remains unverified.
- The website and public tools are explicit server exceptions.
- Email still travels through each user's provider; “email never leaves the
  device” would be inaccurate.

## Acquisition implications

- The page makes beta trial materially easier than the old email gate.
- The blocking consent modal delays the product story on first load, though it
  clearly keeps optional services off.
- Platform click IDs can compare download-button activity but cannot connect a
  Reddit post or directory listing to install and retention.
- The broad feature list shows ambition but dilutes the sharper,
  demonstrable local-first/customization mechanism.
- Privacy is explained more concretely than on many competitor pages, but
  stale metadata and conflicting legal boilerplate create avoidable doubt.
- Tecotype should adapt the explicit provider boundary, version/date clarity,
  and public feedback loop. It should not copy “zero tracking” as a whole-site
  claim, redundant download forms, or a feature catalogue that exceeds the
  release being tested.
