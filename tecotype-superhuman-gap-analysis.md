# Tecotype gaps to become a strong Superhuman contender

**Date:** 2026-07-20  
**Scope:** Superhuman Mail customers only; Tecotype evaluated against the
review-derived switching requirements in
[`superhuman-mail-customer-research.md`](./superhuman-mail-customer-research.md).  
**Tecotype snapshot:** current `../tecotype` working tree at
`df044a3807fb`, including uncommitted local changes present during the audit.

The customer baseline is the preceding multi-platform research corpus: current
official product/help/security material; G2, Capterra, TrustRadius, Product Hunt
and app-store reviews; Reddit and LinkedIn first-person accounts; independent
long-term reviews and workflow essays; comparison/churn discussions; and six
DataForSEO backlink-discovery passes. Backlinks were used to find overlooked
surfaces, not as customer or sentiment counts.

## Executive verdict

Tecotype has a credible differentiated core, but it is not yet ready to replace
Superhuman—or any primary professional email client.

The largest gap is not AI. It is **switch confidence**: a user must be able to
reply, attach and forward files, trust rendering and threading, recover drafts,
and complete ordinary message-level actions without returning to Gmail,
Outlook, or another client. Today that fallback-free loop is not complete.

The most serious verified defect is that Tecotype cannot currently send a real
reply:

- inline Reply's **Send** and **Send later** actions discard the quick reply;
- expanding the reply carries only body content, not account, recipients,
  subject, parent message, or thread context;
- generated MIME lacks `In-Reply-To` and `References`; and
- Gmail submission deliberately sends without a Gmail thread ID until reply
  threading is implemented.

Outgoing attachments are also absent. These two facts alone prevent a
Superhuman switch trial.

Tecotype should pursue a **narrow strong-contender position**, not broad
Superhuman parity:

> The private, desktop-first mail client for keyboard-oriented professionals
> managing several Gmail and IMAP accounts—one unified inbox, cross-account
> local exact and meaning-based search, with focused triage and, for scanners,
> a proposed optional preview-pane mode.

That position rests on three current foundations and one proposed segment
wedge:

1. a true unified view across accounts, which Superhuman does not provide;
2. Gmail plus generic IMAP/provider breadth;
3. local exact search plus multilingual semantic search across accounts; and
4. **proposed:** optional list-plus-reader triage for people who need persistent
   list context.

“Calm control” should remain the experience and retention promise. It is not
strong enough as the acquisition reason by itself: Superhuman customers already
describe Superhuman as calming and relieving. Price is similarly useful but
insufficient. A lower price may earn a trial; it does not survive broken reply,
attachments, rendering, or mobile/provider discontinuity.

## What Tecotype already has

These are meaningful assets rather than speculative roadmap claims.

| Capability                           | Verified state                                                                                                                                       | Competitive value                                                                                              |
| ------------------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------- |
| Unified multi-account views          | Split and ordinary views can operate across accounts, with account-specific filtering                                                                | Direct answer to a repeated Superhuman complaint                                                               |
| Gmail and generic IMAP               | Gmail OAuth/API plus generic IMAP; SMTP sending core exists                                                                                          | Reaches Fastmail, iCloud, self-hosted, and other provider users Superhuman excludes, subject to provider setup |
| Local search                         | Local full-text search plus optional on-device multilingual semantic retrieval                                                                       | Tecotype's strongest technical and privacy wedge                                                               |
| Keyboard-oriented shell              | Direct shortcuts, command palette, thread navigation, archive/read/spam/trash/reminder commands                                                      | Correct foundation for Superhuman's original power-user cohort                                                 |
| Split Inbox engine                   | Cross-account TQL rules, incremental evaluation, counters, and editing are implemented                                                               | Powerful organization foundation                                                                               |
| Reminders                            | Thread resurfacing, reply-aware cancellation, and lifecycle state exist                                                                              | Covers a central “handle it later” loop                                                                        |
| Durable sending core                 | Local drafts/outbox, Gmail API send, SMTP send, Sent APPEND, scheduled send, and a 15-second delayed-execution mechanism that can support Undo exist | Strong foundation once reply, user-visible send safety, and attachment fidelity are completed                  |
| Quiet interface and local processing | Mail is locally stored; semantic search runs on-device                                                                                               | Coherent product character and a credible privacy direction                                                    |

The problem is not a lack of promising components. It is that several missing
links sit directly in the primary email loop.

## Priority definitions

- **G0 — primary-client gate:** do not invite switchers until it passes.
- **G1 — narrow-contender gate:** required to win and retain the recommended
  desktop-first, multi-account ICP.
- **G2 — addressable-market gate:** required for broader Superhuman
  replacement claims or particular professional segments.
- **G3 — later differentiation:** useful after the daily loop is trustworthy.

## Gap map

### G0: primary-client gates

| Gap                                           | Verified Tecotype state                                                                                                                                                                                                                                                                                                                                                                                                                                                      | Why it causes immediate disappointment                                                                                                                    | Required outcome                                                                                                                                                                                                                                                                                                                                                                                                    |
| --------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| True reply, reply all, forward, and threading | **Broken/absent.** Quick Reply Send and Send later discard. Expanded reply loses context. Outbound MIME and Gmail submit do not carry reply-threading data.                                                                                                                                                                                                                                                                                                                  | A user cannot conduct an ordinary conversation without falling back to another client. Incorrect threading also damages recipients' inboxes.              | Reply/reply-all/forward from every message; correct recipients and identity; `In-Reply-To`/`References`; Gmail and IMAP threading; quoted-history control; forward/re-include attachments; send-and-archive; undo and send later.                                                                                                                                                                                   |
| Outgoing attachment lifecycle                 | **Absent.** Incoming cards and Save As exist; compose/outbox contain no attachment model and sending documentation excludes attachments from v1.                                                                                                                                                                                                                                                                                                                             | Professional users regularly send files. A missing attach button is an instant trial failure.                                                             | Add, remove, drag/drop, paste and inline images; provider limits; upload/progress/failure; forward/reply originals; durable local references; offline queue semantics; filename preservation.                                                                                                                                                                                                                       |
| HTML and thread fidelity                      | **Partial.** HTML is clipped at 300,000 characters, sender styling is not faithfully preserved in known Outlook/Word cases, Tecotype injects layout styles, and there is no verified “view original” fallback.                                                                                                                                                                                                                                                               | Premium-client users will not tolerate broken receipts, signatures, newsletters, tables, or long threads.                                                 | A representative Gmail/Outlook corpus with no silent clipping; predictable quote folding; preserved sender layout; safe original-message fallback; long-thread performance and deterministic chronology.                                                                                                                                                                                                            |
| Remote-image privacy and rendering boundary   | **Partial and inconsistent with the privacy promise.** The current iframe permits direct HTTPS image loading, revealing IP address and timing to remote senders. The selected scriptless/network-controlled design is not implemented.                                                                                                                                                                                                                                       | Tracking-pixel exposure undermines “private by design” at the moment users evaluate trust.                                                                | Block remote images by default or fetch through an explicit privacy-preserving policy; clear per-message/per-sender choice; scriptless visible frame; no hidden external fetches; precise explanation.                                                                                                                                                                                                              |
| Professional compose basics                   | **Partial.** Basic rich text, colors, links, lists and quotes exist. Signatures, snippets/templates, tables, font controls, inline images, and attachment composition are absent.                                                                                                                                                                                                                                                                                            | Users fall back to Gmail/Outlook for common business mail, destroying habit formation.                                                                    | Multiple per-account/alias signatures; reliable paste; tables and inline images; formatting that survives Gmail/Outlook; recipient/identity validation; accessible plain-text alternative.                                                                                                                                                                                                                          |
| Draft integrity and recovery                  | **Partly implemented; a loss risk needs testing.** Local drafts exist, but editor and persistence debounces plus actor close behavior do not show a verified final flush. Durable editing history is still planned.                                                                                                                                                                                                                                                          | One lost tail edit can end a premium-client trial.                                                                                                        | No content loss on close, crash, update, sleep, account switch, or network loss; durable local drafts; visible save state only when useful; recovery after process kill; reconnect safety.                                                                                                                                                                                                                          |
| Send safety and state visibility              | **Backend foundation, incomplete user contract.** Send uses a 15-second execution delay, but successful scheduling closes compose and no visible Undo Send affordance was found. Draft-list projection drops persisted error text, and no complete failed/retrying/unknown-delivery recovery surface was verified. Send Later is executed by a local worker, so by inference it cannot send while the device is off; sleep/background behavior is not yet a proven contract. | Superhuman users depend on Undo Send, Send Later and clear recovery. A hidden failure or unexpectedly unsent scheduled message breaks relationship trust. | Visible Undo after every send, restoring the exact draft; queued/sending/retrying/failed/unknown-delivery states; safe Edit/Retry/Discard; Send and Archive; duplicate-send protection. Preserve the local credential boundary: solve background delivery without moving mailbox access to Tecotype infrastructure where possible, and disclose unavoidable device-local scheduling limits before the user commits. |
| Message-level and provider-state fundamentals | **Partial.** Whole-thread archive/read/spam/trash/remind and navigation exist, but reply-all, forward and per-message move/delete/read plus complete Gmail-label/IMAP-folder mutation fidelity were not verified.                                                                                                                                                                                                                                                            | Complex threads require acting on one message without mutating the whole conversation. Losing provider state also makes fallback-client use unsafe.       | An explicit message-action surface distinct from thread actions, available by keyboard and pointer; preserve and reconcile target-ICP label/folder state across Gmail and IMAP.                                                                                                                                                                                                                                     |
| Database-at-rest protection                   | **Planned, not shipped.** Credentials are protected, but encrypted SQLite is a proposed release requirement; cache coverage also remains explicit work.                                                                                                                                                                                                                                                                                                                      | A local-first product stores more mailbox data locally. “Private” becomes weaker, not stronger, if the local store is left exposed.                       | Encrypted database/WAL/temp policy, encrypted or disabled caches, key loss behavior, no plaintext fallback, and independently testable claim boundaries.                                                                                                                                                                                                                                                            |
| Notification and design-partner readiness     | **Incomplete.** Desktop notifications/unread badge, first-run/no-account onboarding, provider preflight/error recovery, public distribution and real-provider release smoke tests are incomplete or remain on the pre-release list. The current release tooling targets Apple Silicon.                                                                                                                                                                                       | A daily client must reliably tell the user about important mail and be safe to connect, install, update and recover before even a design-partner trial.   | Quiet, configurable notifications; first-run and provider preflight; understandable backfill/reconnect state; a verified signed build/update path; recovery support; real Gmail and IMAP smoke tests.                                                                                                                                                                                                               |

### G1: gates for the recommended narrow contender

| Gap                                     | Verified Tecotype state                                                                                                                                                                                                                                                                      | Why it matters to the wedge                                                                                                                           | Required outcome                                                                                                                                                                                                                                      |
| --------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Optional persistent list + reader       | **Infrastructure exists, workflow does not.** The shell can render primary and secondary panes, but ordinary thread open uses the focused pane and replaces the list. Production code opens only compose/expanded quick reply in the secondary pane. Panes are fixed equal-width left/right. | Review evidence shows this is a hard adoption requirement for a meaningful scanner/monitoring cohort, including users who otherwise love Superhuman.  | Optional list+reader; right and below layouts; resizing; density; keyboard traversal; explicit mark-read behavior; stable selection; immediate toggle to Superhuman-like focused mode and auto-next. Do not force panes on everyone.                  |
| Instant, measured keyboard loop         | **Foundation exists; switch-grade performance is not yet demonstrated under realistic load.**                                                                                                                                                                                                | Superhuman loyalty is built around uninterrupted rhythm, not feature count.                                                                           | Instrument key-down-to-paint for open, archive, next, compose, send, split/account switch and search. Test low-end supported hardware, several accounts, long threads and a large archive. No loading modal or focus loss in the core loop.           |
| Deterministic search UX                 | **Strong engine, thin product contract.** Input is only query plus limit. Results are threads with no matching-message anchor, snippet/highlight, filters, operator UI or route explanation. Relevance controls eligibility; recency controls final order.                                   | Local semantic retrieval creates interest, but exact archive trust retains users. A user must understand why a result appeared and jump to the match. | Sender/recipient/account/date/folder/attachment filters and operators; exact literal/email handling; matching message, snippet and highlight; source/explanation for semantic results; stable relevance/recency controls; attachment filename search. |
| Approachable Split Inbox                | **Powerful backend, expert-oriented authoring.** All saved splits are active; there is no priority/enable state. The remaining approachability plan includes recipes, participant/account completion, paraphrases, match previews, traces and a guided builder.                              | Superhuman users value splits because they are easy to shape into VIP/client/team contexts. Raw query-language work is a tax for non-developers.      | Templates for VIP, client, newsletter, notification and account; guided conditions; instant preview and “why matched”; enable/reorder/priority; safe Main behavior; raw TQL as an advanced mode.                                                      |
| Snippets and obligation management      | **Absent beyond reminders/send later.** No reusable snippet library or “waiting for reply” queue exists. Reminders cancel when a reply arrives but do not create a reply-aware outbound follow-up.                                                                                           | Snippets and follow-up are deeply embedded switching costs for Superhuman's solo professionals.                                                       | Personal snippets with variables, formatting, recipients and attachments; quick insertion; import/export; “follow up if no reply”; awaiting-reply view; clear cancel/reschedule behavior.                                                             |
| Migration and reversible trial          | **Absent.** No Superhuman/Gmail/Outlook operating-state migration or guided recreation flow is verified.                                                                                                                                                                                     | Users are switching an email operating system, not merely connecting an inbox. Rebuilding keymaps, signatures, splits and snippets creates reversion. | Detect/offer familiar keymap; import what provider APIs expose; guided recreation for splits/snippets; identity test; explain non-migratable state; reversible trial; record every fallback task.                                                     |
| Sender/account safety                   | **Partial.** Accounts and sender fields exist, but no complete wrong-account/alias safeguard was verified.                                                                                                                                                                                   | A unified multi-account inbox increases the cost of identity mistakes.                                                                                | Make sending account unmistakable; recipient-domain and thread-account checks; alias/signature binding; warning when behavior is anomalous, without noisy confirmation on every send.                                                                 |
| Offline contract                        | **Promising but not release-proven.** Cached bodies, local search, drafts/outbox and queued mutations exist; attachments and remote resources remain network-dependent. Positioning correctly avoids claiming “fully offline.”                                                               | Local-first and unreliable-network use are core reasons to choose Tecotype.                                                                           | Publish and test an exact offline contract: read/search, triage, draft, attach, schedule, restart, queued state, reconnection conflicts and attachment availability.                                                                                  |
| Familiar keymap and complete speed loop | **Partial.** Many direct commands exist, but no verified Superhuman preset/remapping, complete shortcut sheet, Send and Archive, or fallback-free reply/send loop exists.                                                                                                                    | Muscle memory is one of Superhuman's strongest retention mechanisms. “Keyboard first” is not parity until the entire daily loop works.                | Superhuman-compatible preset during onboarding; remapping with conflict checks; contextual discovery; complete keyboard and pointer equivalents; auto-next and Send and Archive; no dropped keys or focus changes under sync load.                    |
| Out-of-office                           | **Absent.** No vacation-responder configuration or provider synchronization was found.                                                                                                                                                                                                       | Consultants, agency principals and travelers need this infrequently but cannot safely abandon the provider client without it.                         | Per-account behavior where the provider supports it; start/end time and time zone; internal/external audience where available; import existing state; preview/test; unmistakable active status.                                                       |
| Fallback-prevention controls            | **Incomplete.** Star, calendar-invite actions, print/PDF, `.eml` export and raw/original-message workflows are absent, post-release, or not verified as a complete user surface.                                                                                                             | These are occasional rather than constant, but each can force a supposedly switched user back to Gmail or another client.                             | Validate frequency with the target ICP, then ship the subset needed for a no-fallback task matrix. Safe View Original is already a G0 rendering requirement; never hide unsupported provider state.                                                   |

### G2: broader-market gates

| Gap                                            | Current state                                                                                                                                          | Strategic consequence                                                                                                                                                                                   |
| ---------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Microsoft 365/Outlook                          | Direct Outlook integration is post-release; no shipped Microsoft adapter was found.                                                                    | Tecotype cannot target Superhuman's current broad commercial or partner-sales ICP without it. This is the highest provider expansion priority after the narrow product is reliable.                     |
| Platform continuity                            | The current signed release target is Apple Silicon Mac; Intel/universal is deferred. Windows distribution is planned. Linux is not currently packaged. | Published Tecotype may support all desktop platforms, but today it cannot claim that. Finish Windows and Linux only after core behavior has one cross-provider conformance suite.                       |
| Mobile continuity                              | Mobile is out of Tecotype's scope.                                                                                                                     | This creates a permanent ceiling versus broad Superhuman use. Target desktop-dominant users who accept provider mobile clients on the go; do not market Tecotype as a universal everywhere replacement. |
| Calendar and availability                      | Absent.                                                                                                                                                | Executive, sales, recruiting and consulting users frequently combine email with scheduling. Integrated availability is a major retention feature for those segments.                                    |
| Cross-device draft and settings continuity     | Drafts are deliberately local-only in the current architecture; no cross-install draft/settings synchronization was verified.                          | Broad Superhuman users expect continuity across computers and mobile/provider surfaces. This is not required for a deliberately single-desktop beta but limits permanent replacement claims.            |
| Read/open status and revenue integrations      | Absent.                                                                                                                                                | Sales, fundraising and recruiting cohorts will miss Recent Opens, CRM/ATS context, availability and follow-up tooling. Avoid targeting these cohorts initially.                                         |
| AI summaries, drafting and mailbox Q&A         | Absent; local intelligence beyond Better search is future work.                                                                                        | Not required to win users who dislike AI bloat, but increasingly expected by Superhuman Business evaluators. Add only after core actions are reliable, source-linked, optional and reversible.          |
| Delegation, collaboration and enterprise admin | Intentionally outside the current individual product.                                                                                                  | Tecotype cannot pursue EA/delegation, shared ownership, mid-market IT or enterprise procurement yet. This should remain a separate validated expansion rather than bloating Individual.                 |

## Claim corrections needed now

Two current product statements are ahead of the verified implementation:

1. `product.md` says **“Compose and reply workflows.”** Fresh compose/send exists;
   a true reply workflow does not.
2. `product.md` says **“Split-pane reading and composing workflows.”** Two-pane
   composition exists; a normal persistent list-plus-reader flow is not wired.

Keep the broader “implemented to varying levels of completeness” disclaimer, but
do not let these bullets become public shipped-feature claims until their
acceptance gates pass. Likewise, Windows/Linux are publication assumptions, not
the present release state.

The internal status record also needs one source of truth:

- the architecture index lists **attachments** as shipped, while only incoming
  display/download is complete;
- the same index lists **Split Inbox** after release, while its implementation
  note and current source say it is implemented; and
- several architecture notes describe older sending and quote-folding states.

Maintain a release capability ledger with `shipped`, `partial`, `planned`, and
`verified on` columns for every provider and platform. A feature becomes
`shipped` only when its user-visible acceptance test passes. This is not
documentation housekeeping: without it, product copy will repeatedly outrun the
client.

## The recommended first ICP

The smallest credible initial segment is:

- a desktop-dominant independent professional;
- two or more work, personal, or client accounts across Gmail and IMAP;
- high message volume and strong keyboard comfort;
- recurring cross-account organization or retrieval pain;
- willingness to pay for dependable professional software; and
- no hard dependence on Microsoft 365, mobile parity, CRM/ATS, delegation, or
  shared inboxes.

Good roles include independent consultants, developers, technical founders and
small-agency principals. “Founder” alone is too broad; the behavioral qualifiers
matter more than the title.

Recruit former Superhuman users who chose Spark for unified control but still
dislike its latency, search/sync reliability, or shortcut inconsistency. They
already value a premium keyboard workflow. Exclude price-only switchers, who
may reject €149/year. Users who returned to Superhuman after a trust failure
will require proof before switching again. See the
[non-Reddit switcher audit](./acquisition/spark/referrals.md#review-sentiment-including-former-superhuman-users).

The preview-pane wedge targets a subset of this ICP: people who repeatedly scan
or monitor a long list and need to retain list position while reading. It is not
a universal requirement for every keyboard-first user.

Do **not** initially target:

- mobile-heavy executives;
- Microsoft-only organizations;
- sales/recruiting users dependent on tracking, CRM/ATS and availability;
- EAs requiring real delegation and state synchronization;
- teams requiring shared ownership, admin, SSO or audit controls; or
- attachment-heavy users until the full attachment lifecycle passes.

This segmentation is not timidity. It prevents Tecotype from losing a broadly
marketed trial for reasons its chosen architecture and scope do not intend to
solve.

## Product strategy: parity floor plus three wedges

### The parity floor

Tecotype's parity floor is boring reliability at:

- reply/reply-all/forward and threading;
- incoming and outgoing attachments;
- rich compose, signatures and drafts;
- rendering and quote/thread fidelity;
- archive/delete/read/move at the right message or thread level;
- search that can be exact and inspectable;
- sync, offline queueing and recovery;
- identity safety, notifications and updates; and
- onboarding, billing, cancellation, export and deletion.

No positioning can compensate for failure here.

### Wedge 1: one real inbox across providers

Superhuman requires account switching and has no unified inbox. Tecotype should
make unified views genuinely safer and calmer:

- one Main view, with visible account identity;
- global search by default;
- per-account and per-client splits;
- sender/account safety on reply;
- fast temporary account isolation; and
- quiet controls for whether a split remains in Main.

This is the clearest immediate switch reason for consultants, agency principals
and people running several identities.

### Wedge 2: private, cross-account mailbox retrieval

Better search is the strongest current differentiator, but it should be sold as
part of a retrieval system, not as an isolated AI feature:

- exact local search across synchronized, indexed mail for things the user
  knows;
- meaning-based and cross-language search for things they only remember;
- every semantic result linked to its source message and match context;
- account/date/sender/attachment refinement;
- clear indexing state and storage/download cost; and
- ordinary search remains fast when the model is absent or disabled.

Do not claim “full history” until backfill is visibly complete, all promised
folders are covered, and every result can route to the matching source message.

The acquisition demonstration should use a real, reproducible retrieval job,
not generic “AI for email” language.

### Wedge 3, proposed: choice of focus mode or preview-pane mode

Superhuman's single-message focus is loved by many users and blocks adoption for
others. Tecotype can serve both without compromising its calm design:

- focused auto-next mode for inbox-zero processing;
- persistent list+reader mode for monitoring, scanning and comparison;
- right/below layouts and adjustable density;
- identical keyboard commands in both; and
- one instant toggle, preserving selection and scroll position.

This is a segment wedge, not a reason to turn Tecotype into a configurable
dashboard.

## Recommended build sequence

### Phase 0 — make email trustworthy

1. Implement and test reply, reply all, forward and threading end to end.
2. Implement outgoing attachments and complete incoming attachment
   preview/cache/offline behavior.
3. Fix HTML fidelity, remove silent clipping, add safe original viewing, and
   close remote-image privacy leakage.
4. Surface Undo Send, Send and Archive, delivery states, safe failure recovery,
   and exact local Send Later semantics.
5. Add signatures and close draft flush/recovery risks.
6. Add message-level/provider-state actions and quote/thread correctness.
7. Complete database encryption, notifications, first-run/provider preflight,
   signed design-partner distribution and real-provider release smoke tests.

**Exit condition:** internal dogfood passes a written daily-task matrix—read,
triage, exact search, compose, reply, reply all, forward, attach, draft, send,
schedule, recover and queue work offline—for two weeks without another client.
No external switch trial starts before this gate.

### Phase 1 — make the narrow switch compelling with design partners

1. Measure and tune the keyboard loop under realistic multi-account load.
2. Add identity safeguards, a familiar keymap option and guided migration.
3. Add deterministic search refinement and matching-message context.
4. Wrap Split Inbox in templates, preview and guided authoring.
5. Wire optional list+reader dual-pane behavior for the scanner/monitoring
   subset.
6. Add snippets, awaiting-reply and reply-aware follow-up.
7. Add out-of-office and the target ICP's validated fallback-prevention
   controls.
8. Turn offline behavior into an explicit tested contract.

**Exit condition:** target users prefer Tecotype for the unified/private-search
workflow, not merely because it costs less, and pass the agreed narrow-ICP
no-fallback task matrix.

### Phase 2 — make acquisition and conversion safe

1. Finish licensing, website checkout, cancellation, export and support.
2. Productize the reversible multi-account trial and provider preflight proven
   with design partners.
3. Instrument activation around completed real work—not time in app:
   first account, second account, first successful reply, first attachment send,
   first split, first successful search recovery, and first full fallback-free
   day.
4. Capture the exact reason whenever a trial user opens a fallback client.

**Exit condition:** the team can distinguish acquisition failure from missing
parity, reliability failure, provider mismatch and positioning failure.

### Phase 3 — expand the addressable market

1. Add Microsoft 365 with native-enough folder/category/state fidelity.
2. Ship and validate Windows and Linux from the same behavior contract.
3. Add calendar/availability and deeper invitation handling.
4. Consider respectful read status and targeted CRM/ATS integrations only for a
   validated revenue/recruiting segment.

Mobile remains out of scope, so this phase expands desktop reach without
claiming universal continuity.

### Phase 4 — add optional intelligence and team adjacencies

Add source-linked summaries, draft assistance, mailbox Q&A, MCP/automation or
collaboration only when actions are explicit, reversible and non-blocking.
Never let AI latency or availability sit in the core triage path.

## Release acceptance gates

Feature checkboxes are not sufficient. Before inviting Superhuman switchers,
run these as product-level gates.

### Reply and send

- Gmail-to-Gmail, Gmail-to-Outlook, IMAP-to-Gmail and IMAP-to-Outlook
  round trips preserve recipients, subject, `Message-ID`, `In-Reply-To`,
  `References`, chronology and expected provider thread membership.
- Reply all handles sender, self-addresses, aliases, duplicates, Bcc and list
  mail correctly.
- Forward can include or exclude original attachments deliberately.
- Send, undo, schedule, edit scheduled, cancel, retry and ambiguous-delivery
  recovery never duplicate mail.
- Every Send exposes Undo for the full execution window and restores the exact
  draft. Failed and unknown-delivery states remain visible and editable.
- A scheduled-send test covers app open, app closed, machine asleep, machine
  offline and machine off. The UI explains any state the local-only architecture
  cannot satisfy before scheduling, rather than after a missed send.

### Attachments

- Drag/drop, picker, paste, remove, retry, reply-with-original, forward and
  Save As work for common PDFs, images and Office files.
- Empty, Unicode, duplicate and long filenames behave predictably.
- Provider size-limit failures remain editable and explain the recovery.
- Restart and offline queueing do not lose local attachment references.
- Large files do not create unbounded memory use.

### Drafts, provider state and out-of-office

- Type and immediately close, navigate, sleep or kill the app at every point in
  the debounce window; no committed character is lost and recovery is obvious.
- Move/delete/read and target-ICP Gmail-label/IMAP-folder actions round-trip
  through provider sync without duplication, resurrection or state drift.
- Out-of-office imports current provider state, validates the audience and time
  zone, survives restart, and can be disabled from Tecotype without a stale
  provider responder.

### Rendering

- Maintain a versioned corpus of Outlook/Word templates, Gmail messages,
  newsletters, receipts, signatures, lists, tables, inline images, nested
  quotes, malformed common HTML and long messages.
- Compare against provider/native-client references.
- Never silently clip content; offer a safe original/raw fallback.
- No sender-controlled script, form or unapproved network request executes.
- Light/dark mode does not erase information or substantially alter hierarchy.

### Offline and recovery

- Disconnect for a full work session: read, exact/semantic search, triage,
  remind, draft, attach, queue and schedule.
- Kill and restart during each operation.
- Show which attachments/resources are local.
- Reconnect after provider-side concurrent changes and verify conflict behavior,
  ordering, mutation replay and no duplicate sends.

### Dual pane

- Keep the message list persistent while moving through messages entirely from
  the keyboard.
- Support right and below reader layouts, resizing and density.
- Preserve selection and scroll position.
- Make mark-read policy explicit and testable.
- Toggle instantly to focused single-message mode and retain auto-next.

### Search and splits

- Exact sender, address, subject, date, account, folder and attachment-filename
  queries have deterministic expected results.
- Every result opens the matching message with context.
- Semantic results show source context and never make exact search unavailable.
- A non-technical target user can create a VIP/client/newsletter split, preview
  matches, understand why messages matched, and undo it without learning TQL.

### Experience and performance

Use proposed internal budgets, then recalibrate from user perception on the
slowest supported hardware:

- core keyboard action to painted state: p95 at or below 100 ms;
- cached thread and compose open: p95 at or below 150 ms;
- first local full-text results: p95 at or below 250 ms;
- no input loss, focus jump or modal interruption in repeated auto-next triage;
- performance tested with several accounts, a large archive and long threads.

### Onboarding, notifications and distribution

- A fresh signed build connects each target provider, preflights permissions and
  credentials, shows backfill/reconnect state, and remains useful while history
  is still arriving.
- Per-account and priority notification controls are quiet by default; delivery
  and badge state survive sleep, restart and network interruption.
- Update, rollback, account removal and data-removal behavior pass on the exact
  design-partner build, not only in development.

### Trial success

A proposed validation cohort is 12–15 qualified users for four weeks. A switch
trial succeeds only when:

- the user completes every task in the agreed narrow-ICP matrix in Tecotype;
- at least 75% require no fallback client for a Tecotype defect or missing
  baseline during the final two weeks;
- there are zero lost drafts, wrong-account sends, duplicate sends or silently
  ambiguous deliveries;
- the user can name the differentiated reason to stay;
- cancellation and data removal remain self-service; and
- failures are categorized by workflow rather than hidden in a generic
  activation metric.

## What to defer

Do not delay the trustworthy daily loop for:

- a general AI assistant;
- autonomous classification or sending;
- team comments and shared inboxes;
- analytics dashboards;
- elaborate contact enrichment;
- an extension marketplace;
- broad project-management integrations; or
- enterprise administration before an enterprise segment is validated.

These may expand the market later. None makes an email client safe to switch to.

## The single most important decision

Tecotype must choose between two claims:

1. **Broad Superhuman replacement.** This implies Microsoft 365, mobile
   continuity, calendar, AI expectations, collaboration/admin and substantially
   wider parity. It conflicts with the current mobile scope and would scatter
   the roadmap.
2. **Best desktop mail client for multi-account, privacy-sensitive keyboard
   professionals.** This turns existing architecture into a coherent wedge and
   makes the missing work finite.

Choose the second. Win a narrow cohort through unified accounts, private local
retrieval and a more trustworthy ordinary mail loop. For the scanner/monitoring
subset, add optional preview-pane triage without weakening focused mode. Broaden
only after that cohort stops falling back.

## Evidence index

The most consequential implementation evidence:

- `../tecotype/src/views/threadView/threadActor.ts:832-852` — Quick Reply Send
  and Send later discard; expand opens compose.
- `../tecotype/src/views/threadView/helpers/quickReply.ts:69-80` — expanded
  quick reply carries only content.
- `../tecotype/src/views/composeView/composeActor.ts:621-635` — absent reply
  context produces a fresh empty compose.
- `../tecotype/native/src/outbox/render.rs:90-112` — generated message lacks
  reply headers and contains only text/HTML alternative parts.
- `../tecotype/native/src/outbox/submit.rs:68-85` — Gmail send deliberately
  passes no thread ID.
- `../tecotype/electron/outbox/types.ts:6-51` and
  `../tecotype/architecture/sending.md:693-697` — no outgoing attachment model;
  attachments are out of scope for the current sending slice.
- `../tecotype/src/views/composeView/composeActor.ts:286-315,965-1015` and
  `../tecotype/src/core/frameManager.ts:653-675` — delayed submission exists,
  but successful scheduling closes compose and global Undo handles message
  mutations rather than sent drafts.
- `../tecotype/src/views/threadsView/helpers/inboxRows.ts:152-164` and
  `../tecotype/src/views/threadsView/components/DraftRow.tsx:43-61` — draft-list
  rows omit persisted send-error state.
- `../tecotype/src/core/frameManager.ts:314-333,427-453` — compose opens
  secondary; ordinary thread open uses the focused pane.
- `../tecotype/src/views/appView/AppView.tsx:20-59` and
  `../tecotype/src/views/appView/components/Pane.tsx:9-28` — two-pane shell with
  fixed equal flexible columns.
- `../tecotype/src/views/threadView/components/MessageBody.tsx:51-74,94-113` —
  HTML clipping and injected presentation.
- `../tecotype/src/views/threadView/components/messageBodySecurity.ts:23-33` —
  direct HTTPS images allowed.
- `../tecotype/architecture/html-email-rendering.md:3-28,136-183` — current
  renderer versus selected unimplemented direction and known fidelity loss.
- `../tecotype/architecture/database-encryption.md:3-32` — encryption is
  proposed and cache coverage is incomplete.
- `../tecotype/architecture/search.md:10-23,216-223` — query/limit-only public
  contract and current search non-goals.
- `../tecotype/architecture/split-inbox.md:3-19` and
  `../tecotype/architecture/tql-approachability.md:42-71` — implemented Split
  engine and remaining product-level authoring barriers.
- `../tecotype/architecture/README.md:3-51` — current pre-release and
  post-release work, including notifications, encryption, onboarding,
  distribution and Outlook.
- `../tecotype/README.md:51-76` and `../tecotype/package.json:41` — current
  Apple Silicon/macOS release target.
- `product.md:117-161,237-255` and `positioning.md:286-324` — current marketing
  capability language and explicit claim limits.
