# Sealed discovery ledger: migration, retrieval, and recovery

Status: Independent second-funnel pass  
Research date: 2026-07-19  
Market/language for keyword checks: United States, English  
Scope: verified mailbox migration audit, silent missing mail or attachments after
migration, Gmail known-message or attachment retrieval, recovery of local bytes
after provider or profile failure, and EML only where it naturally bridges into a
live paid client.  
Excluded before research: the selected Classic Outlook known-message search
funnel and the previously examined MBOX, MSG, and provider-one-mailbox routes.

This ledger does not modify or rely on acquisition conclusions. It records
research evidence, counterevidence, and product truth; it is not a commitment.

## Outcome

**Rigorous null: none of the tested routes currently qualifies as a second
acquisition funnel.**

The strongest near-miss is:

> A Gmail user knows a message exists, but Gmail search omits or badly ranks it,
> so the user needs a private local search that finds the known message and then
> remains useful as the person's everyday mail client.

This route is the only one with all of the following:

- at least five current, direct first-person incidents with the same outward
  job—retrieve a known Gmail message that Gmail search does not return;
- current exact-problem search demand;
- an organic bridge into a live mail client rather than a separate migration or
  recovery utility;
- direct evidence that paid-client users care about search.

It still fails the decision gate:

- the incidents are homogeneous at the user-job level, but not at the exact
  failure-mechanism level: ranking, Trash scope, exact-token behavior, attachment
  content, mobile caching, and sync visibility are mixed;
- the most common successful recommendations are Gmail's free `Most recent`
  toggle, `in:anywhere`, date ranges, exact operators, or desktop web;
- Thunderbird and MailStore Home provide substantial search capability for free;
- no retained incident shows the same person paying for a broader client because
  it solved this exact Gmail miss;
- several incidents are terminal retrieval jobs: find one document, ticket, or
  identifier, then leave;
- Tecotype's current local index does not yet cover several of the retained
  failures.

Therefore, keep Gmail known-message retrieval only as a **bounded activation
experiment after product gaps are closed**. Do not describe it as a validated
funnel, a shipped advantage, or distribution.

## Decision table

| Gate | Gmail known-message retrieval | Migration audit | Local-byte recovery | EML-to-live-client |
|---|---|---|---|---|
| Five homogeneous direct incidents | **Pass only at job/symptom level**; root causes differ | Partial; incidents span source, tool, label, size, and restore causes | Fail; client, storage, and failure modes differ | Fail |
| Current discovery or prevalence | **Partial:** modest exact demand and current support activity | Broad tools have demand; verification/missing-mail intent was not measurable | Weak | Weak |
| Observed recommendations | **Pass, but mostly free/native** | Provider reruns, reports, support, and specialist migration tools | Profile copy, backup restore, or data recovery | Thunderbird, GYB, and IMAP copy |
| Same person naturally uses a live mail client | **Pass structurally** | Often an admin acts for other users | Sometimes, but usually after a disaster | Sometimes |
| Observed same-person paid transition | **Fail** | Fail; buyer/operator and mailbox user usually differ | Fail | Fail |
| Adequate free incumbent | Gmail itself, Thunderbird, MailStore Home | Google/Microsoft tools, imapsync, provider support | Thunderbird/manual restore where bytes exist | Thunderbird and GYB |
| Terminal-job risk | Medium to high | **High** | **Very high** | **High** |
| Fit with current shipped behavior | Partial; local search exists, required coverage does not | Fail | Fail | Fail |
| Zero-user distribution | Fail | Fail | Fail | Fail |
| Verdict | Bounded experiment only | Reject as Individual funnel | Reject | Reject/defer |

## Strongest near-miss: Gmail known-message retrieval

### Direct incident set

The countable unit is a first-person report that a Gmail message is known to
exist—often because the author manually locates or opens it—but a plausible
search does not return it. Relative dates are preserved where the page did not
expose a reliable absolute date.

| ID | Date | Source type | Direct incident | Observed workaround or recommendation | Outcome |
|---|---|---|---|---|---|
| G1 | 2025-09-03 | Google Gmail Community, vendor-hosted peer support | The author knows the messages exist, searches senders and keywords across browsers and devices, and sees only a few results despite thousands of items in Trash. | Change the result ordering from `Most relevant` to `Most recent`. | The author confirms that the missing results appeared after the change. |
| G2 | 2025-09-08 | Reddit user post | The author manually finds a known message in Trash after searches for the email address and keywords omit it; the same searches still miss it while the message is visibly present. | `Most recent`; commenters also suggest `in:trash` and Gmail operators. | The author confirms seven expected results appear under `Most recent`. |
| G3 | 2026-02-26 | Reddit user post and same-page first-person comments | The original author says known mail can take 26 searches or remain undiscoverable. A separate author copies an exact address, subject, and person from an open message, still gets no result, then manually sees the message in Trash. | `in:anywhere`; one person tries Gemini; Thunderbird/local storage is discussed. | One commenter says `in:anywhere` worked. Gemini worked once and then failed for another author. |
| G4 | Page displayed `2mo ago` when accessed 2026-07-19 | Reddit user post | A ferry e-ticket and colleague messages can be found by browsing the known day, but searches for the sender and name omit them. | Try desktop web and `in:anywhere`. | The author says Safari on a laptop behaves the same; no confirmed resolution. |
| G5 | Page displayed `1mo ago` when accessed 2026-07-19 | Reddit user post | The author searches the numeric RMA substring `8812340`; the known message contains `X1ZT8812340` and can be found manually but not by that search. | A commenter explains Gmail's lack of wildcard substring search and recommends Google Scripts or Thunderbird only for search. | No confirmed resolution. |
| G6 | 2026-05-31 | Reddit user post | The author previously found an attached passport using a name or passport number, then AI-enabled Gmail search stopped returning it; disabling Smart Features and exact-number searches did not restore the result. | Quoted exact terms and web search rather than mobile are suggested. | The author says quotes and mobile still fail; web was not yet tested. |
| G7 | Page displayed `19d ago` when accessed 2026-07-19 | Reddit user post | Hundreds of messages are absent from normal Gmail views and sender search, yet a precise date-range search reveals them. | Exact date range and a wider sync range. | A commenter reports finding a known message after changing the sync range. |

Sources:

- G1:
  https://support.google.com/mail/thread/370444425/gmail-search-not-working?hl=en
- G2:
  https://www.reddit.com/r/GMail/comments/1nbnvmo/why_is_it_that_gmails_search_feature_is_so_useless/
- G3:
  https://www.reddit.com/r/GMail/comments/1rfexok/why_cant_i_ever_find_my_past_emails/
- G4:
  https://www.reddit.com/r/GMail/comments/1t3aios/failure_to_find_emails_using_search_function/
- G5:
  https://www.reddit.com/r/GMail/comments/1titp4v/gmail_text_search_function_not_bringing_up_emails/
- G6:
  https://www.reddit.com/r/GMail/comments/1tsx2eq/the_gmail_search_is_literally_pathetic_it_is_worse/
- G7:
  https://www.reddit.com/r/GMail/comments/1u1crn4/emails_not_showing_up_in_gmail/

Attachment-specific corroboration:

- A Google Gmail Community author reports that PDF-content search stopped
  working around April 2025 while PDF-title search still worked:
  https://support.google.com/mail/thread/354141668/gmail-search-not-working-for-pdfs?hl=en

This is a genuine cluster, but it is not one exact technical mechanism. G1 and
G2 are largely ranking/scope incidents with a free resolution. G5 is substring
tokenization. G6 and the PDF report concern attachment retrieval. G7 may include
sync or list visibility. A landing page must not imply that one change solves
all of them.

### Current discovery and prevalence

DataForSEO Google Ads keyword checks were run for US English on 2026-07-19. The
returned data was last updated around 2026-07-14. Three requests cost **$0.03756
in total**.

| Query | US monthly volume | Intent | CPC | Difficulty | Recent signal |
|---|---:|---|---:|---:|---|
| `gmail search not working` | 260 | Informational | Not returned | 0 | Jan–Jun 2026 ranged from 210 to 480 |
| `gmail search not finding emails` | 20 | Informational | Not returned | 0 | Jan–Jun 2026 ranged from 10 to 30 |
| `gmail search attachments` | 110 | Navigational | Not returned | 4 | Mostly stable at 110 |
| `search gmail attachments` | 110 | Navigational | Not returned | 2 | Current measurable demand |
| `find old emails in gmail` | 90 | Informational | Not returned | 0 | Jan–Jun 2026 ranged from 50 to 110 |

`gmail most relevant search` returned no keyword item. This is modest support
intent, not a large commercial category. Zero reported difficulty and absent CPC
also suggest that search visibility alone would not demonstrate purchase intent.

Current public corroboration:

- Google's 2025-03-20 product announcement explains that `Most relevant` ranks
  results using recency, clicked emails, and frequent contacts, with a toggle to
  `Most recent`:
  https://blog.google/products-and-platforms/products/gmail/gmail-search-update-relevant-emails/
- A Gmail Community thread about `Most relevant`, dated 2025-05-21, showed 997
  subscribers and 47 replies when observed; the practical workaround is to
  switch ordering for each search:
  https://support.google.com/mail/thread/345874358?hl=en&msgid=360955277
- Google's current operator documentation covers sender, subject, dates,
  attachments, filenames, exact phrases, `in:anywhere`, and exact-word `+`:
  https://support.google.com/mail/answer/7190?hl=en-eu

The support activity proves current friction. It does not establish that the
user wants to replace Gmail, install a client, or pay.

### Free and paid counterevidence

#### Gmail's own free controls often finish the job

Within the incident set, successful fixes include `Most recent`,
`in:anywhere`, exact date ranges, wider sync range, and desktop web. Gmail also
documents advanced operators for sender, subject, attachment, filename, phrase,
and scope. These are adequate complete fixes for a material share of the
observed incidents.

Google now also offers AI Overview search for eligible Workspace accounts and
personal users on paid Google AI plans. It accepts natural-language inbox
questions but is unavailable when operators are used:

- https://support.google.com/mail/answer/16789526?hl=en
- https://blog.google/products-and-platforms/products/gmail/gmail-is-entering-the-gemini-era/

Google is therefore both the free incumbent and a paid search incumbent.

#### Thunderbird is a strong free live-client substitute

Thunderbird's free, cross-platform global search indexes messages across
accounts and folders and supports sender, recipient, subject, body, and faceted
filtering. Its documentation was updated 2025-03-14:

- https://support.mozilla.org/en-US/kb/global-search

The RMA incident explicitly recommends Thunderbird “only for searching.” A
separate paid-client user says they keep Thunderbird for deep searches because
it finds a query their preferred eM Client does not:

- https://forum.emclient.com/t/better-search-than-gmail-or-thunderbird-please/104663

This is direct evidence that search matters inside a live-client workflow, but
the observed winner is free Thunderbird.

#### MailStore Home is a strong free archive substitute

MailStore Home is free for private use on Windows and supports Gmail, IMAP,
Outlook, large-volume archive search, attachment content, export, and
migration:

- https://www.mailstore.com/en/products/mailstore-home/
- https://help.mailstore.com/en/home/Accessing_the_Archive

It is Windows-only and creates a separate archive workflow, so it is not a full
cross-platform everyday-client answer. It is nevertheless an adequate free
incumbent for the narrow “find an old item” job.

#### Paid clients do not automatically search better

eM Client documents wildcard and advanced search and can search attachment
names or contents when messages are fully cached:

- https://www.emclient.com/faq-getting-started?search=.em
- https://www.emclient.com/faq-em-client-features

Superhuman markets AI retrieval, but direct paying-user discussion cuts the
other way: long-time users say they return to Gmail, Apple Mail, or other tools
for serious search:

- https://www.reddit.com/r/SuperhumanEmail/comments/1i3nqvr/why_is_search_so_bad/
- https://superhuman.com/products/mail/gmail-alternative

The Reddit evidence establishes paid broader-client adjacency, but not a paid
transition caused by this exact Gmail failure. It also warns against assuming a
premium client will be trusted more than provider search.

### Same-person paid adjacency

The route is structurally closer to Tecotype than migration or recovery:

1. the user owns the mailbox;
2. the same user performs the search;
3. the same user can connect Gmail to a desktop client;
4. the client can remain in the normal inbox/reply/archive workflow after the
   message is found.

What was **not** observed:

- an incident author paying for a broader client because it solved the miss;
- repeat everyday use after the one known message was recovered;
- willingness to pay Tecotype's intended price;
- a recommendation surface that sends affected users to Tecotype.

The eM Client and Superhuman discussions show that broader-client payers care
about search. They do not meet the stricter same-person transition requirement
for the retained Gmail incidents.

### Product and release truth

Verified against `product.md`, `positioning.md`, and `../tecotype` on
2026-07-19:

- Gmail OAuth connection and generic IMAP account connection exist.
- Tecotype has local lexical search and optional on-device semantic search.
- The local lexical document currently contains message subject and body, not
  attachment filename or attachment content.
- Search queries exclude Junk and Trash in the current implementation.
- Lexical query terms are combined as tokens; a substring such as `8812340`
  inside `X1ZT8812340` is not verified to match.
- The same Junk/Trash exclusion applies while hydrating semantic candidates.
- Full historical sync, attachment-content indexing, exact/wildcard behavior,
  and parity across every retained failure were not verified.
- Migration auditing, provider-independent local recovery, and EML import were
  not verified as shipped capabilities.
- The public acquisition experience, licensing, and payment flows remain
  unfinished, and the release is Mac-first.

Implication: current Tecotype search may help ordinary subject/body retrieval,
but it cannot truthfully claim to solve G1–G7 as a set. Trash, Junk,
partial-token, attachment-name, attachment-content, and complete-history
coverage must be implemented and verified before comparison copy.

## Rejected route: verified mailbox migration audit

### Direct incidents opened

| Date | Source type | Incident | Workaround or recommendation | Why it does not form the funnel |
|---|---|---|---|---|
| Page displayed about Jan 2026 | Reddit Google Workspace admin post | The source still contained old mail, but the destination initially had only two days. After the native migration path was explained, a later author reports 4,500+ expected messages but only about 250 found despite advanced Gmail searches. | Run Admin Data Migration; inspect source and destination. | Mixes “migration never run” with an incomplete migration; admin actor. |
| Around 2025-04-20 | Reddit Google Workspace/GSuite admin post | An official O365-to-Google migration showed about 30,000 messages, while a second native migration surfaced roughly 40,000 more. | Rerun with the new migration tool, check All Mail/conversation mode and reports; CloudFuze is pitched. | Strong silent-count discrepancy, but business admin/project-tool buyer. |
| 2025-04-15 | Google Workspace Community | After Namecheap-to-Workspace migration, older messages are missing in Gmail but visible in Outlook. | Follow Google's migration guide and seek provider support. | One provider/tool path; resolution not observed. |
| 2025-04-11 | Google Workspace Community | Moved folders initially appeared in the destination, then were empty the next day and messages were gone from both accounts. | Admin restore, support, Takeout, or Vault. | Post-move deletion/recovery rather than a pure audit mechanism. |
| Date not exposed | Zoho Community | A GSuite-to-Zoho IMAP migration reports success and no errors, but many messages are missing; rerunning risks duplicates. | No confirmed fix on the retained page. | Exact silent-loss symptom, different provider and tool. |
| 2025-06-25 documentation update | Official Microsoft troubleshooting article | Remote Exchange migrations can leave folder data missing due to transient errors or corrupt folders. | Administrator restores soft-deleted data within 30 days through a temporary mailbox/PST workflow. | Enterprise recovery, privileges, and deadline; not Individual acquisition. |

Sources:

- https://www.reddit.com/r/googleworkspace/comments/1ql09km/emails_have_not_migrated_to_google_workspace/
- https://www.reddit.com/r/googleworkspace/comments/1k3nfm1/
- https://support.google.com/a/thread/338410743/emails-missing?hl=en
- https://support.google.com/a/thread/337532473/
- https://help.zoho.com/portal/en/community/topic/emails-missing-after-import-from-gsuite-caldav-issues
- https://learn.microsoft.com/en-us/troubleshoot/exchange/move-or-migrate-mailboxes/restore-missing-folder-data-after-migration

These reports prove that migrations can appear complete while mail is missing.
They do not form one consumer mechanism. Causes include a migration never being
started, incomplete passes, provider differences, labels/folders, transient
errors, corrupt folders, deletion after a move, and attachment or size limits.

### Discovery, incumbents, and actor mismatch

DataForSEO returned strong commercial demand for broad migration tools:

| Query | US monthly volume | Intent | CPC | Difficulty |
|---|---:|---|---:|---:|
| `email migration tool` | 880 | Commercial | $22.65 | 27 |
| `imap migration tool` | 140 | Commercial | $6.93 | 14 |
| `migrate email to google workspace` | 70 | Transactional | $18.09 | 0 |

But `email migration checker`, `compare imap mailboxes`, `verify mailbox
migration`, `missing emails after migration`, and `recover local email files`
returned no keyword items. The visible market is migration execution, not a
separate post-migration verifier.

Current official Google migration is admin-led and supports date ranges and
options for deleted mail, spam, and excluded labels:

- https://support.google.com/a/answer/14792635
- https://workspace.google.com/solutions/migration/gmail-migration/

Observed recommendations are provider migration reports, reruns or delta sync,
Google/Microsoft support, imapsync, CloudFuze, MigrationWiz, and other specialist
tools. The buyer is normally an admin, MSP, or business migration operator;
mailbox end users experience the loss. That breaks same-person Individual paid
adjacency.

Complete verification also requires more than comparing visible counts:
message IDs, duplicates, folders versus labels, internal dates, flags, deleted
and spam scopes, attachment bytes, source-side exclusions, and provider
transformations all matter. A one-time audit ends when the migration is accepted
or repaired. This is a terminal project and has no observed route into sustained
Tecotype use.

## Rejected route: recovering local bytes after provider or profile failure

### Direct incidents opened

| Date | Source type | Incident | Workaround or recommendation | Result |
|---|---|---|---|---|
| 2024-06-21 | Microsoft Community | An old provider is disconnected and the author asks whether years of mail can be recovered through New Outlook. | New Outlook has no usable local copy; recover from Classic/export if one exists, otherwise the data may be unrecoverable. | Terminal counterevidence: the bytes may not exist locally. The Classic route is excluded. |
| Page displayed `12d ago` when accessed 2026-07-19 | Reddit Thunderbird post | Five accounts and Local Folders disappear after a restart; later evidence points to broader filesystem loss. | Re-fetch IMAP content and restore Local Folders from backup. | System/profile recovery, not one mail-client mechanism. |
| Page displayed about May/June 2026 | Reddit Thunderbird post | A domain is deleted, but backed-up Thunderbird profile bytes remain and the author struggles to restore them. | Copy the mailbox into Local Folders or restore the profile. | A free manual path exists if the bytes are intact. |
| Around Feb 2026 | Reddit sysadmin post | An old server is gone; a 7 GB Apple Mail cache includes attachments, but copying and Thunderbird import are unreliable. The author wants MIME reconstruction and upload to a new IMAP account. | No confirmed response. | Highly technical, client-specific recovery and reconstruction. |

Sources:

- https://learn.microsoft.com/en-us/answers/questions/4678679/
- https://www.reddit.com/r/Thunderbird/comments/1sz3ajk/entire_profile_gone/
- https://www.reddit.com/r/Thunderbird/comments/1to01xl/recover_of_deleted_emails_under_imap/
- https://www.reddit.com/r/sysadmin/comments/1rb2i98/recovering_apple_mail_cached_imap_mail_domain/

The routes differ by whether bytes exist, whether they are complete, mailbox
format, attachment representation, profile corruption, filesystem loss, and
server availability. Successful workarounds are backup restore, manual profile
copy, Thunderbird Local Folders, or professional data recovery. The job ends
when the data is recovered or declared lost. The high consequence, uncertain
completeness, and implied recovery guarantee create liability without direct
same-person willingness to buy a broader daily client.

## Rejected route: EML as a bridge into a live client

The route was retained only where the author wants old files inside a new active
mail account:

| Date | Source type | Incident | Recommendation | Outcome |
|---|---|---|---|---|
| 2024-03-25 | Google Workspace Community | The author has an old Stackmail backup in MBOX and EML and wants it inside a new live Google Workspace account. | Got Your Back (GYB) or Thunderbird connected over IMAP. | Free or open tooling provides the bridge. |
| 2025-01-10, follow-up 2025-01-19 | Google Gmail Community | The author wants to sync/copy historical mail into another active account. | Configure both accounts in Thunderbird or Outlook over IMAP and copy mail. | The author says the guidance was helpful. |

Sources:

- https://support.google.com/a/thread/265827146/importing-eml-and-mbox-files-into-workspace?hl=en
- https://support.google.com/mail/thread/317512909/sync-emails-to-another-account?hl=en

Thunderbird's current import documentation, updated 2025-03-11, supports
profiles, applications, and files, with a ZIP-size limitation:

- https://support.mozilla.org/en-US/kb/thunderbird-import

This route naturally reaches a live account in some cases, but it did not yield
five current homogeneous direct incidents. Thunderbird, GYB, and ordinary IMAP
copying are adequate incumbents. The user's goal is still a completed import,
not ongoing client use or payment.

## Minimum bounded experiment for the near-miss

Do not build migration, recovery, or EML acquisition pages from this pass. If
the Gmail route is tested, test an activation hypothesis rather than publish a
competitive claim.

### Product prerequisites

Before claiming a known-message advantage:

1. include optional Trash and Spam/Junk scopes with clear privacy and deletion
   semantics;
2. verify complete-history sync and make incomplete indexing visible;
3. support exact phrases, partial identifiers or documented wildcard behavior,
   attachment filenames, and—only with explicit local controls—attachment
   content;
4. explain why a result matched and which folders/scopes were searched;
5. test known provider cases against a fixed corpus without logging mailbox
   contents, addresses, subjects, attachment names, or search terms.

### Acquisition hypothesis

Candidate query:

> `gmail search not finding email`

Candidate promise, only after it is true:

> Find a message you know exists. Search your local mail copy across the scopes
> you choose, then keep working in the same private desktop client.

The important distinction is continuation. “Tecotype found one message” is not
enough. The same person must keep using the live inbox.

### Required measurement

```text
Exact-intent visit
  → Gmail connection
  → complete-enough sync/index
  → query where Gmail missed and Tecotype returns the intended message
  → later inbox/reply/archive use
  → 7-day and 30-day live-client retention
  → paid decision by that same person
```

Advance only if:

- at least five exact-intent users can demonstrate a Gmail miss and Tecotype hit
  without the research team seeing or retaining message content;
- the hit is not merely a missing `Most recent`, `in:anywhere`, date-range, or
  desktop-web workaround;
- users continue into normal mail activity after retrieval;
- paid conversion is attributable to the same person and search materially
  contributed to the decision;
- the sync delay and OAuth permission burden do not overwhelm intent;
- a current comparison/support page has a named evidence-review owner.

Kill or reframe if:

- most users finish with Gmail's free controls;
- Thunderbird or MailStore Home is the preferred answer;
- the majority want a one-time recovery utility;
- exact-intent visitors do not connect an account or wait for indexing;
- the search corpus cannot cover Trash, Spam, identifiers, and attachments
  predictably;
- retention resembles a terminal job;
- sensitive examples such as passport numbers become necessary to demonstrate
  value.

No impression, ranking, visit, message-found event, or install counts as
distribution. Under the workspace definition, none of these routes has a
partner providing permanent pre-install discovery plus an attributable
first-action-to-paid path.

## Final disposition

- **Gmail known-message retrieval:** keep as the only bounded experiment, after
  product coverage is real; not validated.
- **Verified migration audit:** reject as an Individual funnel; actor and buyer
  are usually admins, and the job is terminal.
- **Silent post-migration loss:** real pain, but causes and remedies are too
  heterogeneous for one honest promise.
- **Local-byte recovery:** reject; heterogeneous, high-liability, and often
  impossible because complete bytes do not exist.
- **EML-to-live-client:** reject/defer; fewer than five current homogeneous
  incidents and adequate free tooling.
- **Distribution:** null across the set.

