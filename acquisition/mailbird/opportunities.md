# Mailbird-derived opportunities for Tecotype

Research date: **2026-07-17**

These are experiments, not shipped Tecotype capabilities. They are constrained
by [product.md](../../product.md), [positioning.md](../../positioning.md), and
the current implementation/release state in the adjacent Tecotype repository.

## What the evidence supports

Mailbird suggests six useful hypotheses:

1. A narrow platform and provider story can earn press before a full
   productivity-suite story exists.
2. Search can compound for years, but query intent matters more than raw
   estimated traffic.
3. Referrals work best when an existing user has enough product value to share.
4. Reviewers, affiliates, partners, stores, and paid ads can reinforce one
   category when their landing claims agree.
5. First- and last-touch capture is useful only if source identity continues
   into product activation and retention.
6. Ambiguous update and “lifetime” language can turn customers into long-lived
   negative referrers.

Mailbird's public evidence does **not** establish that a thousand pages,
discount anchors, lifetime offers, referrals, or paid creative are profitable.

## Current release truth

Tecotype is under active development.

### macOS

The repository contains a signed and notarized Mac release path, and the
current signed target is Apple Silicon. That is an implementation capability,
not proof that a public build is released and ready for acquisition. Existing
local builds are testing-only.

Before any public Mac download or paid campaign, verify:

- clean first-run and no-account states;
- accurate public site, screenshots, and provider scope;
- licensing and the €149/year or €15/month payment path;
- Gmail restricted-API/audit completion;
- Developer ID signing, notarization, and clean-machine installation;
- update, rollback, and release-hosting behavior;
- safe, predictable compose, reply, and send behavior;
- current privacy/security and optional Better-search claims;
- support and incident response; and
- privacy-minimal source-to-activation measurement.

Local ad-hoc test builds must not be distributed.

### Windows

The architecture plans signed NSIS, self-hosted and store distribution, and a
Windows signing pipeline. That distribution is not shipped. Research,
interviews, keyword observation, reviewer mapping, and partner discovery can
happen now; public availability, downloads, pricing routes, and “works on
Windows” claims must wait for a signed build to pass the Windows release gate.

### Roadmap boundaries

MCP integration, broader local intelligence, and agent-driven automation are
future work. They must not be placed in acquisition copy as current
capabilities. “Local,” “private,” and “offline” claims must stay within the
verified data path.

## Experiment 1: job-and-switch interviews

**When:** before public release.

**Question:** Which narrow job is frequent and painful enough to make a
professional switch desktop email clients?

Recruit 8–10 people across:

- several Gmail or Google Workspace accounts;
- Gmail plus one or more IMAP accounts;
- keyboard-oriented Mac workflows;
- people who often retrieve mail from partial or cross-language memory; and
- current Apple Mail, Outlook, Thunderbird, Mimestream, Mailbird, or other
  client users.

Ask for the last real incident in which they:

- could not find a remembered message;
- lost focus while triaging;
- switched accounts or applications to complete one email job;
- distrusted a client's data path; or
- tried and abandoned a replacement.

Record provider mix, trigger, workaround, frequency, consequence, switching
attempt, and exact language. Do not present a development build as publicly
available or planned functionality as shipped.

**Decision rule:** choose one lead job only if at least 5 participants
independently describe the same frequent problem and at least 3 have recently
tried to solve it.

## Experiment 2: one job-close landing page

**When:** after the Mac release gate.

**Question:** Can a page close to a validated job produce first value and
return, not just search impressions?

Candidate messages:

- find mail the way you remember it;
- calm keyboard triage for a real inbox; or
- Gmail plus IMAP in one focused Mac client.

The page should contain:

- one honest problem;
- one shipped mechanism;
- current Gmail/IMAP and Mac scope;
- optional on-device Better-search explanation where relevant;
- accurate price;
- a quiet primary CTA;
- known limitations; and
- a durable source identifier.

Measure:

```text
qualified landing session
→ signed-build handoff
→ verified installation
→ first launch
→ mailbox connection
→ completed initial sync
→ page-matched Better-search or triage action
→ voluntary day-1 and day-7 return
→ payment
```

**Decision rule:** do not expand content inventory until at least five non-team
users reach the page-matched first value and at least three return voluntarily
on day 7. These are learning thresholds, not statistical proof.

Mailbird's Juno and Frontier traffic is a warning: volume far from the software
decision should not be the first target.

## Experiment 3: one reviewer or community source

**When:** after a small Mac cohort completes the path reliably.

**Question:** Can a credible external source reproduce the product's core value
and send retained users?

Choose one reviewer or community whose audience matches the validated job.
Provide:

- affiliation and access disclosure;
- one-sentence category and founder motivation;
- exact shipped provider/platform matrix;
- clean installation and update instructions;
- keyboard and Better-search demonstrations;
- a simple data-flow and telemetry statement;
- price and cancellation terms;
- known limitations; and
- no request for editorial control.

Assign one durable source token and report the complete path separately from
unattributed traffic.

**Pass condition:** at least three source-attributed non-team users reach first
value and at least two return on day 7. Comments, votes, article views, and
downloads do not pass.

## Experiment 4: value-earned referral

**When:** only after retained users exist.

**Question:** Does a calm, non-gamified invitation produce equally or more
retained users than direct acquisition?

Trigger the referral option after a user has:

- connected at least one real account;
- completed sync;
- reached the selected first-value action more than once; and
- returned voluntarily.

Test a simple invitation with no fake scarcity and no automatic contact access.
The user chooses recipient and channel. Clearly label any reward and its tax,
renewal, and update implications.

Track:

```text
eligible retained user
→ invitation shown
→ invitation voluntarily sent
→ recipient visit
→ install and activation
→ recipient day-7 return
→ recipient payment
```

Compare referred retention and support burden with the originating channel.
Do not use address-book scraping, pre-checked sharing, social-point schemes, or
“lifetime” rewards.

## Experiment 5: narrow provider support content

**When:** after release and after real support knowledge exists.

**Question:** Can one provider-specific guide attract a qualified setup or
switching user without becoming a low-intent traffic farm?

Choose one provider actually supported in the release. The page should:

- solve a real configuration or switching problem;
- state whether the action occurs in Tecotype, the provider, or the OS;
- name Mac-only availability at that point;
- distinguish IMAP/Gmail behavior;
- link to the relevant trust explanation;
- avoid impersonating a provider login page; and
- carry source identity through product activation.

Primary success is retained first value. Search rank and visits are secondary.
Do not scale into hundreds of setup pages unless several independently produce
retained customers at acceptable support cost.

## Experiment 6: paid exact-intent validation

**When:** only after organic or reviewer traffic shows measurable activation
and day-seven return.

**Question:** Can a small exact-intent campaign acquire a retained paid Mac
user inside the allowable economics?

Use one ad group and one landing page for the proven job. Exclude provider-login
and generic free-email intent. Cap spend in advance and preserve campaign ID
through the full path.

Track:

- qualified clicks;
- installation;
- mailbox connection;
- first value;
- day-one and day-seven return;
- paid conversion;
- refund;
- support time; and
- net cash after tax and payment fees.

Stop if clicks do not activate or activated users do not return. Mailbird's ad
archive proves only that it runs ads; it supplies no benchmark CAC.

## Windows sequencing

Run Windows problem interviews and maintain a release-specific demand ledger
now. Do not reuse the future Mac landing page with a misleading platform
toggle.

After signed Windows distribution is shipped and verified:

1. publish a separate release-accurate Windows page;
2. verify install, update, uninstall, default-client, provider auth, safe send,
   and storage behavior on supported Windows versions;
3. carry source through those Windows-specific events;
4. compare Mac and Windows activation/retention separately; and
5. only then test Windows reviewers, provider guides, partners, or ads.

Platform availability is a claim that must be verified per build, not inherited
from the product roadmap.

## Trust and commercial guardrail

Before acquisition, maintain a claim ledger:

| Claim | Product behavior | Policy/terms | Verification | Owner |
| --- | --- | --- | --- | --- |
| Mac availability | Current signed public build | Download page | Clean-machine install/update | Release |
| Windows availability | Planned until shipped | Roadmap only | Signed-build release test | Release |
| Mail storage | Current implementation | Privacy policy | Storage/network inspection | Engineering |
| Better search | Optional and on-device | Product/privacy copy | Model/data-flow test | Engineering |
| Gmail data | Current scopes and processing | Google disclosure | OAuth and audit artifacts | Engineering/legal |
| Source measurement | Minimal identifiers/events | Privacy policy | Event/network audit | Product |
| Price and updates | €149 annual / €15 monthly | Terms and checkout | Purchase/cancel/refund test | Operations |

Block publication whenever a row disagrees.

Mailbird's licensing history makes one rule especially important: never use
“lifetime,” “forever,” or “all future versions” unless the governing terms,
technical support policy, reserves, and successor plan can honor the plain
meaning.

## Economics guardrail

Mailbird's current free, discounted annual, and Pay Once prices do not reveal
its support costs, retention, refund rate, or margins. They are not evidence to
change Tecotype's decided **€149/year or €15/month** professional position.

For each source, retain:

- content, partner, or advertising cost;
- qualified sessions;
- installs;
- connected mailboxes;
- first-value users;
- day-seven retained users;
- paid customers;
- refunds and payment fees;
- support burden; and
- net contribution where available.

Scale only on retained-customer economics.

## Actions to avoid

- Do not build a thousand-page SEO inventory before one page produces retained
  value.
- Do not treat provider-login traffic as buyer intent.
- Do not use conflicting customer/account/download counts.
- Do not use “last sold” widgets, false urgency, or loud gamification.
- Do not seed apparently independent recommendations.
- Do not broaden local/privacy/offline claims beyond verified behavior.
- Do not promote future MCP or Windows work as shipped.
- Do not distribute ad-hoc Mac builds.
- Do not use a version-bounded one-time license in a way a reasonable buyer
  would interpret as lifetime updates.

## Recommended order

1. Run job-and-switch interviews without offering unfinished access.
2. Complete Mac release, trust, payment, and measurement gates.
3. Publish one job-close page.
4. Test one reviewer or community source.
5. Add referrals only after repeat value.
6. Add one provider guide only after real support knowledge exists.
7. Test paid exact-intent traffic only after activation and retention are
   measurable.
8. Repeat the release-and-measurement gate independently for Windows.
