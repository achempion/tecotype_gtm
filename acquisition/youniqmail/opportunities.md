# YouniqMail opportunities for Tecotype

Research date: **2026-07-17**

YouniqMail demonstrates four useful early-stage patterns:

- A concrete local-provider architecture can earn privacy interest.
- Community posts can rank for category language long after posting.
- Consistent educational content can create discoverability.
- A public feedback loop can surface self-reported use without exposing private
  analytics.

It also exposes four cautions:

- Broad informational rankings may not lead to product intent.
- Repeating launch copy across communities produces very different results and
  removals.
- A privacy-led email gate can feel self-contradictory.
- Download clicks and issue threads still stop short of cohort retention and
  payment.

Tecotype should adapt the evidence discipline, not the feature breadth or
distribution volume.

## Current Tecotype boundary

Tecotype is under active development. Project documents do not establish a
launch-ready public funnel.

Before a public download or payment experiment, the project still needs a
coherent release path including:

- Public website.
- First-run and no-account onboarding.
- Signed, notarized, updateable distribution for the release target.
- Licensing and payment.
- Completion of the Gmail restricted-API audit path.
- A clear evaluation and refund policy.
- Safe, predictable compose, reply, and sending behavior.
- A privacy-compatible activation definition and measurement plan.

The release is Mac-first and current signed-release tooling targets Apple
Silicon; that target does not establish that a distributable signed build
exists. Future MCP and agent automation must not be marketed as current. Split
Inbox is post-release work. Better Search is implemented in the product code,
but any public resource, performance, or compatibility claim must be verified
against the actual distributable build.

Mail still travels through the user's provider. Tecotype must not say that
email never leaves the device.

This boundary allows customer and message research now. It does not authorize
a public download, checkout, or claim that future features are available.

## Decision summary

### Adapt

- One exact job per message.
- Founder explanation grounded in a real product constraint.
- Community-native discussion rather than generic launch copy.
- A release-dated proof and public changelog.
- Optional, voluntary feedback that separates download, current use, and
  discontinuation.
- Source attribution that survives the artifact handoff.
- Separate install, connection, first-value, return, and payment events.

### Do not adapt

- An email address as the price of trying a privacy-led product.
- The same promotional post across many communities.
- CC/BCC-style commodity content without a direct product job.
- Pixel configuration as evidence that paid acquisition works.
- Platform-button clicks as installs.
- Forum accounts or issue volume as an active-user count.
- “Zero tracking” without separating the product, website, and voluntary
  measurement.
- A long feature catalogue containing post-release or future work.

## Experiment 1: job-to-conversation research

### Timing

Now, before public launch.

### Question

Which Tecotype job earns a qualified conversation with an email-heavy Mac
professional?

### Audience

Recruit a small number of:

- Keyboard-oriented developers, founders, and operators.
- Consultants or specialists handling sensitive correspondence.
- People using Gmail or standard IMAP on a Mac.
- People who recently struggled to find a remembered message.
- People who tried a new email client and returned to their old one.

Use communities only where disclosed product research is allowed. Write an
original post for each context; do not cross-post identical launch copy.

### Message cells

#### A: remembered search

```text
How do you look for an email when you remember the situation, but not the
sender or exact words?

We are researching a Mac email client that makes those remembered clues useful.
```

#### B: keyboard handling

```text
Which email actions still force you from the keyboard to the mouse?

We are researching a calm Mac workflow where frequent actions stay direct and
less frequent ones remain discoverable.
```

#### C: switching friction

```text
What made you abandon the last email client you tried?

We are researching the first week of switching, especially account setup,
trust, sending, and the moment people return to their old inbox.
```

These are research prompts, not release claims.

### CTA

Ask for a 20-minute research conversation or permission to contact the person
for later research. Do not require newsletter consent and do not promise
immediate beta access.

### Record

- Community and exact prompt.
- Qualified replies.
- Completed conversations.
- Current client and provider.
- Triggering job.
- Existing workaround.
- Previous switch attempt and reason for returning.
- Whether the person asks to test Tecotype without being prompted.

Do not record message content, sender identity, subject lines, or search
phrases from a real mailbox.

### Decision rule

Advance a job only when it:

- Produces at least five qualified conversations.
- Recurs across more than one participant.
- Fits the providers and platform Tecotype can support.
- Has a clear first-value action.
- Survives direct trust and switching-friction questions.

Votes and comments are context, not the decision metric.

## Experiment 2: release-truth proof page

### Timing

After the public site exists and the candidate release can be captured, before
broad distribution.

### Question

Does one release-accurate demonstration create more qualified intent than a
broad privacy or feature statement?

### Variant A: Better Search proof

Show one real example from the distributable build:

```text
Find a known message from approximate or cross-language remembered clues.
```

The example must use synthetic mail and must not promise resource use, speed,
or accuracy that has not been measured on the release artifact.

### Variant B: keyboard proof

Show one real sequence from the distributable build:

```text
Open, move through, and act on a small inbox sequence using the release's
actual keyboard controls.
```

### Shared page contract

Show:

- Apple Silicon and minimum macOS version.
- Supported Gmail/IMAP setup as it actually works.
- Direct-provider and local-processing boundaries.
- What the website measures and what the app does not send.
- Exact available-now features.
- Separate “In development” material.
- Download size and signing/notarization state.
- Evaluation and price terms once finalized.

Do not blend future MCP, agent automation, Split Inbox, or unverified
capabilities into the page.

### Primary metric

Qualified invitation request per relevant visitor.

Before a public artifact exists, the CTA remains research contact or
invitation interest, not `Download`.

### Guardrails

- No mock interface presented as a shipped screen.
- No time-saved claim.
- No “nothing leaves your device.”
- No customer count inferred from invitations.
- No blocking newsletter requirement.
- Optional analytics off until consent, with a page that still works without
  them.

### Decision rule

Choose a proof only if:

- The message attracts people with the matching job.
- Participants can explain the value without repeating marketing language.
- Trust questions have precise, consistent answers.
- The candidate release can perform the demonstrated action reliably.

## Experiment 3: source-preserving invited cohort

### Timing

Only after:

- The signed and notarized build and its update path are distributable and
  tested.
- First run works from a clean supported Mac.
- Account setup and first sync are reliable.
- Sending behavior is release-ready.
- Licensing and payment work.
- Evaluation, privacy, and refund terms are decided.
- Source tags survive the website-to-artifact handoff.

### Question

Can a message-matched cohort reach first value and return voluntarily?

### Cohort

Invite 20–30 qualified participants from Experiment 1. Use one source and
message cell at a time.

### Funnel

```text
source-tagged invitation
→ release-truth proof
→ signed artifact
→ successful first run
→ account connected
→ first sync usable
→ message-matched first value
→ voluntary next-day return
→ day-seven use
→ paid conversion
```

### Message-matched activation

For Better Search:

```text
Find one known message using an approximate remembered clue.
```

For keyboard handling:

```text
Complete one real triage sequence using the release's intended frequent
controls.
```

Account connection alone is not activation.

### Minimal measurement

Record:

- Source and message cell.
- Artifact requested.
- First run completed.
- Account connection completed.
- First sync became usable.
- First-value event completed.
- Voluntary next-day return.
- Day-seven use.
- Purchase.

Use coarse event names and pseudonymous cohort identifiers. Do not collect
queries, message content, sender, recipient, or subject.

### Decision rule

Expand only if:

- A clear majority of connected participants reach the matching first value.
- Return is voluntary.
- Day-seven use is not concentrated in internal testers.
- Failures are understood and fixable.
- At least some qualified participants accept the finalized paid offer.

Set exact numeric thresholds before invitations, based on the final event
definitions and cohort size.

## Experiment 4: product-intent search/community bridge

### Timing

After one invited cohort shows retained use.

### Question

Can one narrowly useful page or community contribution attract people whose
search intent matches an in-product first-value action?

### Candidate topics

Use research language, not generic high-volume definitions:

- `find email when you don't remember exact words`
- `search email in another language`
- `keyboard first email workflow on mac`
- `local search for gmail and imap on mac`

Validate current wording and difficulty before publishing. Do not assume these
exact phrases have traffic.

### Page structure

```text
exact problem
→ honest explanation
→ real release demonstration
→ architecture and provider boundary
→ source-tagged invitation or download
→ matching first-value event
```

Community contributions should answer the problem fully in the community. The
link should be optional supporting detail, not the entire answer.

### Metrics

- Qualified visits.
- Invitation or artifact request.
- Account connection.
- Matching first value.
- Next-day and day-seven use.
- Purchase.

Pageviews, rank, and votes remain diagnostics.

### Stop rule

Stop or rewrite when a topic:

- Produces informational traffic without qualified activation.
- Attracts unsupported providers or platforms.
- Requires exaggerated privacy language.
- Ranks through a founder post but produces no connected or returning users.

This applies YouniqMail's strongest SEO lesson: visibility can be real while
the product bridge remains weak.

## Experiment 5: voluntary feedback loop

### Timing

Alongside the invited cohort.

### Question

Can Tecotype learn why people stop without adding silent mailbox telemetry?

### Survey

Ask, optionally:

- Did first run complete?
- Did an account connect?
- Was first sync usable?
- Did the person complete the message-matched first-value action?
- Are they still using Tecotype?
- How often?
- If not, what stopped them?
- May the team contact them?

Avoid asking for real query text, subjects, senders, recipients, screenshots of
private mail, or exported logs by default.

### Interpretation

Keep these separate:

```text
artifact request ≠ install
install ≠ connection
connection ≠ first value
first value ≠ retention
survey response ≠ representative cohort
stated willingness ≠ payment
```

## Instrumentation contract

YouniqMail's public configuration shows why the measurement contract should be
designed before distribution.

Tecotype should decide:

- Which website events are essential.
- Which optional analytics require consent.
- How a source identifier reaches the artifact handoff.
- How install/activation is measured without mailbox data.
- How long cohort identifiers live.
- What is never collected.
- How a participant opts out.

Publish this in plain language before inviting a release cohort.

## Pricing and paid acquisition

Tecotype's current project documents describe €149/year as the primary price
and €15/month as an alternative. The public website, licensing, payment,
evaluation, and refund path are not yet complete, so those terms must not be
presented as a live offer until the release gate and policies are satisfied.

Do not buy ads to compensate for an unproven first week. YouniqMail has
configured marketing pixels but no returned Google paid-search evidence, and
its public founder account says privacy does not automatically create
switching or payment.

Paid acquisition should wait until:

- Message-matched first value is reliable.
- Voluntary return is visible.
- Payment works.
- Source-to-retention attribution works.
- Support load is understood.

## Final recommendation

The next Tecotype action is not a broad beta or a content program. It is a
small set of job-to-conversation interviews, followed by one release-accurate
proof when the distributable build and public path are ready.

YouniqMail's useful advantage is visible activity across search, community,
release notes, and feedback. Tecotype can make that evidence chain stronger by
connecting one source and one promise all the way to retained first value.
