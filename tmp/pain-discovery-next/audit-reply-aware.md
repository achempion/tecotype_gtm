# Adversarial audit: reply-aware follow-up

Status: Independent audit only — not shipped, committed, or a channel recommendation.

Research date: 2026-07-19  
Audited candidate: `tmp/pain-discovery-next/workflows.md`  
Rubric: `pain-discovery-prompt.md`  
Tecotype source inspected at: `f7304ff75d845e3dedeaa9a7e55b6bf33fb98e19`

## Verdict

**NO-GO as a qualified acquisition opportunity.**

The exact pain can be repaired to **Confirmed pain, funnel unproven** after
adding independently opened Microsoft Q&A, LinkedIn, and Capterra observations.
Those sources fix the original ledger's fatal source-domain cap.

The opportunity still fails hard gates that a score cannot compensate for:

1. **Paid adjacency fails.** The candidate does not identify an additional
   job that the same free user subsequently encounters and needs Tecotype
   Individual to complete. It instead treats interest in, or prior use of, a
   broader client for the same reminder job as expansion evidence.
2. **Zero-user acquisition fails as written.** Existing Boomerang marketplace
   pages prove that add-ins can be listed, not that a Tecotype desktop client
   or a new sidecar would receive meaningful pre-install discovery. A current
   exact-feature Chrome extension had only 26 users.
3. **Requiring a client switch breaks the wedge.** A Tecotype-embedded free
   reminder asks a Gmail, Outlook, or Apple Mail user to install a different
   client, connect their mailbox, and wait for sync before the first free
   result. That is the high-friction product decision the free wedge is meant
   to precede.
4. **Spark Free is an adequate incumbent.** It supplies the exact conditional
   reminder inside a complete desktop client, plus unlimited accounts. Two
   people in the strongest recent thread actually switched to Spark; the
   original poster said everything they needed was free.
5. **Attribution and the proposed experiment remain incomplete.** The ledger
   does not establish how a direct marketplace install preserves a coarse
   source through a different desktop purchase, and it gives no numeric,
   time-bounded, or cost-bounded stop condition.

This does not reject reply-aware reminders as a product feature. Current
Tecotype source already contains a substantial reminder-and-cancellation
foundation. It rejects the present claim that giving this job away is a
qualified route to Individual.

## Confirmation gate

### Corrected independent evidence set

The original ledger alone could count at most three Reddit observations and
one Super User observation after the rubric's per-domain cap. That is four,
not five. The following independently opened sources repair the count without
relaxing the cap.

| ID | Direct source, publication date, source type | Exact first-person incident | Audit treatment |
|---|---|---|---|
| C1 | [Reddit / coldemail](https://www.reddit.com/r/coldemail/comments/1sbkekn/tool_for_remind_me_if_no_reply_across_multiple/), 2026-04-03, independent forum/community | A person managing 3–4 accounts manually creates and cancels reminders after human conversations begin. They specify send → remind after X days if no reply → cancel if replied. | Count. Exact trigger, state change, failure, and manual workaround. Founder replies in the thread are not counted. |
| C2 | [Reddit / productivity](https://www.reddit.com/r/productivity/comments/1ss6dm2/best_tool_for_snoozing_and_email_follow_up/), 2026-04-22, independent forum/community | A Mac/Exchange user wants a sent message returned to the primary inbox only when no reply arrives; Outlook flags are too clicky and Boomerang is too costly. | Count. The poster later chooses Spark and says the needed behavior is free. |
| C3 | [Reddit / Emailmarketing](https://www.reddit.com/r/Emailmarketing/comments/1peyj8i/what_is_the_best_tool_for_only_email_reminders/), 2025-12-05 page, independent forum/community | A substantive commenter had used Apollo to remind one week after a sent message received no reply and wanted one default rather than repeating the setup for unique messages. | Count the commenter, not the original poster. The original post asks for cheap reminders but does not itself specify reply-aware suppression. This reaches the maximum of three observations from Reddit. |
| C4 | [Microsoft Q&A](https://learn.microsoft.com/en-us/answers/questions/4585373/can-i-get-a-reminder-%2Aemail%2A-in-my-inbox-when-some), 2022-12-06, official support community | An office user handling many messages says Outlook's reminder still fires after a reply and can be dismissed or lost; they want an inbox item only when nobody responds. | Count. Concrete workload, exact failure, consequence, and desired behavior. The page currently shows 100+ people with the same question, but those votes are not direct observations. |
| C5 | [LinkedIn post](https://bm.linkedin.com/posts/yair-saperstein_gmail-remind-me-to-follow-up-if-no-reply-activity-7005568380711641088-aU8I), approximately 2022-12-05, independent firsthand account | The author wants an important sent message resurfaced after one week only if no reply arrives. They currently create Microsoft To Do or HubSpot tasks and tested Superhuman at $30/month. | Count. The page exposes “3y”; the approximate date is encoded by the public activity identifier, not printed as an absolute date. The post and comments also show observed recommendations. |
| C6 | [Capterra Boomerang review](https://www.capterra.com/p/174835/Boomerang/reviews/), 2021-02-16, app/directory review | A managing director and co-founder says the core behavior they use 95% of the time is returning mail after X time when no reply arrived. | Count. Verified, substantive first-person use. The review was incentivized, so it is retained with that limitation. |
| C7 | [Super User](https://superuser.com/questions/1431397/check-if-a-mail-got-a-reply-after-a-certain-amount-of-time), 2019-04-30, Q&A | A workplace user manually remembers which sent messages have no reply and explicitly rejects a generic reminder that fires regardless. | Count as an older durability observation. It had only 71 views when re-opened and is not a prevalence signal. |

The other original Reddit rows may corroborate the pain, but are unnecessary
to meet the count and cannot increase the retained Reddit total above three.

### Confirmation matrix

| Confirmation condition | Result | Adversarial finding |
|---|---|---|
| Five authors, three pages, two domains, two source types; domain/page caps | **Pass after repair** | C1–C7 provide seven independent authors on five operated domains and four fixed source types. Only three Reddit observations are counted. The original workflow ledger did not pass this condition without C4–C6. |
| At least two observations in the prior 24 months | **Pass** | C1–C3 are from 2025–2026. |
| Same actor, trigger, job, and failure mechanism | **Pass narrowly** | The defensible actor is an email-heavy professional sending important, individually written human messages. The shared trigger is sending such a message; the failure is having to remember or dismiss a reminder even after a reply; the job is conditional resurfacing. Do not broaden this to automated sequences, team shared inboxes, or CRM pipeline management. |
| At least three observations show behavior | **Pass** | Manual tasks/reminders, Outlook flags, Apollo, Mixmax, FollowUpThen, Boomerang, Superhuman, and Spark are directly reported. |
| Independent prevalence/discoverability signal | **Pass, weakly** | The current [Google Workspace Marketplace Boomerang page](https://workspace.google.com/marketplace/app/boomerang/907372061162) shows 401K+ installs and explicitly offers no-reply reminders. This is adoption of a multi-feature workaround, not feature-specific usage. Current exact-intent SERPs also contain multiple maintained solutions. |
| Current SERPs and cited pages opened | **Pass in this audit** | Every page retained above was opened. Current searches included `"remind me if no reply" email tool`, `email reminder if no reply Outlook add-in`, and `email client automatic follow up reminders if no reply`. No DataForSEO task was run in this audit. |
| Contradictions and adequate incumbents addressed | **Pass after audit supplementation** | Spark Free, Gmail Nudges, Apple Mail Follow Up Suggestions, Airmail, eM Client, Boomerang, and the low-use Chrome entrant are addressed below. The original ledger covered Spark and Boomerang but omitted several current native/client fixes. |

**Confirmation classification: Confirmed pain, funnel unproven.**

## Opportunity hard gates

| Hard gate | Result | Reason |
|---|---|---|
| Useful free outcome | **Pass as Proposed** | “Set a date on this sent thread; resurface it only if no recipient reply arrives” is a complete narrow job if it remains free, works across the accounts promised, and clearly discloses that the desktop must sync. It must not be limited to one account merely to manufacture an upgrade. |
| Private data boundary | **Pass as Proposed** | Reply matching, deadline state, and reminder display can remain in the local client. Tecotype infrastructure need not receive credentials, message content, participants, subjects, or thread identifiers. Multi-device coordination is not solved; the promise must be device-scoped unless a private design is verified. |
| Desktop relevance | **Pass** | C1, C2, C4, C6, and C7 concern desktop or provider-web workflows. The job is not mobile-only. |
| Specific zero-user source | **Fail** | Existing marketplace listings are inventory for add-ins, not evidence of a discoverable Tecotype desktop-client route. No Tecotype listing, acceptance, ranking, impressions, or persistent placement exists. Exact search is incumbent-heavy, and no query volume or rankability evidence was produced. |
| Recommendation or sharing | **Pass narrowly for a validation hypothesis; no sharing loop** | In the exact LinkedIn thread, peers recommend Boomerang, Followup.cc, Spark, Apollo, and Sortd; in the 2025 Reddit thread, two users report landing on FollowUpThen. The named actor is a peer with the same job, the surface is the public help thread, and the incentive is helping another user solve it. No recipient of the email sees or benefits from the reminder, so there is no product-native loop and no Tecotype recommendation commitment. |
| Paid adjacency | **Fail** | No additional job, timing, and frequency are evidenced for the same free user. The strongest records show users leaving premium bundles, setting a $5–10 ceiling, buying a one-time plug-in, or choosing Spark Free. Whole-client Superhuman reviews establish payment for a bundle, not movement from this completed free job to another Individual job. |
| Private attribution | **Unknown** | A Tecotype-owned landing page could carry a coarse campaign token into a download and later send content-free activation and purchase events. The candidate instead leans on direct marketplace installs and does not show how their source survives into a separate desktop-client purchase. No mailbox-level data is needed, but the stage-by-stage mechanism is not specified or verified. |
| Bounded testability | **Fail as documented** | The proposed experiment has no sample size, duration, maximum cost, success threshold, failure threshold, or numeric stop condition. “Kill if users repeatedly remain in Gmail/Outlook/Apple Mail” is directionally correct but not a bounded experiment. |

Because three opportunity gates fail and one is unknown, the candidate is not
eligible for ranking or recommendation regardless of a prioritization score.

## The Spark and client-switch test

[Spark's current follow-up documentation](https://sparkmailapp.com/help/sending-emails/set-follow-up-reminders)
describes the exact state machine on Mac and Windows: choose a time while
writing or replying, and Spark reminds only if nobody replies.

[Spark's current pricing page](https://sparkmailapp.com/pricing) lists:

- a €0 Free plan;
- unlimited email accounts;
- reminders among the essential inbox features;
- cross-device sync, unified inbox, scheduled send, snooze, and a command
  center in the plan comparison.

The recent direct behavior is more important than vendor inventory:

- C2 says everything needed is free after switching from Outlook to Spark.
- A second independent author in that thread also switches to Spark and says
  it is better than Outlook, while still missing Superhuman's automatic
  reminders.

This creates two separate acquisition failures:

1. **Embedded-free route:** the person must switch clients before receiving
   the free value. The “free utility” no longer lowers the commitment required
   for Tecotype activation.
2. **Sidecar route:** a Gmail/Outlook add-in or Chrome extension could produce
   value without a client switch, but it is a net-new product and the later
   move from sidecar to Tecotype requires a second installation, mailbox
   connection, and workflow migration. No retained source shows that people
   who successfully solve reminders this way then want to switch clients.

Spark is therefore not merely feature competition. It demonstrates that the
exact free job and the broader multi-account client can be delivered together
at €0. Tecotype's €15/month or €149/year Individual price needs evidence for a
different next job; the reminder cannot provide that evidence by itself.

## Paid-adjacency audit

Evidence that initially looks positive does not pass the hard gate:

- The LinkedIn author tested Superhuman, but says Superhuman solved this same
  job and then lists calendar, team-awareness, and $30/month problems. They
  subsequently report Apollo may be the winner. This is switching among
  terminal solutions, not an observed free-to-paid sequence.
- The iOS Reddit user says the reminder is the only Superhuman function they
  miss and wants to leave because it is expensive. This is direct
  cannibalization evidence.
- The Mac/Exchange Reddit user will pay only $5–10 and ends on Spark Free.
- The Mixmax user explicitly wants to pay as little as possible and adopts
  FollowUpThen.
- The Outlook user buys a one-time $29.99 plug-in and recommends it. That
  validates a narrow utility purchase, not recurring Individual expansion.
- The agency owner considering $30 tools after losing a warm lead reports no
  purchase, does not clearly specify the conditional state machine, and is
  told by other participants that the job is CRM pipeline management.
- Current G2 and App Store reviews praise Superhuman's broader bundle.
  Visible reviews mention reminders generically alongside AI, speed, triage,
  multiple accounts, and calendar work; they do not identify a subsequent job
  arising after a free reply-aware result.

The exact missing evidence is two independent people from the same bounded
segment who:

1. complete reply-aware follow-up for free;
2. then encounter a named additional mail job;
3. need that job with recurring timing or frequency;
4. choose or seriously attempt a broader desktop client for it; and
5. are the same buyer or decision-making unit.

“They already use email heavily” and “Superhuman includes reminders” do not
substitute for this sequence.

## Native and incumbent counterevidence

| Current source | What it changes |
|---|---|
| [Gmail Help: Nudges](https://support.google.com/mail/answer/6585?co=GENIE.Platform%3DDesktop&hl=en) | Gmail can automatically surface sent emails that may need follow-up. It does not offer the candidate's user-chosen deadline, but it satisfies a portion of the audience without another install. |
| [Apple Mail on Mac: Follow Up Suggestions](https://support.apple.com/en-mide/guide/mail/mlhlp1052/mac) | Apple Mail automatically resurfaces a sent message after three days without a response. Again, timing is not user-chosen, but the default client covers the basic job. |
| [Spark follow-up reminders](https://sparkmailapp.com/help/sending-emails/set-follow-up-reminders) and [pricing](https://sparkmailapp.com/pricing) | Exact conditional reminders, desktop support, and unlimited accounts are available in a free broader client. Strongest counterevidence. |
| [Airmail follow-up reminders](https://help.airmailapp.com/en-us/article/follow-up-reminders-c4n5t9/) | A maintained 2026 help page documents chosen-time reminders only when no reply arrives. |
| [eM Client Watch for Reply](https://www.emclient.com/blog/never-miss-important-emails-with-em-client-s-watch-for-reply-feature-448) | A paid broader client provides the exact job and keeps an Unreplied folder. It supports the pain but increases incumbent density. |
| [Boomerang for Outlook](https://marketplace.microsoft.com/en-us/product/office/wa104379606?tab=overview) and [Boomerang for Gmail](https://workspace.google.com/marketplace/app/boomerang/907372061162) | Long-lived add-ins already occupy the obvious provider marketplaces. The Google listing requests broad mail and contacts permissions, which gives a local design a privacy angle but not a discovery advantage by itself. |
| [Current exact-feature Chrome extension](https://chromewebstore.google.com/detail/gmail-follow-up-reminder/gdljfkmjgalnncjbhkgngmlpklbhlhnf) | The listing claims local storage, no account, a free allowance, and $5/month unlimited use. It had 26 users and one rating, direct evidence that publication alone is not distribution. |

## Tecotype implementation and release truth

The original ledger says no current implementation claim is made, but current
source contains more foundation than that wording suggests:

- `native/src/mail/ingest.rs` calls a reminder-cancellation helper after
  persisting a message.
- `native/src/mutations/repository.rs` clears a pending reminder when a fresh
  message in the thread arrived after scheduling.
- `src/views/threadView/components/ThreadEventRow.tsx` renders “Reminder
  cancelled by reply.”

This is **Current foundation**, not proof of a public release or an exact
completed implementation. The current helper cancels on a fresh thread message
rather than proving that a qualifying recipient replied to the user's
particular outbound message. Auto-replies, another participant, the user's own
later message, and provider-threading edge cases need explicit semantics and
tests. No public Tecotype release, marketplace listing, entitlement, or
attribution path was established in this audit.

## Exact blockers and reopening conditions

Do not advance this as a qualified free-to-Individual opportunity unless all
of the following materially new evidence appears:

1. **Choose one acquisition form.** Either a low-friction provider sidecar or
   an embedded desktop-client entitlement; do not combine their funnels.
2. **Prove zero-user reach for that form.** Record the exact source, current
   eligible audience, placement/ranking mechanism, attributable destination,
   and observed or contractually committed visibility. A generic marketplace
   listing is insufficient.
3. **Repair paid adjacency.** Obtain the same-person sequence specified above
   for a named additional Individual job. Do not use second-account gating if
   it prevents the free promise from working across the accounts the actor
   already needs.
4. **Resolve client-switch friction.** Show that people will connect and sync
   a new desktop client for this result despite Spark Free and native
   Gmail/Apple suggestions, or show that a sidecar's successful users later
   initiate a separate client switch.
5. **Specify private attribution.** Name content-free events from source,
   first rule set, correctly suppressed/fired reminder, adjacent-job trigger,
   desktop activation, purchase, and retained milestone; identify the store or
   installation handoff breakpoint.
6. **Bound the experiment.** State sample size, duration, maximum cost,
   success and failure thresholds, and a stop condition before launch.
7. **Add economics.** Use the required funnel and CAC formulas with unknowns
   left unknown; include maintenance and support for free users across Gmail,
   Microsoft, IMAP, provider threading, and offline-device behavior.

Until then, retain reply-aware follow-up as a confirmed product pain and a
possible feature-level priority, not as a recommended acquisition wedge,
sharing loop, or distribution route.

## Source protocol and limitations

Every source retained in this audit was opened on 2026-07-19. The Microsoft
short URL initially failed safety resolution, so the exact indexed title was
searched and the canonical underlying page was then opened. The LinkedIn page
prints only a relative age; its approximate publication date is disclosed
accordingly. No account was created, no form was submitted, no software was
installed, and no external write was made. No DataForSEO request was used.

This was an independent red-team audit of one finalist, not a new full
60-minute discovery run. It does not claim to satisfy the parent prompt's
portfolio-wide time, page, query, or DataForSEO coverage floors by itself.
