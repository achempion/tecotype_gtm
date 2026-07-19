# Spark Mail lessons and staged opportunities for Tecotype

Research date: **2026-07-17**

Decision update: **2026-07-19**

Archive notice: the candidate tests below are historical; none is a current
**Experiment**. Use the [current decision](../../next-acquisition-funnel.md)
and [acquisition gate](../readme.md#one-hard-gate).

This document converts Spark's public evidence into bounded Tecotype tests. It
does not recommend a channel merely because Spark uses it, and it does not
present Tecotype's planned release work as shipped.

## Product-truth boundary

Tecotype is under active development. The repository contains a working
desktop product and tooling for a signed/notarized **Apple Silicon** release
target, but it does **not** establish that a public macOS release has shipped.
The website, onboarding, licensing/payment, Gmail restricted-API audit,
compose/sending safety and polish, updates, installers, and public
distribution remain release gates.

Windows distribution is planned, including a signed NSIS package, Microsoft
Store acquisition, a direct fallback, and self-hosted updates. It has not
shipped publicly and must not be described as available.

Current defensible product statements are narrower:

- keyboard-first desktop email client;
- Gmail and generic IMAP support;
- local storage, synchronization, and search;
- optional on-device Better search;
- reminders, Split Inboxes, drafts, and sending implemented to varying levels
  of completeness;
- Mac-first release direction.

Every feature and platform claim still requires release-build verification
before public use.

For current GTM planning, assume the eventual published client is ready on
macOS, Windows, and Linux. The platform-gated sections below preserve the
historical 2026-07-17 release sequence; route decisions are based on pain,
host access, capacity, conversion, and economics rather than incomplete
packaging.

Tecotype Individual is decided at **€149/year or €15/month**, with annual as
the primary offer. These are real billing cadences, not annualized monthly
equivalents.

## What Spark demonstrates

| Spark signal                                               | Defensible lesson                                                                     | Missing evidence                                                   |
| ---------------------------------------------------------- | ------------------------------------------------------------------------------------- | ------------------------------------------------------------------ |
| Free product since 2015 and current stores                 | Useful free distribution can accumulate durable proof and branded coverage            | Incremental active users, support cost, and free-to-paid economics |
| Timed iPad and Android launches around Mailbox/Inbox exits | Category displacement can create unusually qualified intent                           | Causal migration and retention                                     |
| 12 Product Hunt launches                                   | Meaningful platform/feature releases can repeatedly create attention                  | Visits, activation, and revenue                                    |
| 5,509 keywords and 132.0K modeled ETV                      | Owned content can create large discovery beyond the homepage                          | 70.8% is one low-intent page; conversion is private                |
| Ten current Google ad creatives                            | Paid acquisition is active                                                            | Spend, CAC, incrementality, and retention                          |
| Source cookie and CTA/checkout events                      | A web funnel can preserve source and distinguish free, paid, plan, and cadence intent | Cross-client attribution and actual rates                          |
| Free + true monthly/annual paid plans                      | A persistent free tier and real cadence choice lower entry pressure                   | Conversion, abuse, support, and churn                              |
| Setapp                                                     | Bundles create an additional paid-user discovery surface                              | Economics and customer ownership                                   |
| Two Mac apps and 2022 transition                           | Preserving a legacy path can reduce forced migration                                  | It also fragments product identity and support                     |
| 19.5M downloads and 154K aggregate ratings                 | Large scale proof is visually persuasive                                              | Definitions, platform/date mix, active use, and paid status        |
| Homepage “never shared” plus detailed exceptions           | Privacy copy affects consideration                                                    | Broad assurance can conflict with the real data-flow contract      |

## Priority 1: pre-release research

These activities can happen without implying public availability.

### 1. Find language Spark does not already own

Spark currently leads with “Smart. Focused. Email.” Tecotype should not answer
with another broad focus or productivity superlative.

Compare four accurate concepts with one interface image:

1. **Calm control:** mail handled without urgency mechanics.
2. **Keyboard flow:** process Gmail and IMAP work without leaving the keyboard.
3. **Local recall:** find a message using the way it is remembered.
4. **Private intelligence:** optional Better search runs on the device.

Use:

- moderated interviews;
- message-comprehension tests;
- static research pages clearly labeled as in development;
- questions that ask participants to restate the product, audience, and
  inferred data flow.

Do not use a Download, Start Trial, or platform-availability CTA.

Decision:

- choose the clearest accurate recollection among the most qualified audience;
- keep calm as the emotional distinction and speed/privacy as proof;
- reject language that sounds like Spark's broad productivity suite.

### 2. Make the privacy data flow a product proof

Spark's homepage compresses data use into “never shared,” while its policy
describes server features, processors, analytics, integrations, AI providers,
and retention.

Tecotype should prepare one plain-language matrix:

| Capability              | Runs where                    | Data involved                      | External party               | Optional?                      |
| ----------------------- | ----------------------------- | ---------------------------------- | ---------------------------- | ------------------------------ |
| Gmail/IMAP sync         | Verify release implementation | Mail and authorization material    | User's email provider        | Required for connected account |
| Local search            | Device                        | Local working copy                 | None beyond provider sync    | Core                           |
| Better search           | Device                        | Local index/content                | Verify current model/runtime | Optional                       |
| Diagnostics/measurement | Define before release         | Non-content event/failure metadata | Define and disclose          | Consent/control required       |
| Licensing/payment       | Define before release         | Entitlement and billing data       | Payment provider             | Required for paid use          |

Test whether a reader can answer:

- Does mail still travel through Gmail or the IMAP provider?
- Which search runs locally?
- Does Better search send content to a model provider?
- What diagnostics are collected?
- What changes if they decline optional measurement?

Do not use “mail never leaves your device.” Tecotype still communicates with
the person's email provider.

### 3. Define source-to-value measurement before traffic

Spark exposes a thoughtful web event layer, but its activation rates remain
private. Tecotype should define:

- source, medium, campaign, and content;
- intended platform;
- provider family;
- verified signed acquisition;
- successful authorization;
- mailbox-ready state;
- first meaningful keyboard action;
- first meaningful local-search or Better-search result;
- retained meaningful use;
- billing outcome;
- crash, send/sync failure, support, refund, and account deletion.

Use no message text, subject, sender, query, recipient, or content-bearing
payload. Specify consent, deletion, aggregation, access, and retention before
implementation.

The center of the model is retained first value, not page views or downloads.

### 4. Prepare a category-event playbook

Spark's iPad and Android timing around Mailbox and Google Inbox exits is one of
its strongest acquisition lessons.

Maintain a watchlist for:

- client or provider shutdowns;
- price or platform-support changes;
- privacy-policy changes;
- OS architecture or signing transitions;
- workflow removals that affect the qualified Tecotype audience.

For each event, predefine:

- affected people and platform;
- migration requirements;
- accurate comparison claims;
- import/setup help Tecotype can genuinely provide;
- reviewer/community contacts;
- release-readiness threshold;
- a “do not launch” condition.

An opportunity does not override product truth. Do not exploit a category
event unless the relevant Tecotype build can safely absorb the users.

### 5. Choose one high-intent search wedge

Spark's search scale is dominated by a CC/BCC explainer. Tecotype should
research briefs for:

- keyboard-first email client for Mac;
- local email search on Mac;
- Gmail and IMAP desktop client for Mac;
- a calm alternative for people who work from email.

Validate query language and fit. A research or waitlist page must state its
status unambiguously. Do not publish an availability page before the linked
build ships.

## Priority 2: macOS release-gated acquisition

These tests begin only when every relevant public-release gate clears.

### 6. Run one complete Mac intent-to-retention experiment

```text
one qualified source or page
→ signed/notarized Apple Silicon public acquisition
→ verified install and update trust
→ successful Gmail or IMAP authorization
→ mailbox-ready threshold
→ first meaningful keyboard or local-search value
→ retained use
→ €149/year or €15/month outcome
```

Primary metric:

> qualified retained activation per eligible visitor.

Guardrails:

- provider-authorization failure;
- time to mailbox readiness;
- sync completeness;
- crash-free first sessions;
- compose/reply/send safety;
- support contact;
- privacy opt-out;
- uninstall/account deletion;
- refund.

A click or file download is not an activation.

### 7. Keep one Mac product and one migration contract

Spark's 2022 transition combined a new implementation, changed interface,
missing parity, and monetization. Spark Classic reduced forced migration but
left two live Mac identities.

Tecotype should:

- avoid launching a replacement client before the first product contract is
  understood;
- keep release notes, requirements, update behavior, and feature truth in one
  canonical place;
- preserve settings and local data across updates;
- define rollback/recovery before broad distribution;
- introduce major workflow change separately from price change where possible;
- never use roadmap parity as current capability.

### 8. Test a calm trial and clear offer

If a trial is used, test starting it at:

- successful first account connection;
- mailbox readiness;
- first meaningful action.

Do not start a trial clock at download. Use the actual offers:

- €149 billed annually;
- €15 billed monthly.

Show:

- exact charge and renewal cadence;
- what remains usable after trial, if anything;
- cancellation and data-deletion behavior;
- no false urgency;
- a pressure-free Later path.

Spark demonstrates that a functional free tier can lower friction. It does not
show that Tecotype should absorb the operational cost of Free. Model support,
provider/API, abuse, storage, and conversion before choosing that structure.

### 9. Earn narrow review proof

After reliability gates:

- brief Mac email reviewers;
- include keyboard-workflow and privacy-literate technical writers;
- provide reproducible Gmail/IMAP, search, Better search, and sending
  scenarios;
- give a current claim/data-flow sheet;
- request no guaranteed sentiment;
- measure retained activation and support burden by source.

Spark's decade-long press footprint compounds. Its desktop criticism shows why
review traffic should follow quality, not precede it.

## Priority 3: Windows release-gated acquisition

Windows is a separate public promise.

### 10. Complete a Windows distribution contract

Before publishing availability, verify:

- signed NSIS package;
- Microsoft Store acquisition where appropriate;
- direct fallback;
- SmartScreen-aware trust experience;
- self-hosted updates;
- current Windows requirements;
- Gmail/IMAP onboarding;
- mailbox readiness;
- compose/reply/send smoke tests;
- privacy-bounded crash/update diagnostics;
- release and rollback procedures.

Do not reuse a Mac screenshot, conversion rate, rating, reviewer quote, or
“cross-platform” statement as Windows proof.

### 11. Repeat the funnel with platform segmentation

Use the same semantic event definitions so Mac and Windows cohorts can be
compared, but keep the results separate:

```text
Windows-qualified source
→ verified signed Windows distribution
→ install and update trust
→ provider connection
→ mailbox ready
→ first value
→ retention
→ payment
```

The first Windows availability page should ship with the product. An earlier
research or notification page is acceptable only when its status is explicit.

## Priority 4: later scale

### 12. Test paid search only after activation works

Spark's 10 current creatives prove that a mature email client advertises. They
do not prove efficient acquisition.

The first confirmed cluster is people whose locally present Classic Outlook
mail is omitted from search after the applicable Microsoft checks fail. The
canonical design and subsequent economic rejection are in
[the broken-Outlook-search evidence](../../confirmed-pain-opportunities.md#classic-outlook-omits-a-known-locally-present-message).

Start with:

- Windows and Classic Outlook only;
- the narrow `outlook search not finding emails` cluster;
- one accountless local-retrieval promise;
- one qualifying landing page;
- a small fixed spend;
- intended-result-to-live-mail-to-retained-paid measurement;
- quality and refund guardrails.

At a realistic 0.2%–0.36% click-to-paid range, its $0.75 CPC implies $375 CAC
at 0.2% and $208 at 0.36%; 90 modeled monthly searches also prevent meaningful
scale. Use it only for bounded learning. Stop if clicks do not produce
confirmed retrieval, or retrieval does not survive live-mail setup and
retention. Never optimize to impression, click, or download volume.

The Superhuman All Accounts pain is also confirmed, but its
[paid funnel is disqualified](../../confirmed-pain-opportunities.md#superhuman-separates-active-accounts-into-tabs):
40 modeled monthly searches at $15.19 CPC require 30.38% click-to-paid to meet
the $50 media-CAC gate.
Spark is important counterevidence: its permanent free client already offers
unlimited accounts and a unified inbox. Tecotype therefore cannot qualify by
making All Accounts read-only or charging for reply/archive/move. The test is
whether inexpensive organic visitors to a dated comparison retain and buy,
not whether the unified-inbox feature is unique.

Raycast local mail search was previously proposed as a free discovery
integration. It is now parked as a product idea because Store acceptance and
usefulness do not establish capacity for 10 paid users/month or a same-user
paid bridge.

Reply-aware follow-up was also independently confirmed as a real pain, but it
was rejected as the next acquisition wedge. Spark Free supplies the exact
“remind me only if nobody replies” result in a full client; affected users
also report choosing Spark Free or seeking a cheap terminal utility. Current
Microsoft, Google, and Chrome marketplace listings prove that inventory
exists, not that Tecotype would receive permanent discovery or convert the
same user into a distinct paid job. Treat reply-aware reminders as a possible
advanced workflow to test **after** free All Accounts activation, not as a
standalone acquisition promise.

### 13. Expand SEO only from economically legible intent

Require page-level visibility into:

- eligible platform/provider visits;
- signed acquisition;
- successful setup;
- mailbox readiness;
- first value;
- retention;
- paid outcome;
- support/refund cost.

Expand one category-aligned cluster only when retained value supports it.
Spark's 70.8% concentration in a generic CC/BCC page is a reach fact, not a
Tecotype goal.

### 14. Prefer provider client choice to a managed bundle

The [next acquisition-funnel validation](../../next-acquisition-funnel.md) is
permanent email-provider client-choice placement linking to Tecotype's normal
signed build. Namecheap is the capacity/timing test; Fastmail is the
fit/acceptance control. Useful integrations do not receive a separate,
weaker acquisition status.

This applies Spark's useful provider-distribution lesson without inheriting a
bundle's updater, licensing, telemetry, and exit dependency. Before any
provider-specific work:

- obtain written permanent in-account and public placement;
- require monthly unique exposure and aggregate outbound-click reporting;
- preserve Tecotype signing, licensing, update delivery, and support;
- prohibit repackaging, a partner SDK, and user-level referral identifiers;
- keep mailbox credentials, content, metadata, and search activity out of
  Tecotype and partner attribution;
- model incremental economics against the USD 50 CAC ceiling; and
- ensure the underlying provider capability remains useful without the
  partnership.

Setapp is a no-go under the current product boundary because its Membership
build rules remove proprietary updating and licensing and its framework adds
platform-side usage/device telemetry. Reconsider only with a written exception
that preserves the normal Tecotype build and privacy boundary.

### 15. Relaunch meaningful changes, not routine noise

Spark's 12 Product Hunt launches show that important new platforms and
workflows can create repeated attention.

Tecotype can consider distinct launch moments for:

- first public Mac release;
- Windows release, once shipped;
- a materially differentiated local retrieval capability;
- a meaningful provider or migration expansion.

Each launch needs current proof and a complete downstream path. Do not relaunch
roadmap labels or routine maintenance as if they were new products.

## Avoid list

- “Smart. Focused. Email.” imitation or generic mastery/productivity claims.
- “Best,” “fastest,” or “private” without a defined comparison and evidence.
- “Your data is never shared” when providers, payments, diagnostics, or
  integrations create legitimate data flows.
- “Your mail never leaves the device.”
- AI-assistant or meeting-suite positioning; Tecotype is not a chat assistant.
- Current-value claims based on planned features.
- “Available on Mac” before a public signed/notarized build ships.
- “Available on Windows” before signed distribution and updates ship.
- A second desktop client that turns migration into product selection.
- A large download, user, rating, or organization claim without definition,
  date, source, and permission.
- A broad how-to content engine before source-to-retention measurement.
- Paid media optimized to clicks, CTA events, or downloads.
- A partner bundle without economics, support, build, ownership, and exit
  terms.
- Platform parity inferred from one store or one client.

## Recommended sequence

| Order | Test                                                                          | Earliest valid stage                      | Decision signal                                  |
| ----: | ----------------------------------------------------------------------------- | ----------------------------------------- | ------------------------------------------------ |
|     1 | Calm-control vs keyboard-flow vs local-recall vs private-intelligence message | Now                                       | Accurate recall and qualified interest           |
|     2 | Data-flow comprehension                                                       | Now                                       | Correct provider/local/diagnostic understanding  |
|     3 | Privacy-minimal source and activation taxonomy                                | Now                                       | Reviewable event contract                        |
|     4 | Category-event playbook                                                       | Now                                       | Ready response with explicit no-launch gates     |
|     5 | One high-intent Mac search brief                                              | Now                                       | Query/audience fit, no availability implication  |
|     6 | Complete Mac source-to-retention test                                         | After all Mac release gates               | Retained activation and paid outcome             |
|     7 | Reviewer outreach                                                             | After reliable Mac release                | Retained activation, review themes, support load |
|     8 | Windows availability and cohort                                               | After Windows release gates               | Windows-specific setup, retention, and payment   |
|     9 | Small paid-search test                                                        | After a measured retained cohort          | Incremental retained value after full costs      |
|    10 | SEO cluster, bundle, or relaunch program                                      | After one channel is economically legible | Incremental durable value and manageable burden  |

This sequence keeps Tecotype's north star intact: speed is expected, privacy is
structural, and calm is the experience.
