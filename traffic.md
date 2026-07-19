# Tecotype traffic

Purpose: acquisition arithmetic, not measured performance.

Last reviewed: 2026-07-19

Thresholds come from the
[acquisition gate](acquisition/readme.md#one-hard-gate); price comes from
[pricing](pricing.md). The commercial win condition is 100 attributable
first-time paid customers. The planning pace is one/week, which reaches 100 in
about 23 months.

## Planning rates

| Case               | Relevant visitor → paid | Visitors/month for one paid/week | Total visitors for 100 paid |
| ------------------ | ----------------------: | --------------------------------: | --------------------------: |
| External reference |                   0.36% |                             1,204 |                      27,778 |
| Working            |                   0.20% |                             2,167 |                      50,000 |
| Pessimistic        |                   0.10% |                             4,333 |                     100,000 |

The 0.36% reference comes from ChartMogul's 2026 B2B SaaS conversion report:
4.5% visitor-to-trial × 8% trial-to-paid. It is directional, not representative
of a new desktop email client.

These rates may reject a route whose traffic is clearly too small. The 0.2%
working rate may pass only pre-launch capacity when paired with observed
traffic from the exact surface, as defined by the
[acquisition gate](acquisition/readme.md#one-hard-gate). It cannot establish an
**Excellent channel** or replace live Tecotype conversion.

“Relevant visitor” means someone arriving from a purchase-adjacent
recommendation, comparison, provider placement, review, or product
demonstration. Broad page views, platform users, keyword volume, backlinks, and
cumulative marketplace counters are not relevant visitors.

## Economics

```text
CAC = total incremental channel cost / attributable new paid users
```

At one new paid customer/week, the channel may spend approximately USD
264/month on average while remaining at the working USD 61 CAC ceiling. Across
100 new paid customers, total incremental channel cost must remain at or below
USD 6,100.

For the independent-reviewer route, the approved working allocation is:

```text
USD 50 first-time annual-customer commission
+ up to USD 11 attribution, payout, administration, and
  channel-specific support
= up to USD 61 incremental CAC
```

The first 20 customers should use manual or checkout-native attribution. This
caps commission exposure at USD 1,000 and preserves approximately USD 220 for
the rest of the channel-specific pilot cost.

For paid traffic:

```text
CAC = cost per click / click-to-paid conversion
```

At the working 0.20% conversion rate, a USD 61 CAC permits at most about USD
0.12 per relevant click. This excludes VAT, payment fees, refunds, support,
infrastructure, and other operating costs.

## Unknowns

- Actual Tecotype visitor-to-paid conversion by source.
- Qualified traffic available from each exact surface.
- Installation, mailbox-ready, and first-value rates.
- Retention, refunds, support burden, and contribution margin by source.
- Whether any current route can produce 100 attributable first-time paid
  customers over an evidenced useful life.
- Whether that route can approach the one-new-paid/week planning benchmark.

## Reference

- [ChartMogul SaaS Conversion Report](https://chartmogul.com/reports/saas-conversion-report/)
