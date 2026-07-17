# Locker history

Research date: **2026-07-17**

The history is reconstructed from the sole Wayback capture, a search-indexed
earlier page state, current Vercel responses, GitHub release metadata, the
public changelog, legal pages, and the founder Reddit thread.

Observed changes do not reveal why the maker changed the message or whether
any version performed better.

## Timeline

| Date | Observed state | Evidence boundary |
| --- | --- | --- |
| 2025-07-16 | `inbox.locker` redirected to `/lander` | Sole successful Wayback homepage capture; current product not present |
| Before current paid page, exact date unknown | “Email, with the cloud taken back out” page requested one launch notification and described an open-source MCP/approval product | Search-indexed and cached page state; publication dates unavailable |
| 2026-06-23 | Public v0.1.0 and v0.2.0 releases | GitHub release metadata |
| 2026-06-24 | Public v0.3.0 release | GitHub release metadata |
| 2026-06-24 | Founder requested beta testers in r/software and offered free lifetime keys | Public Reddit thread |
| Current capture | Private-AI homepage, direct download, five keys shown as claimed, $39.99 founder checkout handoff, and 10 of 10 paid spots shown left | Rendered page and checkout |
| Current capture | v0.4.0 labeled “Next release · in testing” | Public changelog |
| Future, date unknown | Separate browser-based product with different privacy model and unannounced pricing | Privacy and terms; not available |

## Domain before the email product

The Wayback CDX index returned one successful homepage capture:

[July 16, 2025](https://web.archive.org/web/20250716124225/http://inbox.locker/)

Its entire response redirected the browser to:

```text
/lander
```

No archived `/lander` page was available. This proves only that the domain had
a generic landing route in 2025. It does not identify the owner, product, or
offer at that time.

This boundary matters because several backlink rows were first seen between
November 2025 and February 2026. They predate the current June 2026 release and
must not be credited to the email product.

## Earlier indexed positioning

Search still exposed an earlier page title:

> Locker — Email, with the cloud taken back out.

The cached page described:

- A Mac email client using IMAP or Apple Mail.
- MCP access for Claude Code, Cursor, Zed, and scripts.
- Draft and action approval before anything leaves the machine.
- An audit log, local engine, rules, and tool registry.
- An open-source repository link.
- A one-time “tell me when this is installable” email notification.

It explicitly separated:

- Built work.
- “Building next.”
- Planned work.
- Ideas.

The indexed source link did not resolve to the current public release
repository during this research, and the current page no longer links to
source. The visible public GitHub repository contains release assets rather
than product source and has no declared license.

The exact capture and replacement dates are unknown. Search-title lag is not a
traffic or conversion result.

## Public release sequence

### v0.1.0, June 23

Publisher-authored public notes call it the first Apple Silicon build and say
it is signed and notarized.

### v0.2.0, June 23

Public notes add:

- Automatic updates.
- A natural-language command bar.
- Sent.
- Paste and mailbox-removal fixes.
- A warm on-device model.
- A wired search bar.
- Better marketing-message classification.

The v0.2.0 release text also calls the download signed and notarized. This and
the v0.1.0 wording are publisher-authored claims: no disk image was fetched,
and signing/notarization was not independently verified.

### v0.3.0, June 24

Public notes add:

- Search by meaning.
- Local model processing.
- Automatic local network-port selection.

The disk image grew from roughly 113 MB to roughly 159 MB.

### v0.4.0, current “in testing”

The changelog lists:

- Apple Mail work-account connection.
- Attachments.
- Reply-all, forwarding, Cc, and Bcc.
- Smart notifications.
- Rules, tags, and reminders.
- Per-account inbox view and polish.

This list is future relative to the current public v0.3.0 asset.

## Offer evolution

The earlier indexed page asked for a one-time launch notification.

The current page removes that email gate and provides:

- Immediate disk-image download.
- Five free public license keys, now shown as claimed.
- Direct maker contact for testing.
- $39.99 founder lifetime purchase.
- A published transition to $70 lifetime and then $129 for four years of
  updates.
- Polar checkout and email-delivered key activation.

This is a change from demand collection to simultaneous trial and purchase.
The public counters do not establish conversion.

## Message evolution

The indexed page led with:

- Local ownership.
- MCP.
- Bring-your-own agents and tools.
- Approval and audit.
- Open source.

The current page leads with:

- “Private AI inbox.”
- A bundled on-device model.
- Meaning search.
- Protection and defense.
- Anti-cloud and anti-subscription comparisons.
- A large list of consumer-facing assistant features.

The approval idea remains, but MCP, source access, tool registration, and the
audit log are no longer prominent on the current public page.

## Current inconsistency

The earlier page was unusually explicit about build status. The current page
is less clear:

- It presents notifications, rules, reminders, and work-account behavior as
  things the app does.
- The changelog places overlapping work in v0.4.0 “in testing.”
- Other homepage features do not appear in the public release notes.

That inconsistency prevents feature-level acquisition conclusions. It is not
possible to tell whether a visitor downloaded because of a feature actually
present in v0.3.0, an in-testing feature, or a general privacy promise.

## Acquisition interpretation

Observed:

- The product moved quickly from first release to meaning search.
- The maker paired the public download with a feedback request.
- The homepage showed five free keys as claimed.
- A paid checkout handoff exists; no transaction was attempted.
- The leading message changed substantially from technical openness and MCP
  to bundled local AI and a broad assistant promise.

Unobservable:

- Waitlist size.
- Reason for replacing the earlier page.
- Which message produced more visits or downloads.
- Source of each free-key claim.
- Unique installs.
- Mailbox connection.
- Retention.
- Paid conversion.

The useful Tecotype lesson is not to imitate the sequence. It is to version
message experiments against a release-accurate capability set, then preserve
source and activation evidence across each change.
