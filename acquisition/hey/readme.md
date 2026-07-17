# HEY acquisition research

Research date: **2026-07-17**

HEY is the clearest Wave 2 example of point-of-view acquisition. Its founders
did not market a faster wrapper around Gmail. They argued that the prevailing
model of email was wrong, named a set of original mechanisms, and asked people
to adopt HEY as their provider. The launch combined 37signals' existing
audience, founder-led explanation, a long product demonstration, Product Hunt,
independent press, and an unusually visible App Store dispute.

The strongest public demand signal is historical and first-party: Jason Fried
told TechCrunch that HEY received **125,000 signups in its first 11 days**.
That is a signup count, not evidence of completed trials, paid subscriptions,
retention, or present growth. The current homepage says “tens of thousands”
have switched, without defining the cohort.

The current conversion offer is unusually low-risk for a paid provider:
**30 days free, no credit card, then $99/year**. The product choice is
high-risk for the user. HEY supplies a new address, does not support IMAP or
POP, cannot import historical mail, and asks the user to learn a different
inbox model. Its migration guide reduces that friction with forwarding,
send-as, and contact-import instructions, but it cannot eliminate it.

## Headline evidence

| Observation | Public evidence | Meaning |
| --- | --- | --- |
| Launch demand | Founder-reported 125,000 signups in 11 days; launch press reported a 50,000-person waitlist | Strong attention and signup evidence; payment and retention remain unknown |
| Current social proof | First-party “tens of thousands” switch claim | Directional only; no date, denominator, or active/paid definition |
| Current personal offer | $99/year; 30-day trial; no card; annual billing only | Trial entry is light, but payment and provider-switch decisions are substantial |
| Modeled US-English search | 4,375 organic keywords and 136,901.58 ETV; no paid keywords | The domain is visible, but the aggregate is badly contaminated |
| Search concentration | The generic word `hey` supplies 81.72% of modeled ETV | Domain totals cannot be read as product demand |
| Relevant pages | Homepage supplies 82.78% of domain ETV; most other high-ETV pages are unrelated HEY World posts | Product and user-publishing visibility are mixed under one domain |
| Backlink index | 92,791 backlinks from 9,367 referring domains | Large footprint, heavily mixed with HEY World and the wider 37signals ecosystem |
| Current category check | HEY was first organic result for `hey email service`, absent from the top 10 for `gmail alternative email service` | Strong brand retrieval, weak evidence for broad category discovery |
| Paid-media check | No paid rankings and no US Google Ads archive result in the requested coverage | No current evidence of search ads; not proof that HEY never advertised |
| DataForSEO spend | $0.157556 | 10 billed tasks; below the $2 per-competitor budget |

The search, backlink, and advertising observations are DataForSEO snapshots.
They are provider estimates and indexes, not HEY analytics. See
[traffic](./traffic.md), [referrals](./referrals.md), and the
[request ledger](./requests.md).

## Acquisition model

```text
37signals and founder audience + launch press + opinionated product story
→ branded discovery, earned coverage, Product Hunt, company cross-promotion
→ HEY homepage / HEY Way / 37-minute walkthrough
→ “we finally fixed your email + calendar”
→ try HEY free
→ create account and choose @hey.com address
→ receive and screen a sender, route mail, experience the new workflow
→ decide whether the provider switch is worth $99/year
```

The public evidence supports the discovery and trial-start portions of that
model. It does not expose source-to-activation attribution, trial completion,
renewal, or customer economics.

## Dossier

- [Landing page](./landing-page.md)
- [Traffic and search](./traffic.md)
- [Referrals and earned distribution](./referrals.md)
- [Offer and funnel](./funnel.md)
- [History](./history.md)
- [Tecotype opportunities](./opportunities.md)
- [Request ledger](./requests.md)

## Research boundary

Research used current public webpages, public search results, rendered-page
inspection, and metadata APIs. No HEY client, installer, or app artifact was
downloaded, fetched, mounted, opened, inspected, installed, or executed. No
account was created, no form was submitted, no trial was started, no mailbox
was authorized, and no payment flow was entered.

## Implications for Tecotype

- **What appears to work for attention and evaluation:** one coherent point of view, concrete product mechanisms, founder credibility, deep demonstration, and a no-card trial made HEY easy to understand and discuss; no public source attributes that discovery through paid conversion.
- **What appears weak, discontinued, or inconclusive:** broad category search is not evidenced, domain-level SEO and backlink totals are inflated by HEY World, and no public data connects the historic signup burst to activation, payment, or renewal.
- **What Tecotype should test:** one calm, mechanism-led release story and one complete demonstration, carried through source-tagged invitation, account connection, first useful action, voluntary return, and payment.
- **What Tecotype should avoid:** manufacturing conflict, copying HEY's combative register, or asking users for a disruptive switch before the signed Mac release and dependable first session are ready.
- **Evidence strength and remaining unknowns:** landing-page, offer, migration, launch, and API evidence is strong; present channel mix, conversion, retention, paid-customer count, acquisition cost, and economics are unobservable.
