# Tecotype gaps to become a strong Spark contender

**Date:** 2026-07-20

**Customer basis:** [`spark-mail-customer-research.md`](./spark-mail-customer-research.md)

**Tecotype source snapshot:** `f382ffa2df98`, with an empty working tree at
capture. Later product-repository changes are outside this analysis.

**GTM document snapshot:** `product.md` and `positioning.md` at
`598f92518d77`.

**Verification boundary:** pinned source, tests, architecture notes, product
documents, and a live installer-route probe. No new end-to-end mailbox trial was
run.

## Verdict

Tecotype is not ready to replace Spark as a primary client, and broad Spark
parity is not the right near-term strategy.

Two gaps dominate:

1. **Ordinary email is not yet safe.** Quick-reply Send and Send Later discard
   content; expanded replies lose context; MIME lacks reply headers; Gmail
   submission omits the thread ID; forwarding was not found; outgoing
   attachments are absent.
2. **Spark preserves an accumulated operating system.** Customers depend on
   accounts, identities, categories, shortcuts, obligations, signatures,
   settings, and synchronized restoration across devices. Tecotype has no
   equivalent migration, mobile continuity, or cross-install state.

The second gap is partly architectural. Spark stores authorization material and
uses server processing for specified sync, push, collaboration, and AI
features. Tecotype infrastructure does not receive mailbox credentials or
contents. Copying Spark's token-custody model would remove Tecotype's clearest
privacy distinction.

That distinction is a segment hypothesis, not proven universal demand. Privacy
concerns are less recurrent than reliability, search, and migration complaints,
and public evidence does not show that Spark employees routinely read or sell
mail.

The recommended **post-gate destination** is:

> A private, desktop-first client for individual professionals controlling
> several Gmail and/or IMAP identities: one controllable flow, unmistakable
> per-account identity, inspectable triage, and exact plus meaning-based local
> retrieval, without adding Tecotype as a mailbox processor.

This is not current acquisition copy. Reply, attachments, identity safeguards,
inspectable triage, and the trustworthy search contract remain incomplete.

The public release manifest reported `0.6.0`, and the Apple-Silicon installer
route resolved; macOS x64, Windows x64, and Linux x64 probes returned 404. The
audited config targets macOS 12+, but the live artifact exposes neither its
minimum OS nor source commit. The route proves installer availability, not that
`0.6.0` contains the audited snapshot.

## Current foundations

These are implementation assets from source/tests, not release-artifact
acceptance.

| Foundation                         | Verified implementation value                                                                          |
| ---------------------------------- | ------------------------------------------------------------------------------------------------------ |
| Unified and separate account views | All-account and account-specific thread/draft queries and switching exist                              |
| Gmail plus generic IMAP/SMTP       | Core adapters exist; provider-specific conformance remains unproven                                    |
| Local exact and semantic search    | Full-text remains available without the optional on-device multilingual model                          |
| Split Inbox                        | Cross-account rules, counters, editing, and `hide_from_main` exist                                     |
| Keyboard and obligation core       | Navigation, triage, mutation Undo, timed reminders, and Send Later exist                               |
| Local boundary                     | Credentials and mailbox working state remain local; Tecotype has no infrastructure mailbox-access path |

The sending foundation is narrower than a complete workflow. The outbox worker
runs only with the app process; unknown/sent rows are hidden from ordinary draft
retrieval; accepted provider IDs and SMTP Sent-APPEND failures are log-only.
Timed-reminder cancellation reacts to fresh messages but does not classify reply
direction.

## Priority and state

- **G0 — primary-client gate:** do not invite Spark switchers until it passes.
- **G1 — narrow-contender gate:** required to win and retain the recommended
  desktop Gmail/IMAP cohort.
- **G2 — market-expansion gate:** required for another Spark cohort or broad
  replacement claims.

State vocabulary:

- **Implemented:** source/test path exists; release acceptance is not implied.
- **Release-verified:** the acceptance test passed on a named release artifact.
- **Partial:** useful implementation exists, but the outcome is incomplete.
- **Verified broken:** current control flow prevents the outcome.
- **Not found:** absent from the audited source.
- **Planned:** documented future work.
- **Out of scope:** intentionally excluded.

Customer confidence belongs in the research report. Gap priority below reflects
consequence and dependency, not recurrence or engineering effort.

## Gap map

### G0 — primary-client safety

| Gap                                        | State                                                                                                                                                         | Exit requirement                                                                                                                                             |
| ------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Reply, reply all, forward, and threading   | **Verified broken.** Parent/thread storage exists but the UI-to-MIME/provider path is unwired                                                                 | Correct recipients, identity, quote control, reply headers, Gmail/IMAP threading, forwarding, Send and Archive, Send Later, and Undo                         |
| Outgoing attachments                       | **Not found.** Incoming cards, Save As, and inline retrieval exist                                                                                            | Attach/remove/retry/progress; durable draft/outbox references; inline images; reply/forward originals; provider limits and restart/offline behavior          |
| Compose, signatures, aliases, identity     | **Partial.** Rich text, recipients, and sender identities exist; signatures and complete safeguards do not                                                    | Per-account/alias signatures, reliable formatting, explicit identity binding, and low-noise wrong-account protection                                         |
| Drafts, Send Later, delivery recovery      | **Partial.** Local drafts, delayed send, scheduling, Edit/Discard, and outbox exist; visible Undo and trustworthy failure surfacing do not                    | No lost committed text; visible queued/sending/retrying/failed/unknown states; duplicate protection; explicit app/device-off semantics                       |
| Provider sync and authentication           | **Partial.** Gmail polling, IMAP INBOX IDLE, reconnect/auth state, and queues exist                                                                           | Release conformance for the target provider matrix; visible auth, backfill, freshness, retry, and completeness                                               |
| Known-message search                       | **Partial.** Query/limit returns recency-ordered threads with a generic snippet, but no scope, coverage, matching-message anchor, query snippet, or highlight | Deterministic known-answer search, visible account/folder/history scope, index completeness, matching-message context, and honest zero results               |
| Message and provider state                 | **Partial.** Thread archive/read/trash/spam/remind and Undo exist; per-message actions, full labels/folders, and move/copy fidelity do not                    | Explicit thread/message behavior, provider-safe folder/label state, reversible same-account movement, and honest cross-account limits                        |
| Rendering and original access              | **Partial.** HTML clips at 300,000 characters; known Outlook/responsive fidelity losses remain                                                                | No silent clipping, versioned provider corpus, safe original/raw fallback, stable chronology, and bounded long-thread performance                            |
| Remote resources and visible-frame privacy | **Partial.** Direct HTTPS images are permitted; the selected controlled-resource design is unimplemented                                                      | Explicit remote-image policy, no hidden requests, scriptless frame, and precise data-path explanation                                                        |
| Local mailbox protection and deletion      | **Partial.** Credentials are protected; database/WAL/TEMP/cache encryption is planned                                                                         | OS-owned key, encrypted database/WAL/cache, memory-only TEMP, no plaintext fallback, clear key-loss/deletion behavior                                        |
| Onboarding and switch readiness            | **Partial.** A public Apple-Silicon route and source-level account flows exist                                                                                | Signed target artifact, minimum-OS validation, provider preflight, first-run flow, notifications, update/rollback/removal, smoke tests, and incident support |

Remote-resource blocking and local database encryption are G0 because they are
dependencies of Tecotype's proposed privacy claim, not because Spark research
shows them as frequent switch triggers.

### G1 — narrow-contender requirements

| Gap                                           | State                                                                                                                              | Exit requirement                                                                                                                                              |
| --------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Multi-account scale and identity clarity      | **Partial.** Unified views exist; colors/order, scale budgets, and anomalous-identity protection are incomplete                    | Several large Gmail/IMAP accounts, visible identity everywhere, account health, fast isolation, and safe sender/signature behavior                            |
| Inspectable categories and batch triage       | **Partial.** Split Inbox is powerful but query-oriented; priority/enable, recipes, grouping, selection, and batches are missing    | Guided categories, preview/why-matched, enable/order, sender grouping, safe batch actions, and an unmistakable Everything escape                              |
| Obligation grammar                            | **Partial.** Archive, reminders, Send Later, and Undo exist                                                                        | Predictable active, done, date/no-date deferred, important, scheduled, follow-up-if-no-reply, and undoable outcomes                                           |
| Differentiated retrieval                      | **Partial.** Exact and semantic engines exist; route, source-linked match context, richer filters, and attachment matching do not  | Rich filters, optional multilingual meaning search, source-linked semantic results, and predictable offline/model-disabled behavior                           |
| Migration and reversible trial                | **Not found.** No Spark/Classic importer or guided recreation                                                                      | Reconnect accounts; recreate colors, identities, signatures, keymap, categories, sender decisions, and deferred-state mappings; disclose non-migratable state |
| Setup recovery without Tecotype token custody | **Not found.** Each install owns local account/app state                                                                           | User-owned encrypted profile or direct transfer for metadata, followed by explicit provider reauthorization                                                   |
| Speed, keymaps, and reading layout            | **Partial.** Keyboard shell exists; Spark/Classic preset, remapping, persistent list-reader, resizing, and detachable views do not | Measured large-mailbox speed, conflict-safe remapping, stable list-reader selection/layout, and focused mode                                                  |
| Sender controls, rules, workspaces            | **Partial.** Spam and Split rules exist; allow/block/unsubscribe, decision history, and richer scopes do not                       | Reversible sender/domain decisions, explicit account/workspace scope, provider-vs-local distinction, and safe partial failure                                 |
| Offline, export, and recovery                 | **Partial.** Local bodies/search/drafts/queues/reminders exist; attachments and backup/export are incomplete                       | Published local-availability contract, offline/restart/reconnect tests, readable export, deletion, and conflict behavior                                      |
| Commercial and support contract               | **Partial.** Intended pricing exists; purchase/cancel/export/support journey is incomplete                                         | Reversible trial, one clear individual plan, self-service renewal/cancel/removal, incident chronology, and human escalation                                   |
| Validated fallback controls                   | **Partial.** Full invitation actions, out-of-office, and personal templates are absent/incomplete                                  | Add only task-matrix-proven controls; validate templates for consultants/agencies; keep speculative utilities out                                             |

### G2 — broader Spark cohorts

| Gap                                            | State                                                                                                              | Strategic boundary                                                                                      |
| ---------------------------------------------- | ------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------- |
| Microsoft 365/Outlook/Exchange                 | **Not found.** No Graph provider                                                                                   | Highest provider expansion after Gmail/IMAP trust; tenant approval still applies                        |
| Polished iCloud/Yahoo/custom IMAP setup        | **Partial.** Protocol paths exist                                                                                  | Do not name provider support before dedicated setup and conformance                                     |
| Desktop platforms                              | **Partial.** Apple-Silicon route exists; live minimum OS/source is unverified; other probed routes are unavailable | Ship/validate macOS Intel or explicitly exclude it; add Windows and Linux through one provider contract |
| Mobile continuity                              | **Out of scope.**                                                                                                  | Permanent ceiling on broad “replace Spark everywhere” claims                                            |
| Cross-install drafts/settings/obligations      | **Not found.**                                                                                                     | Any sync design needs an explicit privacy decision                                                      |
| Calendar and integrations                      | **Not found.** Ordinary mail/attachment rendering exists, but calendar and integration outcomes do not             | Add invitation safety first; broaden only for a validated segment                                       |
| Contextual AI beyond retrieval                 | **Partial.** Local semantic retrieval exists                                                                       | Not required for the recommended cohort; later AI must be optional and source-linked                    |
| Delegation/shared inboxes/team templates/admin | **Out of scope.**                                                                                                  | Separate customer, product, infrastructure, privacy, and pricing decision                               |
| Free habit loop/bundle distribution            | **Not found.**                                                                                                     | Distribution economics, not a primary-client feature gate                                               |

## Source-status discrepancies at the pinned snapshot

1. `product.md` said **“Compose and reply workflows.”** Fresh compose/send
   exists; real reply does not.
2. `architecture/README.md` calls **attachments** shipped, but only incoming
   handling is implemented.
3. The architecture index places **Split Inbox** after release although source,
   tests, and its architecture note show implementation.
4. `architecture/imap.md` says SMTP is pending although current code and a
   recorded Gmail/Fastmail check show implementation.
5. `architecture/sending.md` has stale checklist/out-of-scope items; scheduled
   Edit exists.
6. “Private by design” must not imply encrypted local mail, blocked tracking,
   “mail never leaves the device,” or no provider communication.
7. “Available on macOS, Windows and Linux” is intended scope. Current evidence
   proves only a public Apple-Silicon Mac installer route.
8. “Works fully offline” remains inaccurate; state exact local operations and
   Send Later limits.

Maintain one release ledger:

```text
capability
provider
platform
state: release-verified | implemented | partial | verified broken | planned | not found | out of scope
verification: code | automated test | runtime/manual | documentation
verified on
release version and source provenance
```

Public capability copy should use `release-verified`, not infer availability
from source.

## First customer

Target:

- an individual professional controlling their accounts and installation;
- Apple-Silicon Mac for the initial release;
- two or more Gmail and/or supported IMAP accounts;
- recurring pain from account switching, exact retrieval, opaque
  categorization, workflow-generation change, reliability, or performance;
- willingness to pay for dependable professional software; and
- acceptance of provider/native mobile clients and manual reauthorization on a
  second computer.

Promising relationship states:

- privacy/AI-averse multi-account users;
- hybrid verifiers who return to Gmail or another provider for exact search;
- Classic loyalists, after native-feeling speed and familiar controls are
  proven; and
- multi-business operators, after identity and scale safety.

Do not initially target mobile-first users, Microsoft-only/managed tenants,
assistants/shared teams, AI-dependent customers, calendar-heavy workflows,
price-only churners, or attachment-heavy professionals before G0.

Do not require willingness to write rules during recruitment. Include automatic
category users and test whether guided, inspectable recipes are acceptable.

## Strategy

### Parity floor

The floor is boring trust: complete mail, correct reply/send identity,
attachments, drafts, provider state, deterministic exact search, observable
sync/failure state, safe rendering, clear local/remote privacy, and dependable
onboarding/support. Calm, privacy, semantic search, or price cannot compensate
for failure here.

### Segment hypothesis: no Tecotype token custody

Keep credentials and mailbox contents out of Tecotype infrastructure. Complete
local encryption and remote-resource controls before leading with the claim.
Offset reconnection friction with user-owned metadata transfer and explicit
provider reauthorization.

This boundary will repel convenience-first users. Validate conversion and
willingness to pay rather than infer demand from privacy concern.

### Retrieval wedge

Unify two jobs:

1. find the known message exactly; and
2. recover context from imperfect memory.

Make scope/backfill visible, open the matching message, preserve exact search
without the model, and link every semantic result to source context.

### Proposed triage wedge

Turn Split Inbox into guided, inspectable categories with preview, why-matched,
sender grouping, safe batches, enable/order controls, and an inescapable
Everything view. Keep TQL as advanced mode. Validate that customers prefer this
contract enough to configure it.

## Build order

### Phase 0 — trustworthy ordinary email

- reply/reply-all/forward/threading;
- outgoing attachments and reliable compose/identity;
- drafts, visible delivery state, Undo, and app-off scheduling semantics;
- provider state, exact search, rendering, remote resources, and local
  encryption; and
- notifications, onboarding, release smoke tests, update/recovery, and support.

Exit only when all G0 gates pass on the named artifact for personal Gmail,
Google Workspace, Fastmail, iCloud app-password, and one custom IMAP/SMTP
service, followed by two weeks of fallback-free internal use.

### Phase 1 — preserve the Spark loop

- multi-account scale and identity;
- guided Splits, sender controls, batches, and obligations;
- differentiated exact/semantic retrieval;
- Spark/Classic keymaps and optional list-reader layout;
- migration, reversible trial, user-owned setup portability; and
- validated offline/export/fallback controls.

Exit only when all G1 gates pass and qualified design partners complete their
task matrix without a desktop fallback client.

### Phase 2 — safe acquisition

Finish checkout, licensing, cancellation, export, deletion, and support. Measure
completed work and record every return to Spark/provider mail by cause:
parity, trust, provider, device, migration, reliability, or positioning.

### Phase 3 — desktop expansion

Add Microsoft Graph, validated Windows/Linux and macOS architecture coverage,
provider-polished setup, invitations/calendar, and only proven workflow
integrations. Research privacy-preserving cross-install state.

### Phase 4 — optional intelligence or separate team product

Source-linked summaries, mailbox Q&A, drafting, translation, automation, and
MCP may follow the ordinary loop. Delegation, comments, assignments, shared
drafts/inboxes, and admin require a separate decision.

## Release gates

| Gate                                        | Minimum acceptance                                                                                                                                                         |
| ------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Provider/sync [G0]                          | Target accounts connect fresh; history, forward sync, folders, sent/drafts/trash/spam/unread/threading match provider clients; auth/backfill/freshness/failure are visible |
| Message state [G0]                          | Thread and message actions do not expand unexpectedly; labels/folders remain provider-correct; same-account movement and unsupported cross-account boundaries are explicit |
| Reply/send [G0]                             | Gmail↔IMAP round trips preserve identity, recipients, reply headers, chronology, threading; Send/Undo/schedule/edit/cancel/retry never duplicates                          |
| Compose/attachments [G0]                    | Picker, drag/drop, paste, reply/forward originals, inline images, size failures, restart/offline queueing, signatures, formatting, and draft flush pass                    |
| Rendering/privacy [G0]                      | Versioned provider corpus has no silent clipping; safe original exists; no unapproved network request; database/WAL/cache/TEMP boundary passes                             |
| Exact search [G0]                           | Known-answer sender/address/subject/body/date/account/folder/literal tests open the matching message with visible scope and completeness                                   |
| Onboarding/operations [G0]                  | Signed artifact installs on declared hardware/OS, preflights providers, updates/rolls back, removes data, and produces actionable incident chronology                      |
| Triage/obligations/senders [G1]             | Non-technical user creates and explains categories; Everything survives classifier failure; batches recover partially; deferred/follow-up state returns correctly          |
| Retrieval/migration/offline/experience [G1] | Semantic results cite sources; setup state is recreated or disclosed; replacement-computer and offline/reconnect tests pass; keymap/layout remain stable                   |
| Commercial/trial [Phase 2]                  | Billing/cancel/export are self-service; no lost draft, wrong-account send, duplicate, ambiguous delivery, or hidden mail; differentiated stay reason is explicit           |

## Defer

Defer mobile, server-held token restoration, a general contextual AI assistant,
autonomous sending/classification, team collaboration, enterprise admin, broad
integrations, analytics, marketplaces, and a permanent Free tier.

Do not defer ordinary email trust or the **outcome** of setup recovery. Build a
user-controlled alternative instead of copying Spark's custody model.

## Decision

Choose between:

1. **Broad Spark replacement:** mobile continuity, one-login restoration,
   Microsoft/mixed-provider breadth, categories/batches, obligation sync,
   calendar, integrations, contextual AI, teams, admin, and broad support.
2. **Build toward the best private desktop client for multi-account Gmail/IMAP
   professionals:** complete ordinary mail, one controllable flow, trustworthy
   retrieval, inspectable triage, explicit reauthorization, and provider mobile
   clients.

Choose the second.

Broaden only after the narrow cohort stops using Spark or a provider client as
its confidence layer.

## Evidence index

Customer requirements:

- `spark-mail-customer-research.md` sections **Research verdict**, **Customer
  segments**, **What customers value**, **What customers reject**, **Mailbox
  access**, **Microsoft incident**, and **Switching requirements**.

Pinned implementation evidence at `f382ffa2df98`:

- Reply: `src/views/threadView/threadActor.ts:756-852`,
  `src/views/threadView/helpers/quickReply.ts:69-80`,
  `src/views/composeView/composeActor.ts:621-635`,
  `electron/outbox/types.ts:6-40`,
  `native/src/outbox/repository.rs:1179-1322`,
  `native/src/outbox/render.rs:79-115`, and
  `native/src/outbox/submit.rs:68-85`.
- Sending/recovery: `electron/outbox/types.ts:6-57`,
  `src/views/composeView/composeActor.ts:799-1153`,
  `electron/ipc/registerOutboxHandlers.ts:12-53`,
  `native/src/sync/mod.rs:762-830`,
  `native/src/outbox/repository.rs:304-399`, and
  `native/src/outbox/worker.rs:179-250`.
- Unified views/actions/layout:
  `src/views/threadsView/threadsActor.ts:274-320,449-463,607-682`,
  `native/src/mail/api.rs:52-68`,
  `native/src/mutations/types.rs:3-61`,
  `src/core/frameManager.ts:199-228,314-333,427-453,653-693`, and
  `src/views/appView/components/Pane.tsx:9-28`.
- Splits/search/reminders: `architecture/split-inbox.md:3-28`,
  `architecture/tql-approachability.md:42-71`,
  `architecture/search.md:6-23,216-223`,
  `electron/mail/types.ts:1-17`,
  `architecture/reminders.md:3-33`,
  `native/src/mail/ingest.rs:112-134`, and
  `native/src/mutations/repository.rs:544-597`.
- Providers: `architecture/imap.md:275-309`,
  `architecture/gmail.md:283-287`,
  `architecture/syncing-state.md:1-113`,
  `architecture/sending.md:11-13,76-82`, and
  `native/src/outbox/submit.rs:68-145`.
- Rendering/privacy/platform:
  `src/views/threadView/components/MessageBody.tsx:51-74`,
  `src/views/threadView/components/messageBodySecurity.ts:23-33`,
  `architecture/html-email-rendering.md:3-90`,
  `architecture/database-encryption.md:1-36`,
  `README.md:51-76`, `electron-builder.yml:26-38`, and
  `architecture/windows-distribution.md:1-30`.

GTM product evidence at `598f92518d77`:

- `product.md:117-161,237-256`
- `positioning.md:273-324`

Live route probe at 2026-07-20 20:26 CEST:

- `https://releases.tecotype.com/manifest.yaml` reported `0.6.0`.
- macOS arm64 resolved; macOS x64, Windows x64, and Linux x64 returned 404.
- The manifest exposed no source-commit provenance.
