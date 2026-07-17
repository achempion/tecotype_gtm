# Tecotype experiments

Research date: **2026-07-17**

Mimestream supports three useful hypotheses:

1. A narrow, technically credible category can make launch, press, and search reinforce one another.
2. Reviewers form stronger proof when they can use a working product before a commercial launch.
3. A large free audience is not the same as a healthy paid transition.

Tecotype is not ready for Mimestream’s public acquisition sequence. Gmail and IMAP foundations, local storage/search, optional on-device Better search, reminders, sending core, and keyboard architecture exist with important caveats. Split Inbox, first-run/no-account onboarding, license/payment, public website, Gmail audit, signed installers/distribution, reply threading, and scheduled-compose UI are not release-complete.

The experiments below are split into **now**, a **release gate**, and **after release prerequisites**. Thresholds are planning defaults, not facts learned from Mimestream.

## Experiment 1: narrow-category message research now

| Field | Design |
| --- | --- |
| Audience | Mac professionals who spend substantial time in email and use Gmail, IMAP, or both |
| Hypothesis | A precise combination of platform, workflow, and shipped differentiator will earn more qualified research conversations than a broad “better email” promise |
| Candidate messages | “A calm, keyboard-first email client for Mac”; “Gmail and IMAP in one keyboard-first Mac client”; “Local email search for the way you remember messages” |
| CTA | “Help us understand this workflow” or “Ask to be notified when a suitable preview is ready” |
| Primary metric | Qualified conversations with a repeated problem, not raw emails or impressions |
| Continue signal | At least 5 of the first 10 qualified participants describe the same high-cost workflow and at least 3 ask for the same next step |
| Stop or reshape | Audience mismatch, claims require unfinished features, or people understand the message differently than intended |
| Claim boundary | Describe current development state; do not offer a public trial, payment, or ship date |

Interview prompts should separate the hook from preference:

- Does keyboard speed earn attention?
- Does calm control make the product preferable?
- Does Gmail plus IMAP broaden relevance or dilute the story?
- Does optional on-device Better search solve a recurring retrieval problem?
- Which current behavior earns a request to try: triage, search, reminders, sending, or account unification?

Do not lead with Split Inbox until its release behavior is usable enough to demonstrate. Do not call Better search “AI-powered email” or imply any mail leaves the device.

## Experiment 2: founder and reviewer proof package now

Mimestream’s founder credential and Gmail-API explanation made the product story unusually coverable. Tecotype cannot copy the biography, but it can prepare equally specific proof.

| Field | Design |
| --- | --- |
| Audience | Future Mac, email, keyboard-workflow, privacy, and productivity reviewers |
| Hypothesis | A brief grounded in product mechanism and honest limits will make later evaluation easier and more accurate |
| Build now | One-sentence category; founder motivation; shipped-capability matrix; data-flow diagram; keyboard demo; local-search explanation; known limitations; screenshots marked development-only |
| Primary metric | Five reviewer or expert interviews can accurately repeat who Tecotype is for and why it differs |
| Continue signal | At least 4 of 5 can restate the category without correction and identify one proof they would want to test |
| Stop or reshape | Brief depends on unshipped Split Inbox, unsafe reply behavior, unscheduled compose UI, or unavailable distribution |
| Ethical boundary | No press logo, endorsement, testimonial, or “reviewed by” language before publication/permission |

This creates launch readiness; it is not a request for coverage yet.

## Experiment 3: release-readiness gate

Do not amplify public access until representative users can safely reach value.

Required product and business conditions:

- usable first-run and no-account onboarding;
- safe Gmail and IMAP account connection;
- completed Gmail audit required for intended distribution;
- signed/notarized installer and update path on the initial platform;
- public website and download route;
- license/payment behavior for the decided €149/year or €15/month Individual price;
- trial duration and card requirement explicitly decided;
- Split Inbox behavior suitable for any public Split Inbox claim;
- reply threading and scheduled-compose UI resolved or clearly excluded from claims;
- safe send, failure, and recovery paths;
- privacy-reviewed attribution and activation events.

Representative release test:

| Field | Design |
| --- | --- |
| Audience | Ten invited people matching the audience from Experiment 1 |
| Task | Install, connect the intended account type, complete a real workflow, and recover from one expected error without founder help |
| Activation candidate | Successful account sync plus one meaningful action: three keyboard triage actions and a successful local search |
| Gate signal | At least 8 of 10 reach the event unaided, no severe send/data issue occurs, and limitations are understood |
| Stop | Manual rescue is routine, OAuth/distribution is blocked, reply behavior is unsafe, or activation logging collects more data than necessary |

This threshold supplements the architecture and release requirements; it does not replace them.

## Experiment 4: founder-led technical launch after the gate

```text
Specific Mac-email problem
→ technically honest founder story
→ source-tagged landing page
→ signed download
→ account connection
→ meaningful activation
→ retained use
```

| Field | Design |
| --- | --- |
| Hypothesis | A founder explanation of one real Mac email problem will activate more qualified users than generic launch copy |
| Candidate community | One community whose members already discuss Mac software, keyboard workflows, local software, or email clients |
| Story | Why the problem exists, what Tecotype built, what runs locally, what is incomplete, and who should not use it |
| Primary metric | Activated users per qualified landing visit |
| Secondary | Account-connection rate, day-1/day-7 retained use, qualitative objections |
| Continue signal | At least 10 activated users and activation above the direct/homepage baseline |
| Stop | Conversation becomes repetitive promotion, traffic is mostly out-of-platform, or severe product issues appear |

Use one tagged source at a time or preserve clean source separation if launch activities are coordinated. Community points and comments are diagnostic only.

## Experiment 5: expert Mac reviewer sequence after the gate

Mimestream’s strongest referral proof came from reviewers who used the app for months. Tecotype should optimize for credible use, not publication count.

| Field | Design |
| --- | --- |
| Audience | A first cohort of 8–12 independent Mac/email/productivity reviewers with explicit audience fit |
| Offer | Working build, accurate briefing, responsive support, and enough evaluation time; no editorial control |
| Source path | Unique privacy-preserving source link per publication/reviewer |
| Primary metric | Activated and retained users per published review |
| Proof metric | Reviewer can substantiate the specific claim they publish |
| Continue signal | At least 2 independent reviewers choose to publish and at least one source produces retained users |
| Stop | Reviewers cannot reach promised value, coverage depends on payment without clear disclosure, or claims drift beyond shipped behavior |

Do not require positive coverage. Do not use private feedback as a testimonial. Record gifts, sponsorships, and affiliate arrangements conspicuously if any exist.

## Experiment 6: one category-aligned search page after the gate

Mimestream’s homepage holds 95.5% of current modeled organic ETV. Tecotype should first test message/search alignment on one useful public page.

Candidate intent families to validate live before publishing:

- `keyboard first email client mac`;
- `gmail and imap email client mac`;
- `local email search mac`;
- `email client for keyboard shortcuts`;
- `private email client mac`.

| Field | Design |
| --- | --- |
| Hypothesis | One page that precisely matches a qualified problem will produce more activation than broad email-client copy |
| Prerequisite | Shipped proof for every title/description/hero claim and a working download-to-activation path |
| Page | One intent, one audience, one demonstrated workflow, one CTA |
| Primary metric | Activated users from non-brand organic visits |
| Secondary | Qualified impressions, click-through, account type, activation reason |
| Continue signal | The page earns relevant queries and at least 5 activated users before expansion |
| Stop or revise | It ranks for the wrong intent, attracts unsupported provider/platform demand, or produces no activation after a meaningful qualified sample |

Add normal indexability basics—canonical metadata, sitemap, and robots guidance—but do not confuse technical hygiene with demand.

## Experiment 7: trial and paid-transition design

Mimestream proves that a no-card 14-day trial and subscription were used. It does not prove they are optimal. Its public 2023 discussion shows why transition clarity matters.

| Field | Design |
| --- | --- |
| Hypothesis | A trial beginning at first usable account sync, with calm early pricing disclosure, will preserve more qualified activation than deadline-led conversion |
| Variants | Trial length and card requirement only after product/legal/payment implementation; avoid testing too many dimensions at once |
| Disclosure | Price before download, exact trial start/end, what happens afterward, cancellation/refund terms, and data behavior |
| Primary metric | Paid conversion among activated users |
| Guardrails | Activation, day-7 retention, refund, support burden, uninstall, and complaint rates |
| Continue signal | Paid lift without worse activation/retention or abnormal complaints |
| Stop | People cannot complete setup before time starts, pricing surprises users, or expiry risks mail access/data confidence |

Tecotype’s current decided Individual prices are €149/year and €15/month. Trial duration, card requirement, and licensing/payment mechanics remain undecided or unimplemented; do not publish a trial until these choices work end to end.

Avoid a short-notice expiry for existing testers. Give any preview cohort explicit terms at entry and generous notice before changing access.

## Experiment 8: narrow workflow partnership later

Mimestream’s Hookmark collaboration demonstrates a credible shape: real interoperability, shared editorial explanation, and an adjacent audience.

| Field | Design |
| --- | --- |
| Hypothesis | A working integration with a Mac keyboard/productivity tool will produce more retained use than an unrelated affiliate placement |
| Prerequisite | Stable deep links, automation, or another shipped integration plus clear data boundaries |
| Test | One partner, one documented workflow, reciprocal tutorial, tagged destination |
| Primary metric | Activated and day-7 retained users from the partner |
| Continue signal | At least 5 retained users and partner audience reports the workflow is genuinely better |
| Stop | Integration requires private mail access by the partner, support cost exceeds value, or exposure is the only benefit |

No suitable Tecotype integration should be implied until it exists.

## What not to copy

- A headline audience count without source, activation, and retention definitions.
- A free beta whose later commercial terms are unclear.
- A short deadline between paid-launch notice and preview expiration.
- First-year discounts that pressure people before they can finish setup or trial.
- Homepage privacy shorthand without a full data-flow qualification.
- Backlink totals that count piracy and download mirrors as qualified reach.
- Publication logos without direct evidence and permission.
- A content program before one category page can activate users.
- Public acquisition before onboarding, signing, OAuth, payment, and reply/compose safety are ready.

## Measurement sequence

Now:

```text
qualified conversation
→ repeated audience/problem
→ message comprehension
→ request for a suitable future preview
```

Invited readiness test:

```text
invitation
→ signed install
→ account connection
→ chosen meaningful activation
→ unaided repeat use
```

After release:

```text
attributed qualified visit
→ download
→ first launch
→ account connection
→ meaningful activation
→ day-1/day-7 retention
→ paid conversion
```

Collect the minimum data required to make the next decision. Mimestream’s public evidence is strongest at attention and positioning; Tecotype’s experiments should be judged by activation and retained value.
