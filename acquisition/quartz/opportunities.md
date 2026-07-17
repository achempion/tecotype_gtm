# Tecotype experiments

Quartz supports one acquisition hypothesis worth testing and one strong funnel
warning:

- A concentrated launch may create real product trials when the public page,
  download, onboarding, proof, and maker participation arrive together.
- Low web friction can simply move abandonment into installation, OAuth, sync,
  and a large model download.

Quartz does not publish the conversion evidence needed to validate that
hypothesis. Product Hunt points, directory links, and Quartz's first-party
daily-use claim do not provide a conversion benchmark. Suggested thresholds
below are planning defaults for deciding whether to continue, not facts learned
from Quartz.

## Tecotype reality gate

The current public-version source was checked at tag `v0.5.1`.

Tecotype can substantiate:

- Apple Silicon Mac distribution.
- Gmail OAuth and generic IMAP plus SMTP.
- A local working copy and local full-text search.
- Optional on-device Better search with a stated one-time 318 MB model
  download.
- Keyboard navigation and triage.
- Split Inboxes and reminders.
- Local draft autosave and new-message sending or scheduling through Gmail or
  SMTP.

Tecotype should not currently market:

- usable first-run/no-account onboarding;
- licensing, checkout, trial, or a permanent free plan;
- functional reply sending or reply threading;
- outbound attachments;
- an encrypted mailbox, end-to-end encrypted mail, or “mail never leaves your
  device”;
- Intel Mac, Windows, broad platform availability, or first-class Outlook /
  Fastmail OAuth.

The signed distribution and [minimal update
analytics](../../../tecotype/architecture/distribution-updates-analytics.md)
are live. They use no persistent install ID, but the edge derives an
HMAC-derived network key from the client IP and retains it with country,
data-center location (`colo`), and coarse client metadata for three months.
The worker can record UTM
values on a tagged download redirect; it cannot currently join that redirect
to first launch or a product activation event.

The public website, usable first run, license gate, and Gmail restricted-API
audit remain release work in the [current source
status](../../../tecotype/architecture/README.md). Pricing is decided at
[€149 per year or €15 per month](../../pricing.md), but payment and trial
mechanics are not.

## Experiment 1: product-proof and message research now

| Field | Design |
| --- | --- |
| Audience | Email-heavy Apple Silicon Mac users who use Gmail or an IMAP provider and value keyboard operation, retrieval, privacy, or inbox control |
| Hypothesis | A concrete 30–60 second proof earns more qualified research conversations than an abstract “calm email” description |
| Proof variants | Keyboard triage; `“train ticket to copenhagen” finds “Din togbillet til København”`; Gmail plus IMAP; custom Split Inbox |
| Honest CTA | “Help us understand this workflow” or “Ask to be notified when the public first run is ready” |
| Primary metric | Qualified conversations in which the person has the demonstrated problem and a supported setup |
| Continue signal | At least 5 qualified conversations from the first 10 substantive placements, with one proof repeatedly earning interest |
| Stop or reshape | Fewer than 3 qualified conversations, unsupported-provider demand dominates, or people understand the proof but have no switching reason |
| Claim boundary | Do not offer public access, reply automation, a trial, or checkout |

Test the demonstration and lead message separately:

- Calm control over your mail.
- Move through mail from the keyboard.
- Find mail the way you remember it.
- Keep search on your device.

Quartz's headline change does not tell us which message wins. Tecotype must
measure the audience, trigger, proof, and requested action.

## Experiment 2: activation-readiness gate

This is not an acquisition channel. It prevents a public launch from amplifying
an unusable first run.

| Field | Design |
| --- | --- |
| Audience | Ten representative Apple Silicon Mac users across Gmail and generic IMAP |
| Hypothesis | A newly interested person can install, connect a supported account, sync, and experience core value without founder rescue |
| Prerequisite | Guided no-account state, safe account connection, clear sync state, a chosen activation event, and a documented observation plan for the pilot |
| Candidate activation | First sync completes, then the user performs at least three keyboard triage actions and one local search in the same or next session |
| Retained-use check | A core mail action on a separate day within the first seven days |
| Readiness signal | At least 8 of 10 reach activation without founder intervention and without a severe data, sync, or sending issue |
| Stop or reshape | Repeated manual rescue, unclear provider permissions, surprise setup costs, or the demonstrated workflow cannot be completed |

Better search must remain optional. State “One-time 318 MB download” before the
choice and preserve the shipped pressure-free path to continue later.

## Experiment 3: coordinated launch after the gate

Before a source-level launch experiment, Tecotype must design and ship a
privacy-reviewed source handoff plus the minimum app events needed to observe
activation. The current telemetry cannot link a UTM-tagged redirect to app
activity. Specify the handoff's lifetime, deletion point, and aggregation
rules; do not introduce a persistent install identity merely to make the join.

```text
Maker proof or launch post
→ source-specific landing visit
→ direct Apple Silicon download
→ first app launch
→ account connection
→ chosen activation event
→ retained use
→ trial/payment only when implemented
```

| Field | Design |
| --- | --- |
| Hypothesis | A focused launch package will produce activated, retained users, not only votes and downloads |
| Package | Accurate page, one short demonstration, platform/provider facts, setup facts, pricing status, maker availability, and release notes |
| Instrumentation prerequisite | A shipped, privacy-reviewed handoff from tagged download to first launch, plus minimal activation and retained-use events |
| Source separation | After that prerequisite, Product Hunt, each maker account, newsletters, directories, and direct traffic receive distinct short-lived source values |
| Primary metric | Activated users per qualified landing visit |
| Secondary metrics | Download intent, first launch, account connection, activation latency, seven-day retained use |
| Continue signal | At least 20 activated users from the source and an activation rate not materially below the direct/owned baseline |
| Stop or diagnose | 100 qualified downloads produce fewer than 10 activations, onboarding abandonment concentrates at one stage, or seven-day use collapses |
| Claim boundary | If replies remain incomplete, the launch proof and activation event must not depend on sending a reply |

The exact thresholds should be revised after the pilot establishes a baseline.
Do not combine Product Hunt and maker traffic into one “launch” cohort.

## Experiment 4: founder-led prelaunch narrative

Quartz used LinkedIn, Indie Hackers/HackerNoon, and product updates to frame the
problem before launch. Visible engagement outside LinkedIn was small, so this is
a low-cost learning test rather than a proven growth engine.

| Field | Design |
| --- | --- |
| Cadence | Four to six concrete posts over four weeks |
| Topics | Keyboard architecture, approximate-memory search, Gmail plus IMAP, honest local-processing boundary, and one onboarding improvement |
| CTA | Research conversation or accurately scoped pilot notification |
| Primary metric | Qualified conversations and supported-setup pilot requests |
| Continue signal | One repeated audience/problem pattern across at least five people |
| Stop signal | Content attracts builders but no prospective users, or requires hype and unsupported claims to earn attention |

Each post should demonstrate one shipped behavior. Avoid unverified time-saved
claims and do not dramatize inbox anxiety.

## Experiment 5: small newsletter and directory batch

Quartz appeared on BetaList, Fazier, newsletters, launch trackers, and many AI
directories. Only placement is proven.

| Field | Design |
| --- | --- |
| Prerequisite | Public page, usable onboarding, and the privacy-reviewed attribution and activation instrumentation defined above |
| Batch | At most ten relevant sources: Mac utilities, privacy/local software, keyboard workflows, email clients, and carefully selected launch directories |
| Exclusion | Generic AI directories whose audience expects cloud assistants or automation Tecotype does not offer |
| Primary metric | Activated users per placement |
| Secondary metric | Qualified visits; backlink count is diagnostic only |
| Continue signal | A source produces at least one activated and later retained user at acceptable effort |
| Stop signal | Ten placements produce no activated user or mostly unsupported-platform traffic |

Use source tags added by Tecotype, not only parameters controlled by the
directory. If the instrumentation prerequisite is met, retain only the source
context needed for the experiment, delete or aggregate it at the documented
point, and avoid a browsing history or persistent install identity.

## Experiment 6: one descriptive search surface

Quartz captures exact brand/product queries but has no category program. A
single Tecotype page should first test whether precise category demand exists.

Candidate pages:

- Keyboard-first email client for Mac.
- Gmail and IMAP desktop email client.
- Find mail from an approximate or cross-language memory.
- On-device email search with a precise privacy boundary.

Before building:

1. Inspect the live result set and intent.
2. Confirm every phrase against the current release.
3. Use one demonstration, one CTA, and one activation path.
4. Keep category, platform, providers, and availability explicit in the title,
   description, heading, and page copy.

Continue only when impressions lead to qualified visits and activated users.
Do not build a broad content factory from Quartz's three ambiguous rankings.

## What not to copy

- Launch votes, followers, installer downloads, or backlinks as the success
  metric.
- A public launch before the no-account path works.
- A small direct-download installer whose page leaves the multi-gigabyte
  onboarding download undisclosed.
- “End-to-end encrypted,” “no servers,” or “email never leaves the device”
  when the narrower technical facts are different.
- An AI-first category merely because AI directories are easy to enter.
- Mandatory identified telemetry without clear acquisition-stage disclosure
  and a deliberate Tecotype privacy decision.
- A stale iOS or platform promise.
- Free-beta traction as evidence for Tecotype's paid price.
- Product demonstrations of reply sending until reply behavior is genuinely
  shipped.

## Measurement sequence

Now:

```text
Concrete proof
→ qualified research conversation
→ supported setup
→ repeated audience/problem/message signal
```

After the release gate and the attribution/activation instrumentation:

```text
Attributed visit
→ download intent
→ first launch
→ account connection
→ first sync
→ chosen activation event
→ retained use
→ trial and payment only when implemented
```

Keep measurement data-minimal and collect only the product events needed to
answer the experiment. Existing distribution analytics have no persistent
install ID, but they do use an IP-derived network key plus country and colo
with three-month retention. Any new source handoff or product event needs an
equally explicit purpose, lifetime, and deletion boundary. Calm and privacy
should remain structural in the measurement design, not only marketing copy.
