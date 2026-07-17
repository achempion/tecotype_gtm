# Locker opportunities for Tecotype

Research date: **2026-07-17**

Locker offers a useful early-stage contrast:

- A direct, concrete local-privacy promise.
- A public download before payment.
- Five free keys shown as claimed.
- A live one-time checkout handoff; transaction completion was not tested.
- Very small community and search signals.
- No public activation, retention, or paid-conversion evidence.
- A material mismatch between homepage capabilities and the latest release.

Tecotype should adapt the clarity of the product demonstration and the
separation of funnel events. It should not adapt the scarcity, unqualified
privacy language, or release ambiguity.

## Current Tecotype boundary

Tecotype's project documents describe an active product, not a launch-ready
public funnel.

Before a public download or payment experiment, the project still needs a
coherent set of release prerequisites, including:

- First-run and no-account onboarding.
- A public website.
- Signed, notarized, updateable distribution whose install and update paths
  have been verified.
- Licensing and payment.
- Gmail restricted API audit readiness.
- Safe, predictable compose, reply, and send behavior.
- A chosen activation event and privacy-compatible source-to-activation
  measurement.

Current signed-release tooling targets Apple Silicon; this does not establish
a distributable signed build. The broader release is Mac-first. Future MCP
and agent-driven automation must not be presented as current. Split Inbox
expansion and other post-release work must also remain outside any claim
unless the release being tested actually contains it.

This means Tecotype can run audience and message research now. It should not
copy Locker's public download-and-buy path yet.

## Decision summary

### Adapt

- One product proof per message.
- A direct view of the actual app.
- Download-before-purchase as a future hypothesis.
- Public, versioned release notes.
- Separate measurement for download, install, first value, return, and
  purchase.
- A pressure-free way to contact the maker or join research.

### Do not adapt

- Countdown-like limited lifetime inventory.
- Free-key claims as social proof.
- Asset-download counts as users.
- A long assistant-feature catalogue before those capabilities ship.
- “Nothing leaves your device” or “no cloud” without naming provider and
  update/license connections.
- A no-refund policy before Tecotype decides its own trial and refund model.
- Broad AI-assistant positioning.

## Experiment 1: message-to-conversation research

### Timing

Now, before public launch.

### Question

Which concrete Tecotype job earns a qualified conversation with an
email-heavy Mac professional?

### Audience

Recruit a small number of:

- Keyboard-oriented developers and operators.
- Consultants or specialists handling confidential correspondence.
- People using both Gmail and another IMAP provider.
- People who recently failed to recover a remembered message.

Recruit through communities only where disclosed product research is allowed.
Use original copy for each community and do not duplicate the same promotional
post across many groups.

### Message cells

#### A: remembered search

```text
Find mail the way you remember it

"train ticket to copenhagen" finds "Din togbillet til København"
```

#### B: keyboard handling

```text
Move through mail from the keyboard

Frequent actions stay direct. Less frequent ones remain discoverable.
```

#### C: calm local-first control

```text
One focused Mac client for Gmail and IMAP

Local search, a restrained interface, and no cloud AI service added to your
mailbox.
```

The third cell must not say mail never leaves the device. Mail still travels
through the user's provider.

### CTA

Ask for a research conversation or permission to notify them later. Do not
promise immediate public access.

### Record

- Community and exact message.
- Qualified responses.
- Completed research conversations.
- Current client and provider mix.
- Triggering problem.
- Existing workaround.
- Whether the person asks to try the product without being prompted.

### Decision rule

Advance a message only when it:

- Produces at least five qualified conversations.
- Names a recurring job rather than general AI interest.
- Attracts people whose current workflow Tecotype can support.
- Survives direct questions about switching friction and trust.

Do not compare raw upvotes across communities with different sizes and rules.

## Experiment 2: release-truth proof page

### Timing

After the public site exists, before broad distribution.

### Question

Does a single release-accurate product demonstration create more qualified
intent than a broad feature list?

### Variant A

Lead with a short real keyboard-triage recording from the release.

### Variant B

Lead with the canonical Better search example from the release.

### Shared page contract

Show:

- Platform and architecture supported by that build.
- Gmail and IMAP support as it actually works.
- Download size and system requirements.
- Exact evaluation and price terms once decided.
- A short `Available now` list.
- A separate `In development` link rather than blending future work into the
  sales page.

### Primary metric

Qualified install start per relevant visitor.

### Guardrails

- No mock UI presented as a shipped screen.
- No unverified time-saved claim.
- No feature whose current release path has not been walked.
- No pressure counter.

This directly tests the inverse of Locker's homepage/changelog mismatch.

## Experiment 3: invited try-before-buy cohort

### Timing

Only after:

- A signed and notarized release is distributable, and its install and update
  paths have been verified.
- First run works without an existing account.
- Source tags survive through the handoff.
- License and payment behavior work.
- Gmail restricted API audit requirements are satisfied.
- Compose, reply, and send behavior pass the release's safety gates.
- The evaluation, refund, and privacy terms are decided.
- The team can distinguish install from retained activation.

### Question

Does trying Tecotype before purchase overcome primary-inbox switching friction
without attracting only free users?

### Cohort

Start with 20–30 qualified participants from Experiment 1. Do not open broad
distribution until the cohort reaches first value and can return voluntarily.

### Funnel

```text
source-tagged invitation
→ page proof
→ signed and notarized download
→ successful first run
→ account connected
→ first sync usable
→ message-matched first-value action
→ voluntary next-day return
→ day-seven use
→ paid conversion
```

### Message-matched activation

For the Better search message:

```text
Find one known message using an approximate or cross-language memory.
```

For the keyboard message:

```text
Complete a real triage sequence without needing the mouse for frequent
actions.
```

Do not combine those into one generic “account connected” activation event.

### Minimal measurement

Record:

- Source and message cell.
- Download requested.
- First run completed.
- Account connection completed.
- First sync usable.
- First-value event completed.
- Voluntary next-day return.
- Day-seven use.
- Purchase.

Do not record query text, message content, sender identity, or subject lines.
State the measurement plainly.

### Decision rule

Expand only if:

- A clear majority of connected users reach the message-matched first value.
- Return is voluntary rather than forced by a redirect or reminder trick.
- Day-seven use is not concentrated in internal testers.
- At least some qualified participants choose the decided paid offer.
- Support failures are understood and fixable.

Exact numeric thresholds should be set before invitations based on the final
event definitions and cohort size.

## Experiment 4: exact job search page

### Timing

After the release gate and first retained cohort.

### Question

Can one purchase-adjacent job page attract more qualified traffic than broad
“AI email client” positioning?

### Candidate pages

- `search-email-by-meaning`
- `keyboard-first-email-client-for-mac`
- `gmail-and-imap-client-for-mac`

Choose one first. Each page must use real product proof and link to the same
source-attributed evaluation path.

### Why

Locker was absent from two category SERPs despite a highly optimized local-AI
homepage. Its exact brand query was also diluted by unrelated “Locker”
products. Tecotype should target a concrete job that does not depend on prior
brand awareness.

### Success

Measure:

- Relevant search visits.
- Install start.
- Account connection.
- Message-matched first value.
- Day-seven use.
- Purchase.

Ranking without downstream use is not success.

## Pricing and paid acquisition

Locker provides no evidence that an inexpensive lifetime offer converts. If
its visible inventory counter is accurate and complete, it is consistent with
no $39.99 founder sale. Separately, the homepage displays all five free keys
as claimed, without exposing their source, activation, or use.

Tecotype already has a different pricing decision:

```text
€149 per year
or €15 per month
```

Do not use Locker to reopen that decision. Use the cohort to learn whether the
combined calm, keyboard, provider, search, and organization experience earns
the chosen price.

Do not buy traffic until retained conversion is measured. Tecotype's current
gross break-even visitor range is €0.149–€0.50 before VAT, payment fees,
refunds, support, and other costs. Sustainable spend must be lower.

## Instrumentation contract

Every release experiment should preserve:

```text
source
→ message
→ page
→ release version
→ download
→ first run
→ provider connection
→ message-matched first value
→ voluntary return
→ purchase
```

Keep event names and definitions versioned. A change to first run, provider
support, or Better search can otherwise make cohort comparisons misleading.

## Final recommendation

Use Locker as a warning and a useful prototype:

- The concrete local-search example is strong.
- The direct download and separate payment path are testable.
- The visible early signals are too small to prove acquisition.
- The broad feature page exceeds the public release boundary.

Tecotype's advantage should be a calmer and more trustworthy contract:

> Show one real job, state the release facts, let a qualified person try it,
> and measure whether they return and pay.
