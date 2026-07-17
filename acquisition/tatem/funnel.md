# Public funnel

Tatem did not have one stable acquisition funnel. The product, message, access model, and price changed repeatedly. These periodized funnels must not be combined into one synthetic cohort.

## Funnel by period

### 2022–May 2023: legacy operations and project management

```text
Operations, task-management, review, founder, or partner discovery
→ tatem.com
→ free signup, demo, or early-access CTA depending on the date
→ app.tatem.com
→ project-management use
```

This funnel produced legacy Wefunder, G2, Capterra, podcast, and backlink artifacts. It is not evidence about email acquisition. See [history.md](./history.md).

### August 2023–early 2025: email waitlist

```text
Community recommendation, founder response, gallery, or unknown source
→ “Smart email built for speed”
→ request-access form
→ waitlist
→ planned referral-led or high-touch access
→ activation and payment unknown
```

The [archived September 2023 pricing page](https://web.archive.org/web/20230929230840/https://tatem.com/pricing) displayed Free, Plus, and Pro tiers, but every plan still led to request access. The public flow therefore established price intent, not a completed purchase.

In community discussions, Tatem’s founder described expanding access starting with referrals from existing users. That is evidence of a stated plan; it does not prove the referral program’s scale or operation.

### May–June 2025: rebuilt product and paid workspace

Tatem’s [May 2025 announcement](https://tatem.com/changelog/2025-05-14-a-new-beginning) said the product, codebase, infrastructure, ways of working, and website had been rebuilt from the ground up.

The [June team update](https://tatem.com/changelog/2025-06-20-invite-your-team) documented:

```text
Create or join workspace
→ invite teammates
→ Stripe billing
```

This proves that a paid team flow was shipped according to Tatem. It reveals no conversion or revenue.

### July 2025: self-serve early access

The [July announcement](https://tatem.com/changelog/2025-07-01-early-access-begins) removed scheduled calls and 1:1 onboarding:

```text
Homepage
→ Get started
→ Google signup
→ self-serve setup
```

The change reduced visible access friction. Its effect on activation remains unknown.

### September 2025 onward: free base product

The [September pricing update](https://tatem.com/changelog/2025-09-08-updated-pricing) changed the base product to free forever with no card and deferred the paid Tatem+ plan:

```text
Homepage
→ Get started
→ Continue with Google
→ free product
→ no current public payment step
```

The [current pricing page](https://tatem.com/pricing) shows:

| Plan | Price | Availability |
| --- | ---: | --- |
| Tatem | $0 per member per month | Free forever |
| Tatem+ | $10 per member per month, billed annually | “Coming soon” |

The live [terms](https://tatem.com/terms) still contain older language implying payment and no free plan. The newer pricing page and September announcement are stronger evidence for the current offer.

## Current public path

Observed on 2026-07-17:

1. The homepage shows “Now in early access,” “Join 10,000+,” and “Get started.”
2. Every primary CTA points to `https://app.tatem.com/sign-up`.
3. The signup page shows “Continue with Google,” terms/privacy links, and a sign-in alternative.
4. No email input or other account method was visible.
5. Signup-page scripts load Segment-hosted Amplitude integration code.

Not observed:

- The post-Google authorization sequence.
- Gmail synchronization completion.
- An internal activation event.
- Retention or active-user state.
- A current checkout.

Tatem’s [privacy policy](https://tatem.com/privacy) describes access to Google profile data and Gmail, contacts, and calendar. It does not reveal completion rates.

## Community response to funnel friction

The email waitlist created both interest and visible trust costs:

- In an [August 2024 Superhuman pricing thread](https://www.reddit.com/r/SuperhumanEmail/comments/1f2w0wx/leaving_superhuman_after_recent_price_increaes/), some participants said they joined the waitlist.
- The same thread includes reports of waiting a long time, stale public releases, and doubts that access would arrive. Tatem’s founder later replied with the rebuilt product and self-serve announcement.
- A [Superhuman lifetime-access thread](https://www.reddit.com/r/SuperhumanEmail/comments/151fpqb/superhuman_lifetime_subscription/) includes reports of six-to-seven-month waits and lack of onboarding.

These are qualitative reports, not a measured abandonment or churn rate. They do establish that collecting interest without timely access damaged trust among some commenters and prospects.

## Affiliate path

The current [affiliate page](https://tatem.com/affiliate) promises recurring income but says more details are coming and captures interest. It is a planned funnel, not evidence of an operating partner program.

## Potential Tecotype transition path

Tatem’s audience could be tested without transferring the underlying list:

```text
Tatem Inc. or Wander confirms communication rights
→ current rights holder sends an accurate introduction
→ recipient explicitly opts in to Tecotype
→ Tecotype release path
→ chosen activation event
```

Tatem’s [privacy policy](https://tatem.com/privacy) says it does not sell personal information, requires consent for marketing to non-account holders, and permits certain information transfers during a company or asset transaction subject to notice and continuing policy promises. It also places tighter boundaries around Google user data.

Consequently, a Tatem-sent opt-in campaign is a more defensible experiment than purchasing or importing a contact list. No Gmail content, Google authorization token, contact, calendar, or other product data should be part of the campaign. Ownership, consent, and territorial requirements require verification before launch. See [outreach.md](./outreach.md).

## What can and cannot be learned

Observed:

- Waitlist, high-touch access, planned referral-led expansion, paid team billing, self-serve access, and free access were all tried or announced at different times.
- The funnel became easier to enter over time.
- Paid access was replaced by a free base offer.

Unobservable:

- Why the product was rebuilt.
- Why pricing or access changed.
- Source-to-signup, source-to-activation, retention, or payment rates.
- Whether any historical funnel was economically productive.
