# Sealed public pain discovery — archives, mail files, migration, and recovery

Access date for every source: **2026-07-19**.

## Scope and method

This was a sealed pass. I did not read workspace files, feature requests, experiments, partnership/provider-program documents, or other agents' work. I used only the product boundary in the assignment: a future calm, keyboard-first macOS/Windows/Linux desktop mail client; no mobile; mailbox credentials and mailbox contents remain local; browser-local and local-file processing are acceptable.

I tested materially different exact-problem queries around:

1. Thunderbird profile migration and apparently lost local mail.
2. Apple Mail `mbox` import failures and permissions.
3. Opening, previewing, or reading `.msg`/`.eml` without Outlook, an account, or a full client.
4. Bulk `.eml` export failures, long filenames, and fidelity.
5. Outlook-to-Linux `.msg`/`.eml` conversion.
6. Browsing/searching old `.pst` archives without importing or subscribing.
7. File-association and OS app-store discovery.
8. Paid desktop-client adjacency around large archives and old local mail.

More than 30 plausible pages were opened. The retained observations below span six source types: official support communities, independent forums/communities, app/extension reviews, a public issue tracker, Q&A, and independent first-person accounts. Vendor documentation is used only for incumbent/surface verification or counterevidence, never as pain evidence.

## Executive read

The strongest repeated job is not generic “email backup.” It is **regaining confident, local inspectability after email has become a file or database**.

Four pain families recur:

1. **Open or preview a useful mail artifact now.** A person receives or finds `.msg`, `.eml`, or `.pst`, but the installed software refuses it, requires an account/subscription, loses preview context, or opens excessive UI.
2. **Create a portable archive without silent damage.** Bulk export/conversion freezes, stops on filenames, loses hidden items/attachments/headers/folder structure, or gives counts that cannot be reconciled.
3. **Recover locally present mail after identity/server/profile disruption.** The bytes still exist, but the client no longer surfaces them. Recovery becomes profile archaeology and direct filesystem manipulation.
4. **Move a long-lived archive across machines, operating systems, or clients.** Large imports take days, appear frozen, render incorrectly, or require a specific incumbent to be installed.

Important qualifications:

- Several recovery cases have a complete free outcome through manual file copying or a free extension. This is evidence for pain and complexity, not proof that a paid product is required.
- Current Outlook, Apple Mail, and Thunderbird all cover parts of the job. The gap is uneven format/OS support, scale, verification, and low-trust conversion—not mere absence of an Import button.
- Exact-problem search repeatedly surfaces these pages, but search alone is only discovery.
- The strongest zero-user mechanism found is an unsupported-file action that leads into an OS app-store file-type search. macOS documents this as shipped. Windows has a shipped “Browse apps in Microsoft Store” path, but one firsthand account says it loses the originating file context; direct in-dialog Store recommendations were still an Insider preview in the source inspected.
- A received `.msg` attachment is a useful-artifact acquisition trigger, but the evidence does not show that the sender recommends a specific app. It is therefore product-native exposure, not evidenced product-native recommendation.
- Same-person paid adjacency exists, but is limited: a paid eM Client user explicitly needs to retain a large history; another archive importer says they would pay for Pro if it preserved attachments. One current `.pst` actor explicitly rejects paying for Outlook just to read old mail, which is direct counterevidence against assuming willingness to pay for a broad client.

## Retained direct observations

### Family A — open, preview, and inspect local mail artifacts

**A1 — A sent `.msg` becomes a receiver-side opening problem**

- Provenance: [direct URL](https://superuser.com/questions/1341282/need-to-send-msg-file-so-that-it-is-previewable); independent end-user questioner, not a seller; published 2018-07-18; SuperUser / Q&A.
- Observation schema: actor/context = Outlook Web App sender and recipient; trigger = sender attaches a `.msg`; desired job = let recipient preview the saved message; failure = receipt appears as a link and the recipient has trouble opening it; consequence = useful information cannot be consumed and desktop Outlook is explicitly unavailable; behavior/workaround = sender tests by sending it to themself and asks how to change the attachment/preview behavior; current relevance = the proprietary artifact handoff remains current, but the exact 2018 OWA behavior needs retesting; duplication = distinct from local double-click and archive browsing because it starts with interpersonal artifact receipt; supported claim = saved email itself can create a zero-user receiver problem; contradicted claim = the sender did not recommend any viewer, so this is not evidenced referral.

**A2 — External users need a permanent accountless `.msg` reader**

- Provenance: [direct URL](https://superuser.com/questions/1690247/configure-outlook-2016-as-a-msg-reader-only-without-any-profile-or-email-addres); independent administrator/end-user questioner; published 2021-11-29; SuperUser / Q&A.
- Observation schema: actor/context = external users remoting into a machine containing `.msg` files; trigger = double-click a stored message; desired job = view it with no local email identity; failure = Outlook requires setup/account context and cannot act as a reader-only app; consequence = every user hits setup friction and the proposed permanent workflow is impossible; behavior/workaround = administrator investigates `/PIM`, rejects one-off launch tricks, and is told to create an account then disable send/receive; current relevance = Outlook 2016-specific, but the accountless local-inspection boundary remains current and is corroborated by 2026 file-reader demand; duplication = distinct actor (managed external users) and constraint (no environment email address); supported claim = “reader without mailbox setup” is a real job; contradicted claim = Outlook alone is not a complete free accountless outcome here.

**A3 — A valid standalone `.msg` fails in Outlook while online viewers open it**

- Provenance: [direct URL](https://superuser.com/questions/1722270/why-would-some-outlook-installations-not-open-correctly-formed-msg-file); independent personal Outlook user; published 2022-05-21; SuperUser / Q&A.
- Observation schema: actor/context = person using local Outlook and a local-only Wi-Fi sync workflow; trigger = sync a calendar item, drag it to `Test.msg`, and double-click; desired job = inspect the standalone item; failure = two laptops/two Outlook versions say they cannot read it although another organization and two online viewers can; consequence = repeated repair attempts and uncertainty about file fidelity versus local policy; behavior/workaround = repeatedly runs PST repair, repairs Outlook, exports the item, sends it to the sync vendor, and uploads it to online viewers; current relevance = exact versions are older, while “trusted local viewer versus upload confidential mail to a website” remains current; duplication = distinct because the file is apparently valid and local configuration is the suspected blocker; supported claim = users will leak a local file to online viewers to resolve uncertainty; contradicted claim = a parsing success in a web viewer does not prove a trustworthy complete solution.

**A4 — File Explorer preview is absent for `.msg` on Windows ARM**

- Provenance: [direct URL](https://www.reddit.com/r/ARMWindows/comments/1ris76u/windows_11_arm64_file_explorer_preview_not/); independent Windows ARM user; published 2026-03-02; Reddit / independent community.
- Observation schema: actor/context = Windows 11 24H2 ARM64 user with no Outlook install; trigger = select a `.msg` in Explorer; desired job = preview content, attachments, and metadata in place; failure = generic icon/blank pane and no native ARM64 handler; consequence = a common file-inspection workflow is unavailable; behavior/workaround = toggles preview settings, edits registry, restarts Explorer, re-registers handlers, tests ExplorerPatcher, and asks for a third-party handler; current relevance = very current and platform-specific; duplication = distinct from double-click because the desired surface is Explorer preview; supported claim = file-handler/preview integration can be the first-action surface; contradicted claim = one unanswered post does not establish market size.

**A5 — A single archived `.eml` opens the full client plus a message window**

- Provenance: [direct URL](https://www.reddit.com/r/Thunderbird/comments/1fg8ee6/cant_open_eml_file_in_a_window_without_also/); independent Thunderbird user and independent commenters; published 2024-09 (page shows “2y” at access); Reddit / independent community.
- Observation schema: actor/context = user reading old `.eml` files from an archive system; trigger = double-click one file; desired job = read one message and close it; failure = Thunderbird opens both its main app and the message window; consequence = repeated extra windows/clicks and one user says they will stop using Thunderbird; behavior/workaround = closes the main window, downgrades to 115.6.1 or 102, and disables JavaScript; current relevance = behavior is version-sensitive and must be retested, but the “single-artifact calm viewer” job is explicit; duplication = distinct from parse failure because the message opens, but the workflow is disproportionate; supported claim = interaction weight matters even when functional support exists; contradicted claim = not evidence that archive reading alone causes purchase.

**A6 — A Mac user has 40 GB of `.pst` needed for an audit but rejects an Outlook subscription**

- Provenance: [direct URL](https://www.reddit.com/r/MicrosoftOutlook/comments/1s35ehw/stuck_in_pst/); independent former-office-PC user; published 2026-03-25; Reddit / independent community.
- Observation schema: actor/context = person who moved years of work archives from Windows to Mac; trigger = audit requires old client contracts; desired job = search/read old mail while preserving folder tree; failure = cannot open `.pst` without full Outlook subscription, online converters have tiny limits or destroy structure; consequence = 40 GB feels trapped and contracts are hard to locate; behavior/workaround = tries online converters, considers Enolsoft, asks for reliable reviews and a lightweight viewer; current relevance = very current; duplication = distinct because it is cross-platform, large-scale, and time-bound by an audit; supported claim = read/search-only archive access is a concrete job with review-seeking behavior; contradicted claim = explicit refusal to pay for Outlook just for this job weakens broad-client paid conversion.

**A7 — A paid narrow viewer wins through double-click integration and team spread**

- Provenance: [direct URL](https://apps.apple.com/us/app/msg-viewer-for-outlook-pro/id1274576533?mt=12); independent App Store reviewer, no disclosed vendor connection; review published 2020-04-09; Apple App Store / app review.
- Observation schema: actor/context = Mac Outlook user handling hundreds of `.msg`/`.eml` files; trigger = double-click a message; desired job = open it in the normal message view with components preserved; failure before product = macOS/clients did not natively handle the artifact as desired (inferred from product use, not separately described); consequence = repeated file friction across a team; behavior/workaround = buys the $19.99 Pro viewer, uses it for about a year, and deploys it on six team Macs; <=25-word quote = “Worth the investment”; current relevance = the listing is still live but the app version history shown stops in 2019; duplication = distinct because it is successful paid behavior and team diffusion, not a complaint; supported claim = file association plus a narrow local utility can convert and spread; contradicted claim = payment is for a viewer/converter, not proof of willingness to buy a broader mail client.

### Family B — export, convert, migrate, and verify fidelity

**B1 — Decades of Outlook mail block a Windows-to-Linux move**

- Provenance: [direct URL](https://www.reddit.com/r/Thunderbird/comments/1svbvyh/scripts_to_convert_outlook_msg_to_thunderbird_eml/); independent technical user who built and shared scripts after failing with incumbents; published 2026-04-25; Reddit / independent firsthand account.
- Observation schema: actor/context = person moving decades of email from Outlook/Windows to Linux; trigger = making Linux the daily-driver laptop; desired job = clean, faithful RFC 5322 `.eml` suitable for an open-source client; failure = Outlook cannot directly export `.eml`, drag-out freezes/corrupts, COM loses fidelity, free tools freeze or miss items/classes, and closed tools are not trusted with confidential email; consequence = migration cannot be validated and Linux adoption is blocked; behavior/workaround = tests old Thunderbird versions and multiple tools, compares counts/headers/body/format, distrusts online/closed converters, then builds PowerShell and Python converters; current relevance = very current; duplication = strongest fidelity/privacy/OS-switch observation; supported claim = local conversion can be distribution-critical to a broader desktop client; contradicted claim = a complete free script may satisfy this technical actor without a paid client.

**B2 — One long subject stops an entire bulk `.eml` export**

- Provenance: [direct URL](https://www.reddit.com/r/Thunderbird/comments/1teak5e/how_to_skip_overlong_file_names_when_saving/); independent Thunderbird user; published 2026-05-15; Reddit / independent community.
- Observation schema: actor/context = user exporting many messages via Ctrl+A → Save As; trigger = one message has an excessively long subject; desired job = complete a high-volume `.eml` export; failure = the whole operation stops; consequence = user must manually locate each offending message and calls high-volume export impractical; behavior/workaround = asks for a way to skip or sanitize overlong names; current relevance = very current; duplication = distinct deterministic filesystem-name failure, not generic scale/fidelity; supported claim = robust filename mapping is a complete-outcome requirement; contradicted claim = no evidence of paid intent or broader-client switching.

**B3 — A current extension release exports zero of 34 messages in several formats**

- Provenance: [direct URL](https://services.addons.thunderbird.net/en-GB/thunderbird/addon/importexporttools-ng/reviews/); independent add-on reviewer, developer replies separately; published 2026-06-02; Thunderbird Add-ons / extension review.
- Observation schema: actor/context = Betterbird 140.9 on Windows 11, IMAP, ImportExportTools NG 15.0.0; trigger = export a 34-message test folder; desired job = create EML/HTML/PDF artifacts; failure = 34/34 errors, empty destination or `undefined` files, while MBOX works; consequence = no portable per-message output; behavior/workaround = documents versions, formats, counts, logs, and offers test data; developer says to resave options or use a beta; current relevance = extremely current but tied to a specific release/config migration; duplication = distinct from B2 because multiple individual-message formats fail while MBOX succeeds; supported claim = export correctness can regress silently across upgrades; contradicted claim = the developer provides a simple configuration fix, so this may not be durable.

**B4 — An export/import round trip loses messages**

- Provenance: [direct URL](https://github.com/thunderbird/import-export-tools-ng/issues/497); independent add-on user filing an issue; published 2023-11-13; GitHub / public issue tracker.
- Observation schema: actor/context = first-time ImportExportTools NG user converting Thunderbird structure to MBOX for later PST use; trigger = export structured folders, then re-import to validate; desired job = preserve mail and hierarchy before migration to Outlook; failure = comparison shows missing messages in both folders and subfolders; consequence = exported artifact cannot be trusted as a complete migration source; behavior/workaround = constructs a round-trip test, compares original versus import, shares structure/screenshots, and narrows to smaller folders with the maintainer; current relevance = old version and maintainer expected a patch, so exact bug may be fixed; duplication = distinct because the user independently verifies completeness rather than noticing a crash; supported claim = count/structure verification is part of the job; contradicted claim = not evidence of a current unresolved defect.

**B5 — Outlook archive creates a monolithic PST when the user wants inspectable individual files**

- Provenance: [direct URL](https://superuser.com/questions/844613/how-to-automatically-move-outlook-emails-to-a-file-folder-outside-of-outlook); independent Outlook user; published 2014-11-25; SuperUser / Q&A.
- Observation schema: actor/context = Outlook 2013 user; trigger = trying to archive mail outside Outlook; desired job = save messages automatically into ordinary local/server folders and inspect messages individually; failure = built-in archiving creates only PST; consequence = archived messages are not directly browseable as files; behavior/workaround = asks for a rule, receives a vendor recommendation that is challenged, then is pointed to a free VBA approach; current relevance = UI/version is old, but PST-versus-individual-artifact choice remains current; duplication = distinct desired representation, not recovery; supported claim = filesystem-native archives are a real local-workflow job; contradicted claim = commenters assert a complete zero-cost solution exists.

**B6 — Five large PST imports retain mail but lose every attachment; actor volunteers willingness to pay**

- Provenance: [direct URL](https://forum.emclient.com/t/import-large-pst-succeeds-but-all-attachments-are-gone/61617); independent eM Client forum user; published 2019-07-16; eM Client community / official product support forum.
- Observation schema: actor/context = person importing five 10 GB PSTs plus a 2 GB PST; trigger = archive migration into a broader desktop client; desired job = preserve complete messages including attachments; failure = all mail appears but attachments are gone; consequence = the apparent successful import is unusable/incomplete; behavior/workaround = asks whether this is a free-tier limitation and offers to buy Pro if Pro solves it; current relevance = old version and no proof of current defect; duplication = distinct due 52 GB scale, silent attachment loss, and explicit payment statement; supported claim = same-person willingness to pay a broader mail client exists when archival fidelity is the blocker; contradicted claim = support says Pro does not change import behavior, so monetization cannot be a fidelity paywall.

**B7 — PST messages import but display raw HTML; user rejects a hosted workaround and downgrades**

- Provenance: [direct URL](https://forum.emclient.com/t/imported-pst-messages-not-displaying-correctly/82051); independent eM Client user; published 2022-05-29; eM Client community / official product support forum.
- Observation schema: actor/context = person setting up eM Client on a new PC without Outlook; trigger = import PST copied from another computer; desired job = read thousands of archived messages normally; failure = message bodies display raw HTML; consequence = per-message repair is infeasible and the new client becomes a “non-contender”; behavior/workaround = rejects routing private mail through a temporary GMX IMAP account as too much hassle, installs an older client version, re-imports successfully, then upgrades; current relevance = version-specific but directly exposes hosted-workaround rejection and downgrade behavior; duplication = distinct from missing items/attachments because data is present but not inspectable; supported claim = local direct import is a boundary requirement; contradicted claim = a free older version resolved the job.

**B8 — A 17 GB/100k-message PST migration looks hung for more than a week but completes**

- Provenance: [direct URL](https://forum.emclient.com/t/taking-1-week-to-sync-to-gmail/108751); independent long-term eM Client user migrating a family member; published 2025-05-09; eM Client community / official product support forum.
- Observation schema: actor/context = user moving a 17 GB, 100k-message, 220-folder Outlook history to a new Windows PC; trigger = PST import followed by Gmail sync; desired job = complete migration with known progress; failure = continuous sync appears stuck for over a week; consequence = user reinstalls/restarts because they assume failure; behavior/workaround = watches operations, waits, completes in 8–10 days, then describes mirrored NAS, monthly offline USB, and ransomware recovery behavior; current relevance = recent; duplication = distinct because the process ultimately works and exposes progress/assurance rather than correctness; supported claim = progress, checkpointing, and post-import backup are part of the job; contradicted claim = slow does not necessarily mean failed.

### Family C — recovery from local bytes after profile, host, or server disruption

**C1 — Host change hides messages the user knows are still local**

- Provenance: [direct URL](https://support.mozilla.org/en-US/questions/1520830); independent Thunderbird support questioner; published 2025-07-04; Mozilla Support / official support community.
- Observation schema: actor/context = Linux user whose hosting service failed and became unavailable; trigger = change mail host/settings; desired job = retrieve locally stored messages; failure = messages disappear from the client although the user locates them under `~/.thunderbird`; consequence = apparent loss during provider change; behavior/workaround = asks support and follows guidance to search unused profiles and copy non-`.msf` files into active Local Folders; current relevance = recent; duplication = distinct host/identity change with known local bytes; supported claim = provider exit is a recovery/acquisition moment for a local client; contradicted claim = manual file copy yields a complete free recovery.

**C2 — System Restore breaks the profile; replacing with an older backup loses important recent POP mail**

- Provenance: [direct URL](https://support.mozilla.org/en-US/questions/1380147); independent Thunderbird support questioner; published 2022-06-16; Mozilla Support / official support community.
- Observation schema: actor/context = Windows POP user after System Restore; trigger = Thunderbird claims it is already running when no process exists; desired job = recover recent mail from the saved broken profile; failure = whole-profile replacement preserves the defect, older-profile replacement loses weeks of mail, and copying `Mail` alone does not surface folders; consequence = “rather important” mail appears lost; behavior/workaround = saves both profiles, reinstalls, copies extensionless MBOX files to desktop/USB, installs ImportExportTools NG, and reports success; current relevance = old OS/client version but durable profile-recovery mechanics; duplication = distinct corrupt-profile/partial-restore case; supported claim = selective recovery with preview/verification has value; contradicted claim = a free extension solved it.

**C3 — Mail-server disk crash leaves a partial local cache that the client cannot move at scale**

- Provenance: [direct URL](https://support.mozilla.org/en-US/questions/1535661); independent administrator/user; published 2025-09-14; Mozilla Support / official support community.
- Observation schema: actor/context = Ubuntu Thunderbird user administering an IMAP server that suffered disk failure; trigger = server-side folder disappears while some message bodies remain local; desired job = recover 2,000+ cached messages to local folders or a new server; failure = drag/drop moves one or two then stops, offline mode reveals some bodies were never downloaded; consequence = manual transfer could take weeks and some messages may be unrecoverable; behavior/workaround = backs up the MBOX, considers learning `mb2md`, then solves the downloaded subset by copying the MBOX into Local Folders; current relevance = recent; duplication = distinct partial-cache/server-disaster case; supported claim = a client should distinguish complete bodies from headers and quantify recoverability; contradicted claim = no tool can recover bodies that were never local.

**C4 — A careful 10-year profile move still opens as a new installation**

- Provenance: [direct URL](https://support.mozilla.org/en-US/questions/1482278); independent Thunderbird user; published 2024-12-30; Mozilla Support / official support community.
- Observation schema: actor/context = Windows user moving a 10-year installation from Windows 10/custom path to Windows 11; trigger = new computer; desired job = preserve full account/profile state; failure = after following guides and copying data, Thunderbird behaves as new except for the address book; consequence = repeated experiments and uncertainty about which profile/path is authoritative; behavior/workaround = deletes/creates profiles, tries custom locations, and copies Roaming/Local folders; current relevance = recent; duplication = distinct whole-machine migration with custom path; supported claim = profile discovery and mapping are a migration job; contradicted claim = thread is marked solved, so the observation does not prove a permanent incumbent failure.

**C5 — Paid desktop client user must keep old mail but suspects it causes severe lag**

- Provenance: [direct URL](https://forum.emclient.com/t/emclient-very-slow/109534); independent paid eM Client user; published 2025-06-12; eM Client community / official product support forum.
- Observation schema: actor/context = paid eM Client 9.2 user with a large old-mail history; trigger = normal keyboard/mouse mail actions; desired job = retain history and keep the client responsive; failure = delete confirmation takes 5–10 seconds and a possible corrupt/large database is suspected; consequence = daily calm interaction degrades, while starting over would sacrifice needed mail; behavior/workaround = asks for help, rejects “start new” as not solving retention, and considers database repair/partial restore; current relevance = recent; duplication = distinct paid adjacency and archive-induced daily-performance cost; supported claim = same person pays for a broader client and values retained history; contradicted claim = causation by archive size is not established.

### Family D — old Apple Mail MBOX import as stale-but-mechanistic evidence

**D1 — MBOX import silently creates empty folders until permissions are changed**

- Provenance: [direct URL](https://discussions.apple.com/thread/2178762); independent Apple users; published 2009-09-27 with confirmations through 2009-10-07; Apple Support Community / official support community.
- Observation schema: actor/context = Mac user moving Apple Mail mailboxes between accounts, one FileVault-protected; trigger = import saved MBOX packages; desired job = recover mailbox contents; failure = “no valid mbox,” partial-import notices, no Import mailbox, or empty folders, with no useful permission error; consequence = repeated failed imports and uncertainty about file validity; behavior/workaround = removes passwords, tries shares/Home folder/permission changes, copies through Boot Camp or an external drive, and succeeds after permission normalization; current relevance = exact Mail 4.1/macOS 10.6 bug is stale, while current Apple Mail still officially imports MBOX; duplication = distinct permissions/diagnostics mechanism; supported claim = local-file permission state can masquerade as corrupt mail; contradicted claim = do not present this exact defect as current.

## Near-misses, counterevidence, and non-retained pages

1. **Current Outlook can open/search PST.** Microsoft’s current support page says new Outlook can open, read, and search PST, and classic Outlook can open it without importing: [Microsoft Support](https://support.microsoft.com/en-US/Outlook/open-and-find-items-in-an-outlook-data-file-pst). Counterweight: new Outlook currently requires classic Outlook installed, a Microsoft 365 subscription, matching architecture, and does not support PST on ARM. This makes Windows outcomes much better than the Mac audit actor’s case, but not accountless/cross-platform.
2. **Current Apple Mail has native MBOX import/export.** [Apple Support](https://support.apple.com/guide/mail/import-or-export-mailboxes-mlhlp1030/mac) documents import from Apple Mail or Windows/UNIX MBOX and export to `.mbox`. The 2009 failure is mechanistic history, not a current-gap claim.
3. **Current Thunderbird has built-in import.** [Mozilla Support](https://support.mozilla.org/en-US/kb/thunderbird-import) documents profiles, apps, and file import. Counterweights: ZIP import is limited above 2 GB, and Outlook import requires Outlook installed; a PST file alone is insufficient.
4. **The free ImportExportTools NG incumbent is broad.** Its [current repository](https://github.com/thunderbird/import-export-tools-ng) lists MBOX/EML/EMLX import, EML/HTML/PDF/CSV/text export, hierarchy, indexes, complete-profile export/import, and scheduled backups. This can be a complete free outcome for many jobs. Its changelog also shows recurring fixes for filename handling, missing messages, EML import/export, and backup failures—evidence that edge-case completeness is hard.
5. **Positive extension evidence exists.** A June 2026 reviewer specifically values preserved message timestamps on exported files; another calls saving EML attachments to a folder a strong feature. These are useful counterexamples to “all export tools fail.”
6. **An old PST question was solved by simply opening the PST in Outlook.** [SuperUser](https://superuser.com/questions/56210/read-not-import-outlook-pst-file) says the archive can be opened, read, and closed without import; only fast indexing is limited. It is counterevidence to universal archive lock-in, but depends on already having Outlook and is from 2009.
7. **PST viewer recommendations are noisy.** In a [Reddit recommendation thread](https://www.reddit.com/r/Outlook/comments/1cxbmir/recommendations_for_outlook_pst_file_readers/), one independent commenter recommends a free Kernel viewer after use; another reports browser performance on 30k messages but errors in some folders. Many other comments read like vendor promotion. Retained only as surface/incumbent evidence, not pain count.
8. **A new 2026 App Store viewer claims fully local multi-format handling.** [MSG Viewer — Email Opener](https://apps.apple.com/us/app/msg-viewer-email-opener/id6758084152) supports `.msg`, `.eml`, `.mbox`, `.mht`, local processing, search, attachments, and conversion. Its review cluster is unusually repetitive (same reviewer names, similar language, few total ratings), so it is incumbent evidence but weak independent recommendation evidence.
9. **A 2026 Outlook `.msg` refusal may be a transient machine bug.** [Reddit](https://www.reddit.com/r/OfficeHelp/comments/1tphzy7/outlook_old_and_new_suddenly_refusing_to_open_msg/) reports many `.msg` files working on other computers and after changing extension to `.eml`; this supports file-opening pain but was not separately counted because it duplicates A3 and may be temporary.
10. **Generic feature requests, vote counts, vendor copy, snippets, and second-hand statements were excluded.** The existence of buttons such as “Share” was not treated as product-native distribution.

## Current discovery, recommendation, sharing, and incumbent surfaces

### 1. Exact-problem search

Observed: exact queries consistently surfaced Mozilla/Apple support, SuperUser, Reddit, GitHub issues, and add-on reviews. This can introduce an unknown product through a task page or comparison.

Classification: **discovery only**. It is not recommendation unless an independent actor names and endorses the product. It is not counted as distribution by itself.

### 2. macOS unsupported-file → App Store

Apple documents that if no app is set for a document, macOS offers **Search App Store**, where “a list of apps that can open this type of document appears”: [Apple Support](https://support.apple.com/en-ie/guide/mac-help/mchlp1040/mac). Apple also documents setting an app permanently for a file type through Finder’s Open With / Change All.

Mechanism: user double-clicks an unsupported `.msg`/`.pst`/`.mbox` → OS names the need and offers compatible apps → store listing can provide install and purchase → app registers as a permanent handler.

Assessment: **credible zero-user source and attributable first-action funnel candidate**. It is permanent OS discovery, not merely search-engine traffic. Exact blockers: confirm Tecotype’s eligible file-type declarations; verify live filtered results and ranking for each extension; confirm whether a full mail client is accepted/relevant for the narrow query; instrument first launch from file-open without reading/uploading the file; verify store-to-paid attribution. No evidence of a partnership or guaranteed placement.

### 3. Windows Open With → Microsoft Store

A 2024 firsthand Microsoft Tech Community post says **Browse apps in Microsoft Store** opens Store results for the originating extension and the desired app appears, but opening/installing it does not set the default or preserve the originating file context: [direct source](https://techcommunity.microsoft.com/discussions/windows11/open-with-app-from-the-windows-app-store/4282363). A second user reported the same in January 2026.

Microsoft’s current developer documentation says Store publishing provides search/collection discovery, trusted install, revenue processing, analytics, and supports MSIX plus existing signed MSI/EXE installers: [Microsoft Learn](https://learn.microsoft.com/en-us/windows/apps/package-and-deploy/choose-distribution-path).

A December 2025 report described direct Store recommendations inside Open With, but explicitly said they were rolling out gradually to Insider Beta/Dev and did not establish general release: [Windows Central](https://www.windowscentral.com/microsoft/windows-11/windows-11-will-soon-show-microsoft-store-app-download-recommendations-in-the-open-with-menu).

Assessment: **credible but operationally leaky zero-user surface**. Do not claim the direct-recommendation UI as shipped without a current stable-build test. Exact blockers: confirm current stable Windows behavior; verify extension-specific listing results; ensure install registers the handler and reopens the original file; measure Store attribution; support ARM64.

### 4. Independent recommendation

Evidence:

- The App Store reviewer in A7 independently says the paid viewer was worth the investment and reports six team Macs using it.
- A Reddit PST-reader commenter reports using a recommended free viewer successfully and recommends it onward, while another documents partial read errors.
- Mozilla support contributors repeatedly recommend ImportExportTools NG and direct local file copying; questioners report successful recovery.

Assessment: **evidenced actor/surface**, but it recommends narrow viewers/extensions or recovery procedures—not a broader Tecotype-like client. The recommendation would need to remain honest: “open/recover this locally” first, with broader-client value earned later.

### 5. Useful artifact receipt / product-native sharing

Evidence: A1 shows a `.msg` sent through email becoming a receiver-side opening problem. The artifact is inherently useful and carries its own trigger. A7’s incumbent copy describes files generated on PC and opened on Mac; the reviewer confirms repeat team use.

Assessment: **evidenced exposure, not evidenced recommendation**. No source shows a sender choosing “Share with Tecotype,” inviting the recipient, or endorsing a viewer. A generic Share button does not count. A possible complete free outcome (convert/send as `.eml` or PDF) also limits paid conversion.

### 6. Existing-client extension/add-on surface

Thunderbird’s Add-ons Manager and Mozilla support recommendations can surface ImportExportTools NG. This is strong problem-solution recommendation, but it begins with an existing Thunderbird user and therefore is **not a zero-existing-user source for a broader client**.

## Incumbent map

| Incumbent | Complete free outcome observed | Strength | Boundary/gap exposed |
|---|---|---|---|
| Outlook classic/new | Open/search PST on supported Windows configurations | Native fidelity for PST/MSG and archive search | Subscription/classic-install/architecture/ARM constraints; not cross-platform/accountless in several observed contexts |
| Apple Mail | Native MBOX import/export | Installed on macOS; interoperable format | No native PST; historical permission ambiguity; not Windows/Linux |
| Thunderbird built-in import | Profiles, apps, files; free cross-platform client | Broad and free | ZIP >2 GB limitation; PST import requires Outlook; profile/path complexity |
| ImportExportTools NG | Broad MBOX/EML import/export, indexes, profile backup | Free, recommended in support, actively maintained | Version/config regressions; filename/fidelity/completeness edge cases; requires Thunderbird |
| Narrow PST/MSG viewers | Often free viewing, paid export/batch; app-store/file association fit | Fast path to read-only job | Trust, reliability, stale updates, platform silos; limited broader-client adjacency |
| User-built/open-source converters | Can be complete and local for technical actors | Private, auditable, free | Setup/debug burden; brittle at high scale and corrupt/hidden items |
| Hosted/online converters | Immediate no-install experiment | Easy discovery | Size limits, structure damage, confidentiality/trust conflict |
| eM Client / Mailbird-class paid clients | Import/archive plus broader daily mail | Paid-client adjacency exists | Large-history performance, slow/opaque migration, version regressions, hosted workarounds rejected |

## Opportunity registry by underlying job

Evidence counts below refer only to retained observations, not vendor pages or near-misses.

| Underlying job | Evidence count and diversity | Possible complete free outcome | Zero-user source | Evidenced recommender/sharing actor and surface | Same-person paid adjacency to broader client | Exact blockers | Next materially different query |
|---|---|---|---|---|---|---|---|
| Open/preview a single `.msg` or `.eml` locally without mailbox setup | 7 observations; Q&A, Reddit, App Store review; end user, admin, receiver, ARM user, team | Thunderbird, browser-local/open-source viewers, or conversion to `.eml`/PDF may complete it; fidelity and calm UI vary | macOS Search App Store is shipped; Windows Store-by-extension exists but loses context; file double-click is the first action | Paid App Store reviewer recommends a viewer and spreads it to six Macs; `.msg` sender/receiver is evidenced exposure but not recommendation | Weak: A7 uses Outlook and pays for a narrow viewer, but broader-client payment is not shown | Register formats/Quick Look/preview handlers; ARM64; sandbox/local-only proof; safe HTML; malformed files; preserve reply/forward semantics without forcing account setup; live Store ranking/attribution | Search first-person legal, audit, construction, and public-record workflows where `.msg` is an exchanged deliverable, not just an archive |
| Browse/search a large `.pst` archive without import, subscription, or cloud upload | 2 retained observations plus two counterevidence threads; Reddit and Q&A; audit actor and legacy archive owner | On supported Windows with existing Outlook, yes; free PST readers may work; no trustworthy complete free Mac outcome was directly established | Unsupported-file → App Store; exact-problem search; potentially Store extension lookup | Independent Reddit commenter recommends a viewer after use, but vendor-like comments pollute the surface | Negative/weak: current Mac audit actor refuses Outlook subscription; no same-person broad-client payment | PST parsing/search/attachments/folder tree at 40+ GB; corruption; read-only guarantee; Mac/Linux; review trust; Outlook licensing; export upsell without trapping data | Search “audit subpoena old PST Mac/Linux,” “estate executor PST,” and “former employee archive PST” first-person accounts |
| Export portable per-message files with verifiable fidelity and safe filenames | 5 observations; Reddit, extension review, GitHub issue, Q&A; Linux switcher, bulk exporter, validation-minded user | Thunderbird/ImportExportTools/scripts can be complete free outcomes for many archives | Exact-problem search; add-on manager is not zero-user; the output artifact can later trigger file-open discovery | Support contributors recommend the free extension; Linux actor publishes scripts; not a product-native recommendation for a broader client | None direct for broader client; technical actor builds free scripts | Hidden/corrupt/class items; filename/path rules; counts; headers/CID/attachments/timestamps; structured folders; resumability; audit log and source-to-output reconciliation | Search first-person “email export evidence chain,” “FOIA email export EML,” “eDiscovery PST to EML fidelity,” and accountant/project-folder workflows |
| Recover locally present mail after host/server/profile failure | 4 observations; Mozilla official support community; Linux admin, POP user, host-switcher, Windows migrator | Yes in several cases: direct MBOX/profile copy or free extension solved it | Exact-problem support search; provider failure itself is a trigger, but no provider recommendation surfaced | Mozilla contributors recommend concrete free recovery paths; questioners confirm success | No paid adjacency in retained recovery actors | Detect active/inactive profiles; distinguish headers from bodies; non-destructive preview; quantify recoverable messages; permissions; explain provenance; avoid credentials/upload; preserve current profile | Search first-person “provider shut down local mail cache recovery,” “domain expired IMAP local copy,” and MSP/client handoff cases outside Thunderbird |
| Migrate a long-lived archive across client/OS while preserving structure and content | 7 observations across Reddit, GitHub, Mozilla, eM Client forum; Windows→Linux, Windows→Windows, Outlook→eM, Thunderbird→Outlook | Sometimes: built-in import, free client, free extension, scripts, or version rollback; large/faulty archives remain uncertain | Exact-problem search and OS file/store surface; no evidenced provider/OEM introduction | Support communities recommend free tools and old versions; no sender-like sharing loop | Yes: B6 explicitly offers to pay Pro for preserved attachments; C5 is already a paid broader-client user who must retain old mail | PST/MSG licensing; format parity; 10–50+ GB scale; progress; resumability; attachment/category/calendar/contact coverage; folder mapping; post-import validation; multi-day sync | Search paid-client reviews that explicitly say migration/import caused purchase or churn, segmented by archive size and OS switch |
| Keep a large local history usable and recoverable in daily work | 3 observations; eM Client forum and Reddit; paid user, family migrator, audit user | Manual profile copies, NAS/USB rotation, and built-in backup can be free/complete if restoration works | Not a strong zero-user source by itself; failure/recovery search is reactive | Forum helpers recommend database repair, partial restore, and offline copies; no independent product recommendation to a new client | Strongest retained adjacency: C5 already pays for a broad desktop client; B8 uses it on three PCs and maintains extensive backups, but payment status is unstated | Fast search/keyboard interaction at 100k+ messages; incremental backup; restore drills; corrupt database isolation; dedupe; ransomware-safe offline copies; transparent local storage | Search “paid email client large local archive slow,” “offline email backup restore test,” and “ransomware email archive recovery” firsthand reports |
| Send a saved email artifact another person can open | 1 direct sender/receiver observation plus successful team-viewer evidence | Sender can use `.eml`, PDF, forwarding, or screenshots; completeness/metadata varies | The received artifact itself is zero-user exposure; its unsupported-file action can enter an OS store | Sender is evidenced; recommendation is not. App Store team spread is evidenced separately but not tied to sender action | None | Standard output; attachments/headers; safe rendering; recipient OS; no mailbox setup; sender intent; attribution without tracking contents | Search first-person “client sent MSG cannot open,” “lawyer/accountant sent MSG,” and cross-company artifact handoff; look specifically for senders recommending a viewer |

## Prioritized interpretation

### 1. Best-supported job: “Open and verify this mail file locally”

Why it survives counterevidence:

- Multiple actors begin outside a mail client: receiver, auditor, external remote user, Explorer user, archive reader.
- The first action is observable and narrow: double-click/select/open a file.
- macOS and Windows already expose file-type-to-store mechanisms.
- Privacy is structurally aligned: A3 and B1 show people either upload private mail reluctantly or distrust closed converters.
- A narrow free outcome can be complete and still serve as a truthful first experience. The unsolved business question is whether the same person later values a broader client.

Do not infer:

- That a standalone viewer should be paid.
- That every `.msg` user needs a new mail client.
- That artifact receipt itself is a referral.

### 2. Highest-stakes job: “Make a portable archive I can prove is complete”

Why it matters:

- The failures are often silent: missing messages, attachments, headers, folder placement, or timestamps.
- Sophisticated users perform round trips and compare counts because “export completed” is not enough.
- Local-only processing is a material differentiator where mail is confidential.

Hard product boundary:

- A credible outcome requires deterministic manifests, per-item status, resumability, source/output counts, exception explanations, and a way to inspect failures. A plain Export button is not the job.

### 3. Most emotionally acute but least monetizable alone: “Recover the mail I can see on disk”

Why:

- Consequences include apparently lost important mail, provider failure, and server disaster.
- Free manual recovery repeatedly succeeds.
- The better opening is trust and rescue, not a claim that a paid client is necessary.

Potential bridge:

- A non-destructive local recovery/inspection mode can show competence, then offer normal daily mail only after the archive is safe. This is a hypothesis, not an evidenced funnel.

## Exact blockers before any distribution claim

1. Verify that Tecotype can safely register `.eml`, `.msg`, `.mbox`, and possibly `.pst` without misrepresenting current shipped support.
2. Test stable macOS and Windows file-handler/store results with clean machines; do not rely on search snippets or Insider previews.
3. Establish local-only parsing and rendering for malformed/untrusted HTML, embedded objects, attachments, and TNEF/OLE content.
4. Define a complete free outcome for each format. “Preview first N messages” would conflict with the calm/honest boundary unless plainly justified.
5. Instrument acquisition without collecting mail filenames, senders, subjects, contents, or mailbox credentials.
6. Prove large-archive scale and verification: 10–50+ GB, 100k+ messages, long paths, corrupt records, mixed item classes, and interrupted/resumed operations.
7. Separate archive viewer economics from broader-client economics. The strongest current counterevidence is the Mac PST actor who wants lightweight read-only access and explicitly rejects a full Outlook subscription.
8. Obtain same-person evidence that a successful local rescue/viewer causes adoption and payment for everyday mail. Current evidence demonstrates pain, narrow-tool payment, and paid-client archive burden, but not that causal bridge.

## Next discovery pass

The next pass should avoid more generic Thunderbird migration questions. Use materially different actors and consequences:

1. Legal/audit/eDiscovery practitioners exchanging `.msg` or reviewing PST on non-Windows machines.
2. Accountants, property/construction teams, and public-sector staff who file email alongside project documents.
3. MSPs and domain/hosting customers after provider shutdown or domain loss.
4. Paid-client reviewers whose purchase/churn explicitly followed an import, recovery, or large-history job.
5. File-handler discovery tests on clean stable macOS/Windows installations, recording the exact app-store result set for `.msg`, `.eml`, `.mbox`, and `.pst`.
6. Independent recommendations in trusted professional communities, specifically asking whether the recommended solution is a narrow viewer, a converter, or a full desktop mail client.

The key unanswered question is no longer whether archive/file pain exists. It is whether a **complete, private, free local outcome** can create enough trust and adjacent daily-mail value to produce a broader-client paid funnel without turning a rescue moment into a trap.
