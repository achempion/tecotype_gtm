# Tecotype experiments

Tatem supports one strong acquisition hypothesis and one strong warning:

- Specific incumbent pain can create high-intent community discovery.
- Attention collected too far ahead of reliable access can damage trust.

Tecotype’s public website, first-run onboarding, broader distribution, licensing/payment flow, and acquisition experience are not complete. Trial duration and card requirements are undecided. The experiments below are therefore split into **now**, **release gate**, and **after the public funnel exists**.

Suggested thresholds are planning defaults for deciding whether to continue, not facts learned from Tatem.

## Experiment 1: problem and message research now

| Field | Design |
| --- | --- |
| Audience | Email-heavy Mac users who publicly describe one concrete problem: price, search, inbox control, keyboard workflow, or privacy |
| Hypothesis | A useful, disclosed contribution in a relevant discussion will lead to qualified research conversations and reveal which problem earns action |
| Prerequisite | A short, accurate explanation of Tecotype’s current state and a way to schedule research or request a future notification |
| Activity | Contribute to existing discussions only when Tecotype can add useful information; record the original pain, audience, and message used |
| Honest CTA | “Help us understand this problem” or “Ask to be notified when a suitable preview is ready” |
| Primary metric | Qualified research conversations, not impressions, votes, or raw email addresses |
| Continue signal | At least 5 qualified conversations from the first 10 substantive contributions, with a repeated pain among at least 3 people |
| Stop or reshape | Fewer than 3 qualified conversations, repeated audience mismatch, or discussion moderators/users perceive the activity as promotion |
| Claim boundary | Do not promise public access, a trial, payment, or a ship date that is not decided |
| Ethical risk | Undisclosed promotion or manufacturing conversations |

Test messages as hypotheses, not conclusions:

- Move through mail faster.
- Find mail the way you remember it.
- Keep inbox work calmer and more controlled.
- Run optional Better search locally, on-device.
- Use keyboard-first workflows.

The goal is to learn which combination of audience, trigger, and message earns a qualified next step.

## Experiment 2: access-readiness gate

This is not an acquisition channel. It addresses Tatem’s most visible access and trust risk.

| Field | Design |
| --- | --- |
| Audience | A small invited pilot matching the audience selected in Experiment 1 |
| Hypothesis | People who express interest can reach a meaningful product outcome without a long or ambiguous wait |
| Prerequisite | A defined activation event, safe distribution, accurate access instructions, and usable first-run/account onboarding |
| Honest CTA | “Join this limited pilot”; state who it is for, what works, what is incomplete, and when a response will arrive |
| Primary metric | Share of invited testers who can install, connect an account, and reach the chosen activation event |
| Access-readiness signal | At least 8 of 10 representative testers reach activation without founder intervention and without a severe data or sending issue; this does not replace Tecotype’s other release requirements |
| Stop or reshape | Access dates slip, onboarding requires repeated manual rescue, or the product cannot safely deliver the promised outcome |
| Claim boundary | Do not call a research list or unreachable waitlist “early access” |

The exact activation event still needs a product decision. It should represent experienced value, not merely an account connection.

## Experiment 3: community-to-activation after release prerequisites

Run only after the public site, distribution, onboarding, source tracking, and activation measurement work.

```text
Specific email problem
→ useful, disclosed community contribution
→ source-tagged problem page
→ accurate product demonstration and availability
→ download
→ successful account connection
→ chosen activation event
```

| Field | Design |
| --- | --- |
| Hypothesis | A page that continues the exact community problem will activate more qualified users than a generic homepage |
| Primary metric | Activated users per qualified landing visit |
| Comparison | Problem-specific page versus the general homepage |
| Continue signal | Activation rate exceeds the direct/homepage baseline after at least 10 activated users in the cohort |
| Stop or reshape | Traffic is unqualified, activation is below baseline, or community participation becomes repetitive promotion |
| Later metric | Trial or payment only after those mechanics are decided and implemented |

Use separate source tags for each community and discussion. Do not infer success from clicks alone.

## Experiment 4: curated design placements

Tatem Email was featured on dedicated pages at Curated Design, SEESAW, Godly, Minimal Gallery, and Refero. This proves placement, not why the sites selected Tatem or whether the placements produced users.

| Field | Design |
| --- | --- |
| Prerequisite | Polished, accurate public page; working download/onboarding; source-to-activation tracking |
| Activity | Submit one consistent page to a small batch of relevant design and product galleries |
| Primary metric | Activated users per placement |
| Secondary metric | Qualified visits; backlink count is diagnostic only |
| Continue signal | At least one placement produces activated users at acceptable effort, then repeat the source type |
| Stop signal | Ten relevant placements produce no activated user or mostly irrelevant traffic |
| Claim boundary | Do not treat a gallery’s view counter as Tecotype traffic |

## Experiment 5: one non-brand search page

Tatem’s current residual search is mostly branded and ambiguous. That does not prove historical SEO failed, but it shows why Tecotype should preserve category clarity.

Candidate phrases from the existing US keyword snapshot include:

| Keyword | Estimated volume | Difficulty | Research use |
| --- | ---: | ---: | --- |
| `email client for mac` | 480 | 36 | Strong platform/category candidate |
| `gmail desktop client` | 140 | 28 | Candidate if the page accurately describes shipped Gmail support |
| `privacy focused email client` | 390 | 23 | Validate intent and ensure every privacy claim is precise |
| `fast email client` | 20 | 49 | Low-volume message test |

These are third-party estimates, not Tatem performance.

Before building a page:

1. Inspect the live result set and search intent.
2. Confirm Tecotype can substantiate the exact phrase.
3. Choose one page and one activation path.
4. Preserve category, platform, and product clarity in title, description, heading, and directory copy.

Continue only if the page earns qualified impressions/clicks and activated users. Revise or stop if it ranks for the wrong intent or produces no qualified behavior after a meaningful impression sample.

## Experiment 6: Tatem audience-transition campaign

Run only after Tecotype’s public release path and activation measurement work, and only with the party that controls Tatem’s communication rights.

```text
Tatem or Wander sends to a defined email-era cohort
→ recipient sees an accurate Tecotype introduction
→ explicit Tecotype opt-in
→ source-tagged Tecotype page
→ download
→ successful account connection
→ chosen activation event
```

| Field | Design |
| --- | --- |
| Hypothesis | A defined Tatem Email cohort contains people whose original problem and platform match Tecotype |
| Prerequisite | Verified rights holder, valid consent, accurate cohort definition, working Tecotype funnel, and legal review |
| Test | Small Tatem-sent cohort; no raw list transfer |
| Primary metric | Activated Tecotype users per delivered message and per explicit opt-in |
| Secondary metrics | Delivery, click, unsubscribe, complaint, download, and account-connection rates |
| Continue signal | Qualified activation at an acceptable acquisition cost without abnormal complaints or unsubscribes |
| Stop signal | Legacy-product contamination, unclear consent, poor deliverability, low platform fit, or no qualified activation |
| Data boundary | No Gmail content, Google tokens, contacts, calendars, or other Tatem product data |

See [outreach.md](./outreach.md) for the founder, contact routes, privacy boundary, and diligence questions.

## What not to copy

- An indefinite waitlist without a credible access schedule.
- A broad “10,000+” count that does not define the cohort or value reached.
- Referral language before an actual referral mechanism exists.
- Undisclosed recommendations or manufactured conversations.
- AI, privacy, speed, or time-saved claims that are not demonstrated.
- A trial or payment step before Tecotype has decided and implemented one.
- Backlink, mention, or signup totals as a substitute for activation and retention.
- Legacy review pages that describe a different product.
- A raw purchase or import of Tatem’s audience instead of an explicit opt-in transition.

## Measurement sequence

Now:

```text
Community contribution
→ qualified research conversation
→ repeated audience/problem/message signal
```

After the release gate:

```text
Attributed visit
→ download
→ successful account connection
→ chosen activation event
→ retained use
→ payment only when implemented
```

This sequence matches Tecotype’s current stage and keeps planned work separate from shipped behavior.
