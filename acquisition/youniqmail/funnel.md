# YouniqMail funnel

Research date: **2026-07-17**

Scope boundary: **public, unauthenticated surfaces only**

No consent preference was saved. No form was submitted. No direct artifact was
followed or fetched. No client was downloaded, installed, or opened. No mailbox
was connected, and no payment path exists to inspect.

## Current funnel summary

```text
search, Reddit, listing, newsletter, or direct visit
→ blocking consent modal
→ homepage hero and beta download section
→ one of six direct artifacts or an optional Brevo form
→ first-party platform click event
→ static WordPress artifact URL
→ install and account connection unobserved
→ optional public forum or feedback survey
→ future premium offer unpriced and unavailable
```

The current funnel is materially more open than the alpha funnel:

```text
alpha interest
→ email signup
→ newsletter/privacy acceptance
→ double confirmation
→ emailed download link
→ artifact
```

## Stage 0: first visit and consent

At 1280 × 720, the first rendered state was a centered Borlabs **Privacy
Preference** modal over a dimmed hero.

| Group or service | Initial state |
| --- | --- |
| Essential | On, locked |
| Statistics | Off |
| Marketing | Off |
| Google Analytics | Off |
| LinkedIn Insight Tag | Off |
| Reddit Pixel | Off |
| X Pixel | Off |

Opening the individual list did not change or save anything.

This is transparent consent behavior, but it means the privacy message and
download CTA are not the first unobstructed interaction.

## Stage 1: offer and primary action

The visible offer is:

- Public beta.
- Free during alpha and beta.
- Windows, Apple Silicon macOS, and Linux.
- v0.9.0 dated July 13, 2026.
- Future freemium model with a paid premium tier.

The header `Download` link only moves to `#download`. It does not open an
account, store, or checkout.

The platform section exposes six direct choices:

| Platform artifact | Public filename | Public response metadata |
| --- | --- | ---: |
| macOS ARM64 DMG | `youniqmail-0-9-0-arm64.dmg` | 152,099,657 bytes |
| Windows EXE | `youniqmail-0-9-0-.exe` | 120,459,848 bytes |
| Debian AMD64 | `youniqmail-0-9-0-linux-amd64.deb` | 113,040,228 bytes |
| Debian ARM64 | `youniqmail-0-9-0-linux-arm64.deb` | 107,831,244 bytes |
| AppImage ARM64 | `youniqmail-0-9-0-linux-arm64.appimage` | 155,841,293 bytes |
| AppImage x86_64 | `youniqmail-0-9-0-linux-x86_64.appimage` | 155,299,704 bytes |

Public header checks returned status 200 for all six. The artifacts themselves
were not requested.

The page does not state:

- Minimum operating-system versions.
- Disk-space expectation after local mail storage.
- Checksum.
- Code-signing, notarization, or Windows signing status.
- Whether the beta auto-updates.
- Whether old builds remain available.

## Stage 2: direct-download measurement

Selecting a platform button is designed to send a same-site asynchronous event
before navigation:

```text
POST /wp-admin/admin-ajax.php
action=ebct_track_click
button_id=<platform track ID>
```

The six button IDs are stable and platform-specific. They can answer “which
button was selected?” but not:

- Which source caused the visit.
- Whether the response completed.
- Whether the file was opened.
- Whether the client installed.
- Whether a mailbox connected.
- Whether the user returned.

The static artifact URLs have no UTM or referral token. Some listing links
carry attribution on the homepage visit, but that parameter is not embedded in
the artifact URL.

No public click totals were exposed.

## Stage 3: optional email forms

The current homepage contains two Brevo-backed forms:

1. `Brevo get download form`.
2. `Brevo signup form`.

Each includes:

- An email field.
- A required acceptance checkbox combining newsletter consent and the privacy
  statement.
- A disclosure that personal information is transferred to Brevo.

No form was submitted.

Because direct artifacts are already in the public DOM, neither form is a
technical download prerequisite. The “get download” name can nevertheless
suggest that the old gate still matters.

This produces two parallel paths:

```text
homepage → direct artifact
```

and:

```text
homepage → Brevo consent → email follow-up → artifact or updates
```

The public page does not state whether the two forms add people to the same
list, apply the same tags, or produce different email sequences.

## Stage 4: artifact handoff

The files are hosted under YouniqMail's WordPress uploads path rather than:

- An app store.
- GitHub Releases.
- A dedicated download service.
- A signed, expiring URL.

This reduces account friction and keeps the handoff first-party.

The two AppImage responses lacked explicit `Content-Type` and
`Content-Disposition` headers in the public header check. A Reddit commenter
reported that Linux links displayed binary content and required a save-link
workaround. This is a plausible platform-specific conversion defect.

The DEB, Windows, and macOS artifacts had conventional metadata in the public
header check. Installation behavior was not tested.

## Stage 5: installation and mailbox connection

The homepage says the client supports:

- Standard IMAP and SMTP.
- Gmail.
- iCloud.
- Yahoo.
- GMX and WEB.DE.
- Other preconfigured providers.

Microsoft is described as future work.

The [app privacy policy](https://youniqmail.com/app-privacy-policy/) says
credentials use the operating system's secure storage and that message/account
data travels only between the device and the user's provider.

No public walk establishes:

- Gatekeeper, SmartScreen, or Linux execution behavior.
- Whether an in-app account or license is requested.
- OAuth versus app-password paths by provider.
- Gmail verification state or scopes.
- First-sync duration and progress.
- Mailbox-size or storage behavior.
- Default remote-image behavior.
- First useful search, triage, reply, rule, or customization.
- Error recovery.

These stages are deliberately left untested.

## Stage 6: feedback loop

There are two visible feedback routes.

### Public forum

The [feedback forum](https://feedback.youniqmail.com/) contains release notes,
feature requests, bug reports, and maker replies. Seventeen discussions were
created by non-maker accounts.

This is credible self-reported evidence consistent with people crossing
download, install, and meaningful-use stages. It is not independently verified
and does not provide a denominator or retained-use rate.

### First-party survey

The [feedback form](https://youniqmail.com/feedback-form/) asks:

- Whether the client was downloaded.
- Whether it is still being used.
- Frequency from installed-but-not-used to almost daily.
- Reasons for discontinuing.
- Likes, dislikes, missing features, and current client.
- Country and optional email.

All substantive fields appeared optional. No survey was submitted.

The survey design correctly separates:

```text
download
→ current use
→ frequency
→ reason for stopping
```

Public response counts and outcomes are unavailable.

## Stage 7: activation evidence

| Funnel stage | Public evidence | What remains unknown |
| --- | --- | --- |
| Visit | Live page, search result, and public referrals | Visitors and source mix |
| Consent | Initial state observed; optional services Off | Consent rates and effect on exit |
| Download intent | First-party platform event exists | Event totals and unique people |
| Artifact response | Six public 200 responses and sizes | Completed downloads |
| Install | Specific self-reported feedback threads are consistent with installs | Install count and failure rate |
| Account connection | Proton Mail and account-related issue details imply attempts | Completion rate and provider mix |
| Meaningful use | Reply, attachment, thread, signature, image, and UI issues | First-value rate |
| Continued use | One Reddit tester praised the macOS client; survey asks frequency | Cohort retention and duration |
| Payment intent | One commenter said they would happily pay; others debated subscription | Completed payment |
| Revenue | No checkout or public premium tier | Entirely unknown |

The forum is the only public source that crosses from intention into credible
usage detail. Even there, an issue report is not retention.

## Stage 8: price and payment

The homepage FAQ says:

- Premium pricing will be announced soon.
- Beta and alpha are free.
- An early-bird discount is planned.
- A subscription and freemium model are intended.

In an April Reddit reply, the founder also considered:

- One-time purchase.
- One-time purchase plus an update fee.
- Subscription.

The current homepage still uses subscription language. No decision beyond
future freemium is publicly complete.

There is no observed:

- Pricing page.
- Plan comparison.
- License endpoint.
- Checkout.
- Tax handling.
- Account portal.
- Refund policy for the future premium tier.
- Successful purchase.

The funnel currently ends at beta use and feedback.

## Historical gated funnel

### Waitlist

The [August 2025 archive](https://web.archive.org/web/20250818024847/https://youniqmail.com/)
showed:

```text
in development
→ Join waitlist
→ email plus newsletter/privacy acceptance
→ Brevo
→ updates and future alpha
```

### Alpha download gate

The [March 14, 2026 archive](https://web.archive.org/web/20260314223626/https://youniqmail.com/)
showed public beta v0.5.1 but still required:

```text
enter email
→ accept newsletter/privacy statement
→ confirm email
→ receive download link
```

The still-public
[newsletter signup confirmation page](https://youniqmail.com/newsletter-signup/)
is `noindex` and says the download link is sent immediately after email
confirmation.

The [newsletter thank-you page](https://youniqmail.com/newsletter-thank-you/)
then points to the feedback form and download page.

The old [alpha download page](https://youniqmail.com/alpha-app-download/) is
still public and currently mirrors the v0.9.0 artifacts rather than preserving
an alpha build.

### Gate removal

On March 29, the maker
[announced the gate removal](https://www.reddit.com/r/YouniqMail/comments/1s6gwd3/youniqmail_removed_it_gates/).
The stated reasons were:

- Alpha needed committed testers and direct conversations.
- Beta needed wider feedback.
- The gate had become friction.
- Requiring an email address contradicted the privacy promise.

This is a rare explicit account of funnel intent. It does not provide before
and after conversion or retention rates.

## Instrumentation gaps

The public configuration can measure:

- Consented website analytics.
- Consented Reddit, X, and LinkedIn marketing events.
- Platform download-button clicks.
- Brevo form submissions and email engagement.
- Public feedback activity.

It cannot publicly demonstrate a joined journey from:

```text
source
→ visit
→ artifact complete
→ install
→ account connected
→ first useful action
→ next-day return
→ paid conversion
```

Server-side or private app measurement could exist, but the app privacy policy
says there is no client analytics sent to YouniqMail. The public feedback form
appears to substitute voluntary research for silent product telemetry.

## Tecotype implications

- An email gate is especially costly when privacy is part of the promise.
- Direct download should not launch until Tecotype has a signed, notarized,
  updateable supported release, clear system requirements, first-run/no-account
  onboarding, licensing, payment, and a chosen privacy-compatible activation
  measure.
- Artifact request, install, account connection, first value, and return must
  remain separate.
- A voluntary feedback loop can provide qualitative evidence without
  collecting message content.
- Tecotype should preserve source through the download handoff while avoiding
  query text, subject, sender, recipient, or message-content collection.
- Platform packaging and response headers are acquisition details: a broken
  Linux or macOS handoff can erase the value of community attention.
- Tecotype must not describe public download, payment, MCP, agent automation,
  or post-release Split Inbox work as current until those release gates are
  actually satisfied.
