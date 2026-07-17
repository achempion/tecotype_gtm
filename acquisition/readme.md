# Acquisition research

Study how emerging competitors attract and convert attention, then use that evidence to choose acquisition experiments for Tecotype.

For each competitor, investigate:

- How people are likely to discover them
- Which search queries, referring sites, communities, partnerships, content, ads, or other channels appear to generate meaningful traffic
- How those channels connect to the competitor’s landing pages, positioning, offer, signup flow, activation, and payment
- Which acquisition approaches appear to be working, which appear weak or abandoned, and what evidence supports that assessment
- What the competitor has tried or changed over time, when historical evidence is available
- What Tecotype should test, adapt, or avoid based on the findings

The goal is not to copy competitors blindly. It is to find repeatable acquisition patterns that are relevant to Tecotype’s stage, audience, and positioning, then turn the strongest patterns into measurable experiments.

This research intentionally deprioritizes established market leaders. It focuses on emerging competitors whose acquisition methods, constraints, and scale are more comparable to Tecotype’s current stage.

## Directory structure

Give each competitor its own directory:

```text
competitor/
├── readme.md        # short conclusion and raw headline numbers
├── landing-page.md  # trackers, metadata, audience, positioning, and copy
├── traffic.md       # search queries, rankings, and landing pages
├── referrals.md     # backlinks, communities, and referring sites
├── funnel.md        # offer, CTA, signup, activation, and payment
├── history.md       # positioning, release, and funnel changes over time
├── opportunities.md # staged Tecotype marketing/distribution experiments and evidence gates
└── requests.md      # API calls, parameters, results, and limitations
```

Add other category files only when the research produces useful evidence. Keep
the competitor `readme.md` concise and link every conclusion to the detailed
file that contains its source and context.

Every competitor `readme.md` should conclude with:

```markdown
## Implications for Tecotype

- What appears to be working
- What appears weak, discontinued, or inconclusive
- What Tecotype should test
- What Tecotype should avoid
- Evidence strength and remaining unknowns
```

## Pipeline model

Map each pipeline as:

```text
Acquisition activity
→ discovery channel
→ search query, ad, mention, or referring site
→ landing page
→ offer and message
→ CTA
→ signup/download
→ activation
→ payment
```

Example:

```text
SEO page targeting keyboard-first email
→ organic search
→ “keyboard-first Gmail client” query
→ focused landing page
→ calm, private email client
→ download
→ connect Gmail
→ trial
→ subscription
```

## Stage 1: landing-page research

Start every competitor report with the public landing page. This stage is usually free and produces the hypotheses that later API calls should validate.

Record the URL, capture date, market, device or viewport, and whether the page appears current. Preserve the exact observed copy separately from interpretation.

### Technical evidence

Inspect the rendered page, not only its initial HTML:

- Analytics, advertising pixels, product analytics, session replay, A/B testing, chat, CRM, and affiliate scripts
- Measurement IDs and parameterized CTA destinations when publicly visible
- Page framework and CMS when they help explain how the site is operated
- Title, description, canonical URL, language, robots directives, Open Graph and Twitter tags, structured data, `hreflang`, and app links
- Primary and secondary CTA destinations, forms, downloads, signup links, and visible consent interfaces

An installed tag proves measurement capability, not active advertising or useful data. A missing client-side tag does not rule out server-side, consent-gated, geographically conditional, or blocked tracking.

### Customer and message hypothesis

Map the page as:

| Question | Evidence to capture |
| --- | --- |
| Who is it for? | Role, team or individual, company stage, sophistication, and use case |
| What job or pain leads them here? | Trigger, frustration, risk, and desired progress |
| What is the promise? | Outcome in the headline, description, and closing CTA |
| Why this product? | Mechanism, differentiated features, category, and alternatives |
| What is the emotional angle? | Calm, speed, status, control, delight, fear, or another appeal |
| What supports the claim? | Customer counts, testimonials, logos, benchmarks, demonstrations, and security claims |
| What is the offer? | Free plan, trial, demo, download, waitlist, guarantee, or pricing |
| What action is requested? | CTA wording, destination, friction, and the next visible step |

Label each conclusion:

- **Observed:** directly present in copy, metadata, scripts, or CTA behavior.
- **Inferred:** the most plausible customer, positioning, or channel hypothesis.
- **Unobservable:** traffic, conversion, activation, retention, and revenue.

Use these findings to choose a small set of distribution questions. For example, “Built for your keyboard” justifies checking keyboard-related queries and communities; a polished visual presentation justifies checking design galleries.

## Stage 2: DataForSEO validation

Use API evidence to confirm or reject the landing-page hypotheses. Do not collect every available metric: prioritize queries, referring sites, mentions, or ads that connect to a visible customer promise or CTA.

The reusable endpoint workflow, request guidance, pricing, and budget model live in [the DataForSEO documentation](../tools/dataforseo.md).

## Stage 3: funnel and experiment

Inspect the public path only: landing page, visible signup or download
destination, public store metadata, stated onboarding, activation clues,
offer, and payment terms. Do not download, install, mount, open, execute, or
inspect a competitor client or artifact, and do not create an account, connect
a mailbox, start a trial, submit a form, or enter checkout. Label the
unobserved client and commercial stages as stated, inferred, or unobservable.
Then map the strongest evidenced channel into a Tecotype marketing or
distribution experiment with source tags and a downstream activation event
supplied by the working client.

## Evidence boundary

External channel data provides evidence of potential acquisition paths, not actual traffic attribution. Search traffic is estimated, a backlink does not prove referral clicks, and a mention does not prove that it produced a signup.

Offer, message, CTA, signup, download, onboarding, activation, and payment must be inspected manually. Competitors’ actual conversion rates cannot be observed and must be validated through Tecotype experiments.

## Research queue

The queue contains 25 competitors. Earlier waves have higher priority, and
competitors within each wave are listed in the suggested research order.

### Wave 1: direct and comparable competitors

- [x] [Tatem](./tatem/readme.md): historical community, waitlist, and design-gallery acquisition
- [x] [Quartz](./quartz/readme.md): public-beta launch, download funnel, and close focus/privacy overlap
- [x] [Carbon Mail](./carbon-mail/readme.md): founder-led community discovery and reported retention difficulty
- [x] [Mimestream](./mimestream/readme.md): narrow Gmail-on-Mac positioning, long free beta, independent Mac coverage, and durable category search
- [x] [ZenMail](./zenmail/readme.md): owned SEO and repeated linked recommendations leading to an unquantified private-beta waitlist
- [x] [Epistles](./epistles/readme.md): provider-specific community research, broad distribution, early comparison SEO, and visible but unverified paid signals
- [x] [YouniqMail](./youniqmail/readme.md): broad informational SEO, founder community distribution, direct public beta, and a visible tester-feedback loop
- [x] [Velo](./velo/readme.md): open-source and AI-built launch attention on Reddit/GitHub, followed by signing, OAuth, update, and attribution friction
- [x] [Castellum](./castellum/readme.md): clear manager/local-AI positioning and a public build without an evidenced discovery or activation channel
- [x] [Locker](./locker/readme.md): direct release distribution, claimed free keys, small asset-request counts, and no observed paid conversion

The cross-client conclusions and recommended Tecotype sequence are in the
[Wave 1 synthesis](./wave-1.md).

### Wave 2: established clients and visible acquisition surfaces

- [x] [Mailbird](./mailbird/readme.md): provider-help and comparison SEO, current advertising, partners, referrals, stores, and licensing trust risk
- [x] [Superhuman Mail](./superhuman/readme.md): premium category creation, referrals, guided activation, team expansion, and suite-level attribution limits
- [x] [HEY](./hey/readme.md): point-of-view marketing, founder-led demonstration, launch attention, and provider-switching friction
- [x] [Shortwave](./shortwave/readme.md): Google Inbox replacement, recurring launches, taught workflow, AI/team expansion, and product-native sharing surfaces
- [x] [Canary Mail](./canary-mail/readme.md): broad informational SEO, store presence, privacy/security positioning, and data-flow qualifications
- [x] [Spark](./spark/readme.md): long-running freemium, stores, Setapp, launches, content, current ads, and dual-client migration risk
- [x] [eM Client](./em-client/readme.md): provider-help SEO, reseller economics, Postbox migration, advertising, and explicit desktop licensing
- [x] [MailMate](./mailmate/readme.md): durable independent discovery within a narrow keyboard-and-search niche

The cross-client conclusions and recommended Tecotype sequence are in the
[Wave 2 synthesis](./wave-2.md).

### Wave 3: emerging signals, failures, and adjacent models

- [x] [ReplylessAI](./replyless-ai/readme.md): repeated launches, directories, lifecycle email, and the wave's clearest small verified paid signal without source-to-paid attribution
- [x] [Orchid](./orchid/readme.md): Zero's open-source and coordinated launch visibility followed by a category, domain, and CTA transition
- [x] [MonoMail](./monomail/readme.md): founder/community discovery and measurable release downloads without observable activation or payment
- [x] [Extra](./extra/readme.md): consumer action-first launch, tagged referral and creator routes, recent creatives, and an unmonetized free offer
- [x] [Airo Mail](./airo-mail/readme.md): conflicting mobile-consumer and solo-founder public variants, concrete workflow evaluation, and no adoption or price validation
- [x] [Notion Mail](./notion-mail/readme.md): major-brand launch discovery followed by a scheduled September 22, 2026 inbox shutdown and transition intent
- [x] [Newton Mail](./newton-mail/readme.md): shutdowns, relaunches, brand-led search, public-state conflicts, and persistent trust and alternative-search debt

The cross-client conclusions and recommended marketing sequence are in the
[Wave 3 synthesis](./wave-3.md).

## Additional checks

When relevant, research may benefit from:

- **Wayback Machine** for historical positioning, pricing, and funnel changes.
- **Official ad libraries**, especially Google and LinkedIn.
- **Dealroom, Crunchbase, and founder statements** to verify funding status.
- **Manual landing-page and funnel inspection**, which remains indispensable.
