# Superhuman Mail and Spark Mail performance distribution

Captured: **2026-07-21**

This is the current, publicly verifiable infrastructure through which another
company, publisher, creator, customer, store, or marketplace can bring
Superhuman Mail or Spark Mail users in exchange for a commission, platform
share, reseller margin, or customer discount. Private contracts and affiliate
dashboards are not visible.

## Answer

**Superhuman has the broader partner-acquisition system:** Impact, Dub,
creator affiliates, customer referrals, founder and SaaS perk marketplaces,
Brex, startup partners, enterprise resellers, and AWS Marketplace.

**Spark has fewer channels, but the clearest pay-on-real-use model:** Setapp
pays Spark only from paid members who use Spark. Apple and Google take their
share only when a subscription is purchased through their stores.

For a strict “pay only after gaining a real client” test:

- **Clear matches:** Spark through Setapp, Apple, and Google; Superhuman through
  enterprise resellers and AWS Marketplace.
- **Affiliate infrastructure confirmed, payout trigger private:** Superhuman
  through Impact and Dub.
- **Signup/redemption-linked rather than paid-client-linked:** Superhuman's
  creator deals, FounderPass, Secret, Brex, startup program, and customer
  referrals.

## Current channels

| Company | Channel | Public economics | Verdict |
| --- | --- | --- | --- |
| Superhuman | [Impact](https://help.superhuman.com/hc/en-us/articles/46210168100493-Coda-s-affiliate-program-moves-to-Grammarly) | Superhuman confirms that affiliates can earn from Superhuman Mail. A live [Tool Finder link](https://toolfinder.com/go/superhuman) routes through Impact and carries publisher, offer, and promo identifiers into signup. | Active cash affiliate channel. Rate, payout event, attribution window, and refund clawback are private. |
| Superhuman | [Dub Partners](https://dub.co/blog/network-referral-bonus) | Dub says its partners have driven revenue and earned commissions from companies including Superhuman. Superhuman appears in Dub's [customer directory](https://dub.co/customers) and has a login-gated [marketplace program](https://partners.dub.co/programs/marketplace/superhuman). | Active affiliate infrastructure; exact terms and its division of work with Impact are private. |
| Superhuman | [Efficient App](https://efficient.app/deals/superhuman) | New users receive two months free through a tracked link and `Efficient2`. Efficient says it receives a small affiliate commission for traffic from its videos, reviews, and comparisons. | Clearest named creator affiliate. Efficient says a later free-to-paid upgrade usually does not trigger the offer, so this is not proven pay-after-payment. |
| Superhuman | [FounderPass](https://www.founderpass.com/partners/superhuman-mail) | New customers receive one month free through a partner link. FounderPass says it may earn commission when the offer is redeemed. | Active founder-perk marketplace; public trigger is redemption, not retention. |
| Superhuman | [Secret](https://www.joinsecret.com/superhuman) | New users receive the first month of Starter or Business free through a designated partner link. | Active SaaS-deal marketplace. Fees and post-free-month conversion are private. |
| Superhuman | [Brex perks](https://superhuman.com/products/mail/brex-bundle) | Brex customers receive 50% off Business for the first year. | Active partner perk. The discount is visible; any Brex commission is private. |
| Superhuman | [Superhuman for Startups](https://help.superhuman.com/hc/en-us/articles/46185445904781-Superhuman-Mail-for-Startups) | Approved VCs, accelerators, and incubators introduce eligible startups, which receive Business free for 12 months for up to five people. | Active, discount-funded partner acquisition; the startup is initially free and no partner commission is disclosed. |
| Superhuman | [Customer referrals](https://help.superhuman.com/hc/en-us/articles/46005742648077-Account-Structure) | When a first-time user joins through a personal referral link, both people receive one month free. The [“Sent via Superhuman” signature](https://new.superhuman.com/two-ways-to-get-superhuman-for-free%21-265980) also distributes referrals. | Active product loop; reward follows signup, not a proven paid client. |
| Superhuman | [Superhuman Alliance](https://superhuman.com/partners) | Resellers and solution providers sell Enterprise with deal protection, rewards, and a private margin model. The [partner FAQ](https://cdn.allbound.com/grammarly-ab/2026/02/17222305/Superhuman-Mail-Partner-FAQ.pdf) limits this motion to Enterprise. | Sale-linked channel and a strict match; exact margin is private. |
| Superhuman | [AWS Marketplace](https://aws.amazon.com/marketplace/pp/prodview-r7e62ikdwulig) | Enterprise buyers purchase through AWS billing; a public 12-month, 100-seat contract is listed. | Transaction-linked procurement channel; AWS fees are private. |
| Spark | [Setapp](https://setapp.com/apps/spark-mail) | Setapp distributes 70% of paid membership revenue among developers whose apps the member opened during the billing period. Trial use earns nothing. Spark Plus is included. | Strongest pay-on-real-use match. See [Setapp's revenue rules](https://docs.setapp.com/docs/setapp-membership-revenue). |
| Spark | Setapp [affiliates](https://setapp.com/affiliate-program), indirectly | Setapp advertises $25 per new paid member. A live [Tool Finder Spark link](https://toolfinder.com/go/spark-mail) routes through Setapp's Impact program to Spark's Setapp listing. | Proven creator → Setapp affiliate → paid member → Spark usage path. Setapp, not Spark, pays the affiliate. |
| Spark | Apple App Store and Mac App Store | Apple handles subscriptions started on iPhone, iPad, or the Mac App Store build. | Transaction-linked store distribution; exact applicable commission is not inferred. |
| Spark | Google Play | Google handles subscriptions started on Android. | Transaction-linked store distribution; exact applicable commission is not inferred. Spark documents both routes in its [billing guide](https://sparkmailapp.com/help/billing-subscription/personal-subscription). |

Spark also publishes through Microsoft Store and Huawei AppGallery, but Spark
says Huawei and desktop payments use Stripe. They are discovery/download
surfaces, not verified store-commission acquisition channels.

No public Spark-specific affiliate program, rewarded customer referral,
creator commission, cashback offer, or live deal marketplace was found.

## Influencers and podcasts

- **Superhuman:** Efficient App is a confirmed creator affiliate. Tool Finder
  is a confirmed Impact publisher. Dub supplies a broader affiliate, creator,
  and publisher network, but its active roster is private.
- **Spark:** Tool Finder promotes Spark indirectly through Setapp's affiliate
  program. No direct Spark creator-affiliate program was verified.
- **Podcasts:** Superhuman loads Podscribe with advertiser ID
  `superhumanmail`, proving podcast attribution capability. It does not reveal
  current shows or whether compensation is CPA, CPM, flat fee, or hybrid.

## Landing and signup evidence

The live pages and rendered signup paths were inspected on 2026-07-21.

### Superhuman

- The Mail landing page loads Impact, Dub, Podscribe, G2 conversion
  attribution, LinkedIn Insight, Reddit Pixel, Google Tag Manager, and
  LaunchDarkly.
- The signup bundle accepts or preserves UTMs, `gclid`, `fbclid`, `msclkid`,
  campaign and ad IDs, Impact's `irpid` and `irgwc`, `dub_id`, `promo_code`,
  referral code, and referrer email.
- The rendered signup path also loads Google Ads/Analytics, Meta, Taboola,
  LinkedIn, Reddit, Podscribe, Oktopost, ZoomInfo, and Qualified.

This corroborates the named affiliate, referral, promo, podcast, review, paid
media, and B2B paths. It does not disclose payout rules, spend, conversions, or
profitability.

### Spark

- The homepage loads GTM, Meta Pixel, Amplitude, and Tailor experimentation.
- The server sets a one-year `spark_conv_r` cookie containing current and
  initial source, medium, and campaign. Spark attaches it to Amplitude events.
- Spark measures free-download, buy-now, plan, billing cadence, and checkout
  actions. Direct desktop purchases route through Stripe.

Spark is attribution-ready from source to checkout, but the captured code
shows no affiliate-specific integration or payout program.

## Not counted

- Spark's [AppSumo page](https://appsumo.com/products/spark-mail/) is a request
  placeholder, not evidence of a completed deal.
- Coupon aggregators, Product Hunt, press, organic reviews, and app directories
  do not prove commercial terms.
- Superhuman's ambassador community discloses perks and advocacy opportunities,
  but no per-client commission.
- G2, Podscribe, Reddit, LinkedIn, Meta, Taboola, Google, Oktopost, ZoomInfo,
  Qualified, Amplitude, and Tailor are measurement or marketing tools. Their
  presence alone does not prove pay-on-client economics.
- No credible current Superhuman or Spark cashback/card-linked offer through
  Rakuten, Honey, Capital One Shopping, Chase, or Amex was found.
