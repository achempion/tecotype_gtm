# Canary Mail lessons and staged opportunities for Tecotype

Research date: **2026-07-17**

This document translates Canary’s public evidence into tests for Tecotype. It does not recommend copying a channel merely because Canary uses it.

## Product-truth boundary

Tecotype is under active development. The repository documents a Mac-first product and tooling for a signed/notarized Apple Silicon release target, but it does **not** establish that a public macOS release has shipped. Any local builds are testing-only. Public website, onboarding, licensing/payment, Gmail restricted-API audit, safe compose/sending polish, updates, installers, and distribution remain release gates.

Windows distribution is planned: signed NSIS, Store acquisition, a direct fallback, and updates. It is not a shipped public capability and must not be described as available.

Current defensible product claims are narrower:

- keyboard-first desktop email client;
- Gmail and generic IMAP support;
- local storage and search;
- optional local Better search;
- Split Inboxes, reminders, drafts, and sending, with completeness and release status verified before publication;
- Mac-first release direction.

Tecotype Individual is decided at **€149/year or €15/month**, with annual as the primary offer. Those are actual billing cadences, not annualized monthly equivalents.

## What Canary demonstrates

| Canary signal | Defensible lesson | Missing evidence |
| --- | --- | --- |
| 3,115 organic keywords and 217 relevant pages | A large owned content system can create discovery beyond the homepage | Qualified installs, activation, retention, and paid conversion |
| Homepage only 4.9% of modeled ETV | Distributed entry pages reduce dependence on one product page | Whether broad problem intent is commercially efficient |
| Four current store surfaces | Stores create durable platform proof and branded-result coverage | Active installs and quality parity |
| Free plus no-card trial | Low billing anxiety can reduce evaluation friction | Support cost, abuse, conversion, and revenue |
| Explicit GA/app-attribution components | Cross-surface measurement is operationally possible | Event quality, consent, and actual rates |
| Privacy plus security pages | Data handling and audit framing can support consideration | Publicly reviewable audit and simple claim consistency |
| Setapp history and 2026 exit | Bundles can produce discovery and customer transition risk | Channel economics |
| 1M+ users and logo row | Large proof is visually persuasive | Definition, permission, source, activity, and payment |

## Priority 1: pre-release research

These tests do not require public availability.

### 1. Validate a singular promise

Compare three accurate concepts with the same audience and screenshot:

1. **Calm control:** a focused place to handle email without urgency mechanics.
2. **Keyboard flow:** move through Gmail and IMAP work without leaving the keyboard.
3. **Local recall:** find mail through local search and optional local Better search.

Method:

- moderated interviews and message comprehension;
- static page or concept tests clearly labeled as research or in development;
- no Download or Start Trial CTA;
- ask participants to restate what the product does, who it is for, and what data handling they infer.

Decision:

- choose the concept with the clearest accurate recall and strongest qualified follow-up intent;
- do not optimize for generic click-through on a product that is not publicly available.

Why Canary matters: its current page accumulates AI, calendar, security, teams, and power features. Tecotype can be more memorable by making one emotional and workflow outcome dominant.

### 2. Publish-ready data-flow proof

Draft one plain-language matrix before launch:

| Capability | Runs where | Data involved | Provider/service | Optional? |
| --- | --- | --- | --- | --- |
| Gmail/IMAP sync | Verify against release | Mail and credentials | User’s provider | Required for connected account |
| Local search | Device | Local working copy | None beyond provider sync | Core |
| Better search | Device | Local indexed content | Verify model/runtime | Optional |
| Diagnostics/measurement | Define minimum | Event and failure metadata | Define before release | Consent/controls must be explicit |

Test whether participants can correctly answer:

- Does mail still travel through their provider?
- Which search runs locally?
- Is Better search optional?
- What product data, if any, is sent for diagnostics?

Why Canary matters: “not used for model training” and “on-device” are different claims. Tecotype should never force readers to discover that distinction deep in a policy.

### 3. Define source-to-value measurement

Establish a privacy-minimal vocabulary now:

- `source`
- `medium`
- `campaign`
- `content`
- intended platform
- provider family
- successful authorization
- mailbox-ready state
- first meaningful keyboard/local-search action
- retained meaningful use
- billing outcome

Do not implement cross-site surveillance or retain content-bearing event payloads. Define deletion, consent, aggregation, and access rules before collection.

Why Canary matters: it exposes download events, UTMs, web analytics, app analytics, and mobile attribution, but the public record cannot connect them. Tecotype should make activation—not CTA clicks—the measurement center.

### 4. Choose the first search wedge

Create briefs, not a broad publishing engine, for a small set of high-intent pages:

- keyboard-first email client for Mac;
- Gmail and IMAP desktop client for Mac;
- local email search on Mac;
- focused email client for people who work from email.

Validate query language, audience fit, and the claims boundary. Do not publish an availability page until the linked build is publicly releasable.

Avoid starting with CC/BCC definitions, provider-password tutorials, or hundreds of comparison pages. Canary proves these can create reach, not that they create good Tecotype customers.

## Priority 2: macOS release-gated acquisition

Run only when all relevant public-release gates are cleared.

### 5. One complete intent-to-retention experiment

```text
one intent-aligned page
→ signed/notarized Apple Silicon public download
→ verified install
→ successful Gmail or IMAP connection
→ mailbox-ready threshold
→ first meaningful keyboard or local-search action
→ retained use
→ €149 annual or €15 monthly outcome
```

Primary success metric: qualified retained activation per unique eligible visitor.

Guardrails:

- authorization and sync failure;
- time to mailbox readiness;
- crash-free first sessions;
- support contact rate;
- compose/reply safety failures;
- uninstall or account deletion;
- privacy opt-out rate.

Do not call a download an activation.

### 6. Match the trial clock to value

If Tecotype adopts a trial, compare:

- trial starts after successful first account connection;
- trial starts after mailbox readiness;
- trial starts at first meaningful action.

Do not start the clock at file download. Canary’s public terms show how setup can consume a fixed seven-day window before value.

Any test must preserve clear no-surprise billing, the real monthly and annual prices, and a calm end-of-trial state.

### 7. Build Mac distribution proof

At release, keep these surfaces synchronized:

- system requirements and architecture;
- signed/notarized status;
- release notes;
- current version;
- update behavior;
- provider compatibility;
- accessibility and keyboard support;
- privacy and diagnostics;
- direct/store availability if both exist.

Canary’s help/store requirement drift shows how small inconsistencies add decision friction.

### 8. Earn narrow independent coverage

After reliability evidence exists:

- brief Mac email reviewers, keyboard-workflow specialists, and privacy-literate technical writers;
- give them a claim sheet and reproducible workflows;
- ask for no guaranteed sentiment;
- preserve source tags through the public download handoff;
- evaluate retained activation and support load, not link count.

Canary’s credible referral core is more useful than its noisy raw backlink total.

## Priority 3: Windows release-gated acquisition

Plan the channel now; publish availability only after the Windows product ships.

### 9. Create a separate Windows readiness contract

Windows acquisition requires its own verified proof:

- signed NSIS package;
- Microsoft Store path where appropriate;
- direct fallback;
- SmartScreen-aware trust experience;
- self-hosted update path;
- current Windows requirements;
- crash and update telemetry within Tecotype’s privacy boundary;
- Gmail/IMAP setup and compose/send smoke tests on Windows.

Do not reuse a Mac conversion rate, review quote, screenshot, or “available everywhere” statement as Windows evidence.

### 10. Repeat the same funnel with platform segmentation

Use the same event definitions as Mac so cohorts are comparable, but retain platform separation:

```text
Windows-intent page
→ verified signed Windows distribution
→ successful install/update
→ provider connection
→ mailbox ready
→ first value
→ retention
→ payment
```

The first Windows landing page should be released with the build, not months ahead as an availability claim. A clearly labeled research or notification page is acceptable only if its status is unmistakable.

## Priority 4: later scale tests

### 11. Expand SEO only after one page is economically legible

Require a page-level dashboard that distinguishes:

- generic informational sessions;
- eligible platform/provider visits;
- download or store handoff;
- successful setup;
- retained activation;
- paid outcome;
- support and refund burden.

Expand from one category-aligned cluster only if retained activation justifies it. Canary’s 61.2% ETV concentration in six broad blog pages is a reach benchmark, not a Tecotype target.

### 12. Test partnerships without surrendering the customer path

Potential later partners:

- keyboard-launcher and automation tools;
- local-search or knowledge-work tools;
- provider or migration specialists;
- curated software bundles;
- reviewers with a high share of Mac or Windows professional users.

Contract requirements:

- source visibility;
- direct customer communication rights where lawful;
- update and support responsibilities;
- economics by platform;
- exit and migration plan;
- no separate-build burden unless justified.

Canary’s Setapp exit shows why the end of the partnership must be designed before its launch.

### 13. Use app/store proof carefully

If Tecotype chooses platform stores:

- keep direct and store versions feature-compatible;
- track acquisition without invasive identity stitching;
- segment reviews by platform and version;
- respond to reliability themes in product work, not marketing rebuttals;
- never blend a rating from one platform into proof for another.

## Avoid list

- “Best,” “smartest,” “enterprise-grade,” or unbounded privacy claims without reviewable evidence.
- “Your email never leaves your device”; email still travels through the provider.
- AI-assistant positioning; Tecotype explicitly does not position itself as a chat assistant.
- “Available on Windows” before a public signed Windows build and update path ship.
- “Available everywhere” while distribution is Mac-first.
- A large customer/user count without active/paid/time/source definitions.
- Organization logos without permission and a defined relationship.
- Annualized monthly equivalents presented as if monthly billing exists.
- Trial time consumed before setup succeeds.
- Low-intent content volume before source-to-retention measurement works.
- A bundle or affiliate agreement without channel-exit protections.
- Platform parity claims based on one client.

## Recommended sequence

| Order | Test | Earliest valid stage | Decision signal |
| ---: | --- | --- | --- |
| 1 | Calm-control vs keyboard-flow vs local-recall message | Now | Accurate recall and qualified interest |
| 2 | Privacy/data-flow comprehension | Now | Correct understanding without policy prompting |
| 3 | Source and activation taxonomy | Now | Reviewable, privacy-minimal event specification |
| 4 | One high-intent Mac search brief | Now | Query/audience fit; no availability claim |
| 5 | Complete Mac page-to-retention test | After Mac release gates | Retained activation and paid outcome |
| 6 | Reviewer outreach | After reliable Mac release | Retained activation, review themes, support load |
| 7 | Windows readiness and platform page | After Windows release gates | Windows-specific setup, retention, payment |
| 8 | SEO cluster or partnership | After one legible cohort | Incremental retained value after full costs |

This sequence preserves Tecotype’s north star: speed is expected, privacy is structural, and calm is the experience.
