# Castellum-derived opportunities for Tecotype

Research date: **2026-07-17**

These are staged experiments, not a recommendation to copy Castellum’s public
launch. Castellum has a clear message and a visible download surface, but no
publicly evidenced acquisition source, activation, retention, or payment path.
Its first build crashed at launch, and its latest explicit Gmail note still
described a test-user gate.

Tecotype’s north star is equanimity: calm, clarity, and control. “Command your
inbox like a fortress” is memorable Castellum language; it is not Tecotype’s
voice.

## Current Tecotype boundary

Repository evidence supports an active-development product with core desktop,
Gmail, IMAP, local storage, synchronization, search, Better search, reminders,
Split Inbox, drafts, and sending implemented to varying degrees of
completeness.

It does not support a public-release claim yet.

Before public acquisition, the release gate explicitly includes:

- usable first-run and no-account states;
- a public site and coherent acquisition route;
- licensing and payment for the decided Individual price;
- the Gmail restricted-API audit or verification required by the intended
  release configuration;
- signed, notarized, updateable distribution validated on release-candidate
  bytes;
- safe sending, visible failure handling, and recovery;
- privacy-compatible source-to-activation measurement.

Remaining compose/send work includes undo/discard surfaces, failure UI,
reply-threading behavior, and scheduled-compose UI. The distribution/update
technical path is implemented, but source-tagged landing links are deferred.
These distinctions must remain visible in every experiment.

## What to adapt

Castellum offers several useful shapes:

- one named audience rather than “everyone with email”;
- a direct line from audience to mechanism;
- a screenshot and technical explanation before download;
- explicit disclosure of the separate Ollama dependency;
- no required lead form before inspecting the build;
- public release notes, versions, asset sizes, and digests;
- sample data or a no-account route before mailbox authorization;
- a provider-specific release ledger.

Tecotype can adapt the clarity and inspectability without copying the
fortress metaphor, broad AI label, or unqualified privacy/provider claims.

## What not to infer

Do not infer that Castellum’s:

- manager segment converts;
- private-AI message is the winning hook;
- 24 disk-image requests are 24 people;
- eight latest-asset requests are retained users;
- 31 provider names represent 31 verified end-to-end integrations;
- zero issues mean a reliable client;
- free early access creates demand;
- direct GitHub delivery produces source attribution;
- founder profile reach created the asset requests.

There is no public activation or retention denominator for any of those
conclusions.

## Experiment 1: message-to-conversation test now

Use research conversations, not a public build, to test whether one implemented
job earns attention.

| Field | Design |
| --- | --- |
| Audience | Mac professionals who process consequential work through Gmail or IMAP and prefer keyboard control |
| Hypothesis | A narrow, calm workflow promise will produce more repeated problem evidence than a broad “AI email client” label |
| Candidate jobs | Keyboard triage without losing context; Gmail and IMAP in one focused client; “Find mail the way you remember it” through local Better search |
| Surface | One private text or static prototype per job; clearly marked active development |
| CTA | A 20-minute research conversation or request to hear when a suitable preview exists |
| Primary metric | Qualified people who independently describe the same costly workflow |
| Continue signal | At least 5 of the first 10 qualified conversations repeat one problem, and at least 3 ask for the same next step |
| Stop or reshape | People read a privacy, provider, platform, or automation promise that the product cannot support |

Interview for the job beneath the phrase:

- What causes the person to leave their current client?
- Which mailbox/provider mix matters?
- Which repeated action makes keyboard control valuable?
- Is calm control the preference, or does it solve a costly failure?
- Does local Better search solve an observed retrieval problem?
- What would make connecting a real mailbox unacceptable?

Do not offer download access, a ship date, payment, or an “AI assistant.”
Better search can be described only according to its implemented local data
flow and current limits.

## Experiment 2: release-truth matrix now

Castellum’s homepage got ahead of the latest explicit Gmail-access state.
Tecotype should maintain a single claim ledger before writing acquisition copy.

| Claim family | Required evidence | Current public-copy rule |
| --- | --- | --- |
| Gmail | Intended OAuth configuration, required review complete, fresh-account success | Do not promise public Gmail access before the gate |
| IMAP/SMTP | Representative provider setup, sync, send, sent-copy, and error recovery | Name only verified provider/configuration boundaries |
| Local/private | Data-flow review for local storage, provider traffic, updates, attribution, and optional intelligence | Say what stays local; never say mail “never leaves the Mac” |
| Better search | Release-candidate indexing, query, model/resource, and fallback behavior | Avoid generic “AI-powered email” |
| Sending | Successful delivery plus ambiguous/permanent-failure and recovery tests | Do not promote sending until safe-send gate passes |
| Distribution | Exact binary signed, notarized, installable, updateable, and recoverable | “Implemented pipeline” is not “available download” |
| Price | License, checkout, renewal, cancellation/refund, and entitlement work | The decided price can inform research; do not sell until it works |
| Split Inbox / scheduling | Shipped UI and representative behavior | Exclude unfinished behavior from launch copy |

For every claim, record:

```text
implemented in source
→ verified in a release candidate
→ available to the intended public
→ measurable after activation
```

Those are different statuses.

## Release gate

No broad public invitation should occur until every row below has a named
owner, tested artifact, date, and pass/fail result.

| Gate | Minimum evidence |
| --- | --- |
| First run / no account | Fresh profile reaches a comprehensible useful state without a mailbox; restart preserves expected state |
| Public site | Accurate platform/provider/feature copy, privacy/data-flow pages, support route, source-tagged CTA |
| Licensing / payment | Annual and monthly entitlements, checkout, activation, renewal, cancellation/refund, outage and reinstall behavior |
| Gmail restricted API | Intended scopes and architecture pass applicable Google review/audit; non-tester authorization succeeds |
| Distribution | Release-candidate DMG is signed, notarized, quarantine-clean, installable, updateable, rollback-safe |
| Safe send | Gmail and SMTP delivery, reply threading, unknown delivery, permanent failure, retry, sent copy, undo/discard boundaries |
| Measurement | Consent/data review; source, install intent, first run, account connection, first value, return, and payment remain distinguishable |
| Support / recovery | User can diagnose account, sync, update, and send failures without founder-only intervention |

Passing the source implementation tests is necessary but not sufficient. The
gate concerns the exact bytes, public configuration, policies, and end-to-end
experience people will receive.

## Experiment 3: clean release-candidate smoke gate

Castellum’s first installed build failed because a native dependency targeted
the wrong Electron ABI. Tecotype should explicitly test the packaged artifact,
not only development builds.

| Field | Design |
| --- | --- |
| Artifact | One immutable versioned release candidate per supported Mac architecture |
| Machines | Clean supported macOS versions, including a machine/profile without developer credentials |
| Sequence | Download through public route; verify digest/signature/notarization; install under quarantine; launch; use no-account state; connect representative Gmail/IMAP; send safely; quit/relaunch; update; exercise rollback/kill switch |
| Primary metric | Every critical path passes without manual file or credential repair |
| Stop | Crash, Gatekeeper warning, broken native module, unusable no-account state, blocked OAuth, unsafe send ambiguity, or failed update/recovery |

Record the exact version, architecture, OS, route, expected result, actual
result, and evidence. Do not publish a candidate that passes only on a
developer machine.

## Experiment 4: ten-person invited activation cohort after the gate

Use a small source-tagged cohort before any launch post, review outreach, or
SEO program.

```text
invited source
→ message-specific landing page
→ signed install intent
→ first launch
→ provider connection
→ message-matched first value
→ voluntary second session
→ day-seven retained use
```

| Field | Design |
| --- | --- |
| Cohort | 10 people matching the winning audience/job from Experiment 1 |
| Sources | One explicit source code per invitation or tightly separated cohort |
| Activation | Provider sync succeeds plus the exact advertised value: e.g. three keyboard triage actions and one successful local search |
| Primary gate | At least 8 of 10 reach activation without founder rescue |
| Retention signal | At least 5 return voluntarily and repeat the matched workflow within seven days |
| Safety guardrail | Zero severe send, data-loss, credential, authorization, installer, or update incident |
| Stop | Routine manual rescue, unclear privacy consent, provider mismatch, or activation only with coaching |

Ten people are enough for a readiness diagnostic, not a market-size or
conversion-rate claim. Report every denominator and reason for exclusion.

## Experiment 5: one founder-led source after invited readiness

Castellum’s maker has a credible public background but no observed
product-specific launch path. Tecotype should turn founder credibility into a
measurable source, not a reach claim.

| Field | Design |
| --- | --- |
| Hypothesis | A precise account of one Mac-email problem and its implemented mechanism will attract more qualified activations than a generic product announcement |
| Channel | One audience where the founder already participates authentically |
| Content | Problem, why existing behavior fails, what Tecotype does, local/provider data flow, current limits, who should not install |
| CTA | Source-tagged landing route to the signed release |
| Primary metric | Message-matched activations per qualified visit |
| Secondary | Provider connection, day-one/day-seven use, support and safety events |
| Stop | Discussion becomes repetitive promotion, claims drift, or product failures make continued exposure unsafe |

Do not coordinate undisclosed votes, endorsements, testimonials, or planted
comments. A founder’s followers are not a funnel until the source-to-value path
is observed.

## Experiment 6: one problem page after retained use

Castellum’s one-page site has almost no qualified search visibility and a
severe name collision. Tecotype should not respond with a large speculative
content program.

Choose one intent only after interviews and cohort behavior agree, for example:

- `keyboard first email client mac`;
- `gmail and imap email client mac`;
- `local email search mac`;
- `find old email by meaning mac`.

| Field | Design |
| --- | --- |
| Page | One audience, one problem, one demonstrated shipped workflow, one CTA |
| Prerequisite | At least five invited users have activated and repeated that workflow |
| Search basics | Canonical URL, accurate title/description, sitemap/robots, useful structured data where valid |
| Primary metric | Activated and day-seven retained users from qualified non-brand visits |
| Continue signal | Relevant queries plus at least five matched activations before expanding |
| Stop or revise | Wrong intent, unsupported platform/provider demand, or no matched activation after a meaningful sample |

Do not publish dozens of provider or comparison pages until each claim has
release evidence. Indexability is not demand, and modeled traffic is not use.

## Experiment 7: early-access and paid transition

Castellum is free now and leaves future price and transition open. Tecotype has
a decided Individual price of **€149/year or €15/month**, but licensing and
payment flows are not yet a public product.

Test commercial framing only after the payment gate passes:

| Field | Design |
| --- | --- |
| Disclosure | Show both prices, billing period, trial/preview terms, card requirement, cancellation/refund, entitlement, and what happens at expiry before download |
| Cohort | People who already reached meaningful activation |
| Primary metric | Paid conversion among activated users |
| Guardrails | Activation, day-seven retention, refund, complaint, support, send safety, and uninstall |
| Continue signal | Paid conversion without material activation/retention harm or surprise |
| Stop | Pricing changes access unexpectedly, setup time consumes a trial, or licensing failure threatens local mail confidence |

Do not manufacture urgency, call a preview permanently free, or change an
existing cohort’s entitlement with short notice. An installed email client
holds unusually sensitive state and deserves predictable terms.

## Minimal measurement contract

Castellum’s public evidence collapses at asset requests. Tecotype should keep
these stages separate:

| Event | Meaning | Must not be called |
| --- | --- | --- |
| Qualified landing view | Intended person saw the message | User |
| Install-route redirect | Browser requested the stable download route | Completed download or install |
| First launch | Packaged client opened | Activated |
| Provider connected | Intended mailbox authorization/setup succeeded | Retained |
| Message-matched first value | User completed the workflow promised by that source | General product success |
| Voluntary return | A later real session repeats useful behavior | Day-seven retention unless timing qualifies |
| Paid entitlement | Payment and license both succeeded | Revenue retained |

The implemented distribution analytics deliberately avoid install IDs and use
an IP-derived network key. Preserve that privacy posture. A future
source-to-activation design should:

- collect only the source and stage needed for the decision;
- avoid message content, subject, recipient, search query, or mailbox identity;
- document how IP-derived counts merge or split people;
- separate manual testing and release verification;
- let people understand any client measurement;
- expire unnecessary raw attribution;
- report counts with definitions and denominators.

## Recommended sequence

```text
message conversations now
→ release-truth matrix
→ complete explicit release gate
→ packaged clean-machine smoke test
→ 10-person source-tagged cohort
→ retained-workflow evidence
→ one founder source
→ one problem/search page
→ commercial test among activated users
```

The highest-value Castellum lesson is not to move faster into public
distribution. It is to preserve a specific message while making every
downstream transition honest, observable, and calm.
