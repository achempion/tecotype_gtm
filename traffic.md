# Tecotype traffic

Purpose: acquisition arithmetic, not measured performance.

Last reviewed: 2026-07-19

Thresholds come from the
[acquisition gate](acquisition/readme.md#one-hard-gate); price comes from
[pricing](pricing.md). The calculations below use 10 paid users/month for one
channel and 100 paid users/month for portfolio planning.

## Planning rates

| Case               | Relevant visitor → paid | Visitors for 10 paid/month | Visitors for 100 paid/month |
| ------------------ | ----------------------: | -------------------------: | --------------------------: |
| External reference |                   0.36% |                      2,778 |                      27,778 |
| Working            |                   0.20% |                      5,000 |                      50,000 |
| Pessimistic        |                   0.10% |                     10,000 |                     100,000 |

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

At 10 new paid users/month, the channel may spend less than USD 500/month to
remain below the USD 50 CAC gate.

For paid traffic:

```text
CAC = cost per click / click-to-paid conversion
```

At the working 0.20% conversion rate, a USD 50 CAC permits at most USD 0.10 per
relevant click. This excludes VAT, payment fees, refunds, support,
infrastructure, and other operating costs.

## Unknowns

- Actual Tecotype visitor-to-paid conversion by source.
- Qualified traffic available from each exact surface.
- Installation, mailbox-ready, and first-value rates.
- Retention, refunds, support burden, and contribution margin by source.
- Whether any current route can sustain 10 new paid users/month.

## Reference

- [ChartMogul SaaS Conversion Report](https://chartmogul.com/reports/saas-conversion-report/)
