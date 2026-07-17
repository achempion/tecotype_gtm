# Tecotype experiments

Research date: **2026-07-17**

Velo supports one attractive hypothesis and one strong warning:

1. An inspectable technical story can create rapid, durable attention.
2. If distribution, setup, claims, and measurement are not release-ready, that attention can select for controversy and create no legible path to retained use.

Tecotype is in active development. Gmail and IMAP foundations, local storage/search, optional on-device Better search, reminders, sending core, and keyboard architecture exist with important caveats. This is not a public-release claim. First-run/no-account onboarding, the public site, licensing/payment, Gmail restricted-API readiness, signed/notarized updateable distribution, safe-send behavior, and source-to-activation measurement remain release-gated.

The experiments below are split into **now**, a **release gate**, and **after the gate**.

## Experiment 1: message research now

| Field | Design |
| --- | --- |
| Audience | Mac professionals with a recurring high-cost email workflow |
| Hypothesis | A precise shipped-capability story will produce more qualified conversations than “AI-powered email” or a long feature list |
| Candidate problems | Keyboard triage; finding mail by remembered context; calm multi-account handling; follow-up control |
| Candidate language | “A calm, keyboard-first email client for Mac”; “Find email the way you remember it”; “Gmail and IMAP, under your control” |
| CTA | Research conversation or honest release notification |
| Primary metric | Repeated problem and requested next step, not impressions or raw email count |
| Continue signal | At least 5 of the first 10 qualified participants describe the same costly workflow; at least 3 request the same next step |
| Stop/reshape | People interpret the promise differently, the hook depends on unfinished behavior, or interest is mainly generic AI curiosity |

Rules:

- describe Tecotype as in development;
- demonstrate only behavior that can be reproduced;
- do not offer a public trial or payment before the gate;
- keep Split Inbox and other unfinished behavior out of acquisition claims;
- distinguish on-device Better search from provider-hosted processing.

## Release gate

Velo’s public friction makes these prerequisites acquisition-critical, not housekeeping.

| Gate | Minimum evidence before public acquisition |
| --- | --- |
| First-run/no-account | A fresh Mac can reach the account-choice screen without a Tecotype account; errors and recovery are tested |
| Public site | Truthful pages for product, platform requirements, provider setup, privacy/data flow, pricing, support, and download |
| Licensing/payment | License state, checkout, entitlement, renewal/cancellation, failed-payment handling, and recovery are tested |
| Gmail restricted API audit | Requested scopes, consent-screen status, verification/audit obligations, privacy policy, and reviewer path are explicitly cleared |
| Signed/notarized distribution | macOS application and installer pass signing, notarization, Gatekeeper, clean-machine install, and provenance checks |
| Updateable distribution | Signed update manifests/artifacts, rollback/recovery, stale-build behavior, and a real update rehearsal pass |
| Safe-send | Reply/new-message routing, aliases, recipients, attachments, draft recovery, error states, undo behavior, and duplicate-send prevention pass |
| Source-to-activation measurement | Consent-aware source, message, platform, build, setup, sync, first-value, and retention events join without message content or personal addresses |

Do not begin broad public acquisition while any gate can turn attention into lost trust.

## Experiment 2: prove the end-to-end release path

Run this before inviting external traffic.

```text
clean Mac
→ source-tagged landing page
→ correct signed/notarized download
→ verified first launch
→ no-account onboarding
→ Gmail or IMAP setup
→ first sync
→ first useful action
→ safe reply
→ update to next signed build
```

Test at least:

- current supported macOS minimum and latest macOS;
- Apple Silicon and Intel if both are promised;
- one ordinary Gmail account after audit clearance;
- two materially different IMAP providers;
- interrupted setup and sync;
- expired or revoked credentials;
- offline/reconnect;
- update failure and recovery.

Pass only if the observed product and public setup copy agree.

## Experiment 3: founder proof story after the gate

| Field | Design |
| --- | --- |
| Audience | Mac email power users and technically credible reviewers |
| Hypothesis | A founder explanation of one hard email problem plus inspectable proof earns qualified activation without making the build method the product |
| Asset | Short post, 60–90 second reproducible demo, architecture/privacy note, and source-tagged landing variant |
| Story spine | User problem → design constraint → shipped proof → exact privacy boundary → who should try it |
| Primary metric | Provider connection and first-value completion per qualified landing visitor |
| Guardrail | Support incidents, signing failures, unsafe-send incidents, and privacy misunderstandings |
| Continue signal | Activation exceeds the baseline without increased trust/support failures |
| Stop signal | Discussion centers on implementation spectacle, claims outrun the build, or activation cannot be joined to source |

Do not frame Tecotype as “built by AI.” If AI assisted development, that is process detail, not the acquisition promise.

## Experiment 4: staged community launch

Use small, sequential cohorts so each source teaches something.

1. Invite 10–20 problem-matched design partners.
2. Resolve common first-run, provider, sync, send, and update failures.
3. Invite a small Mac/productivity community cohort with unique source links.
4. Invite two or three hands-on reviewers with a support and disclosure brief.
5. Only then consider Hacker News, Reddit, Product Hunt, or a larger founder-network launch.

For each source, record:

- landing view;
- CTA;
- signed first launch;
- provider setup start/completion;
- first sync;
- selected first-value event;
- day-1 and day-7 active state;
- paid conversion where applicable;
- coarse support category.

Do not compare channels on clicks alone.

## Experiment 5: privacy and setup truth page

Velo’s absolute privacy copy and hidden Gmail prerequisite create a concrete opening.

Test a page that answers, before download:

- where mail and indexes are stored;
- what is encrypted and what relies on macOS file protection;
- whether Tecotype operates a mail-processing backend;
- what Google or an IMAP provider necessarily receives;
- what optional on-device Better search does;
- which diagnostics exist and what they exclude;
- exact Gmail/IMAP setup prerequisites;
- supported macOS versions and update behavior.

Primary success metric: setup completion without an increase in privacy-related abandonment or support. A lower CTA rate with higher qualified activation may be a win.

## Experiment 6: category pages after release

Velo has branded-result coverage but almost no broad category footprint. Tecotype can test a small page set after the public product path works:

- keyboard-first email client for Mac;
- local email search;
- Gmail and IMAP on Mac;
- calm inbox triage;
- privacy architecture;
- platform/setup/download.

Each page should:

- target one job, not a 130-feature list;
- contain a real screenshot or reproducible demo;
- name compatibility and provider constraints;
- use a source-preserving CTA;
- join the visitor to activation without collecting message content.

Continue only when a page contributes activated or paid cohorts, not merely rankings.

## Experiment 7: reviewer proof

Velo’s third-party coverage mostly repeats first-party text. Tecotype should seek fewer, deeper reviews:

- provide a signed build and exact setup guide;
- disclose development status and unsupported behavior;
- ask reviewers to test search, triage, provider setup, safe reply, offline/reconnect, and update;
- do not prescribe positive language;
- quote only with permission and retain context.

The success signal is independently observed workflow value and trust, not article count.

## Measurement model

Use a privacy-minimal join:

```text
source_id
+ message_variant
+ platform/build
+ provider_class
+ setup result
+ coarse first-value event
+ day-1/day-7 state
+ license state
```

Exclude:

- sender/recipient addresses;
- subject or message content;
- search queries;
- attachment names;
- OAuth tokens or provider credentials.

Publish a clear measurement explanation. Calm acquisition depends on users understanding what is measured.

## What not to copy

- “completely private” or “data never leaves” when any provider flow exists;
- “ready in two minutes” before timing ordinary-user setup;
- the AI build process as the primary customer promise;
- feature-count hero copy;
- free/open-source positioning for a commercial product;
- generic release-page handoffs;
- unsigned or non-updateable public distribution;
- votes, views, stars, forks, or asset requests reported as users;
- rapid channel expansion before source-to-activation evidence exists.

## Priority order

1. Run narrow problem/message research honestly now.
2. Complete and verify the release gate.
3. Prove the signed source-to-first-value path internally.
4. Launch to small, source-tagged cohorts.
5. Add founder, community, reviewer, and search channels sequentially.
6. Scale only the channels that produce safe activation, retention, and paid conversion.
