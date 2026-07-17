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
└── requests.md      # API calls, parameters, results, and limitations
```

Add other category files only when the research produces useful evidence. Keep the competitor `readme.md` short and link every conclusion to the detailed file that contains its source and context.

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

Walk the public path from landing page through signup or download, authorization, onboarding, activation clues, and payment. Then map the strongest evidenced channel into a Tecotype experiment with source tags and a defined activation event.

## Evidence boundary

External channel data provides evidence of potential acquisition paths, not actual traffic attribution. Search traffic is estimated, a backlink does not prove referral clicks, and a mention does not prove that it produced a signup.

Offer, message, CTA, signup, download, onboarding, activation, and payment must be inspected manually. Competitors’ actual conversion rates cannot be observed and must be validated through Tecotype experiments.

## Research queue

The queue contains 25 competitors. Earlier waves have higher priority, and
competitors within each wave are listed in the suggested research order.

### Wave 1: direct and comparable competitors

- [x] [Tatem](./tatem/readme.md): historical community, waitlist, and design-gallery acquisition
- [x] [Quartz](./quartz/readme.md): public-beta launch, download funnel, and close focus/privacy overlap
- [ ] [Carbon Mail](https://www.carbonmail.app/): founder-led community acquisition and reported retention difficulty
- [ ] [Mimestream](https://mimestream.com/blog/mimestream-launches): independent Mac-client path from public beta to a paid product
- [ ] [ZenMail](https://usezenmail.com/): closest calm, keyboard-first, local-AI positioning overlap; research when its private-beta funnel is more observable
- [ ] [Epistles](https://epistles.com/): shipping local-first client with broad provider support and visible pricing
- [ ] [YouniqMail](https://youniqmail.com/): public-beta distribution for a private, customizable, cross-platform IMAP client
- [ ] [Velo](https://velomail.app/): open-source distribution for a keyboard-first, private Gmail client
- [ ] [Castellum](https://castellummail.com/): early-access positioning around managers, Gmail plus IMAP, and local AI
- [ ] [Locker](https://www.inbox.locker/): downloadable local IMAP client with approval-gated automation

### Wave 2: proven acquisition models

- [ ] [Mailbird](https://www.getmailbird.com/about/): large-scale search, content, comparison, and partner acquisition
- [ ] [Superhuman Mail](https://superhuman.com/company/about): premium category creation, referrals, and assisted activation
- [ ] [HEY](https://37signals.com/01): point-of-view marketing, calm positioning, and provider-switching friction
- [ ] [Shortwave](https://www.shortwave.com/blog/introducing-shortwave/): venture-backed launch, batching, team adoption, and multi-platform expansion
- [ ] [Canary Mail](https://canarymail.io/): privacy-led positioning combined with broad platform distribution
- [ ] [Spark](https://sparkmailapp.com/about): long-running freemium and app-store distribution across platforms
- [ ] [eM Client](https://www.emclient.com/for-companies): provider breadth, business acquisition, and durable desktop distribution
- [ ] [MailMate](https://freron.com/): durable independent acquisition within a narrow keyboard-and-search niche

### Wave 3: emerging signals, failures, and adjacent models

- [ ] [ReplylessAI](https://www.producthunt.com/products/replylessai): early paid signal from a bootstrapped cross-provider product
- [ ] [Orchid](https://0.email/about): open-source, GitHub, and community-led distribution
- [ ] [MonoMail](https://monomail.millosaurs.me/): measurable early downloads for a minimal, open-source mobile client
- [ ] [Extra](https://www.upstartsmedia.com/p/extra-consumer-ai-email-app-launches): consumer launch and early-beta adoption around a non-chronological inbox
- [ ] [Airo Mail](https://www.airo.email/): founder-focused positioning and an unusually high visible price for an emerging client
- [ ] [Notion Mail](https://www.notion.com/help/notion-mail-inbox-is-going-away-what-to-do-next): launch attention without durable primary-inbox adoption
- [ ] [Newton Mail](https://newtonhq.com/blogs): shutdowns, relaunches, pricing, and the acquisition cost of damaged trust

## Additional checks

When relevant, research may benefit from:

- **Wayback Machine** for historical positioning, pricing, and funnel changes.
- **Official ad libraries**, especially Google and LinkedIn.
- **Dealroom, Crunchbase, and founder statements** to verify funding status.
- **Manual landing-page and funnel inspection**, which remains indispensable.
