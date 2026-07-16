# Tecotype traffic

Status: Working acquisition model

Last reviewed: 2026-07-16

## Targets

- At least 25 new paid subscribers per week.
- At least 100 new paid subscribers per rolling month.
- €15 per month or €149 per year, with the annual plan as the primary offer.
- 3,000 relevant visitors per day is the current conservative scale target. It
  is derived from the funnel model, not from measured traffic.

## Funnel assumptions

| Scenario | Relevant visitors per purchase | Visitor-to-paid conversion |
| --- | ---: | ---: |
| Optimistic | 300 | 0.33% |
| Working | 500 | 0.20% |
| Pessimistic | 1,000 | 0.10% |

Traffic required:

| Scenario | For 25 purchases per week | For 100 purchases per month |
| --- | ---: | ---: |
| Optimistic | 7,500 | 30,000 |
| Working | 12,500 | 50,000 |
| Pessimistic | 25,000 | 100,000 |

At 3,000 relevant visitors per day, or approximately 90,000 per month:

| Scenario | Purchases per month |
| --- | ---: |
| Optimistic | 300 |
| Working | 180 |
| Pessimistic | 90 |

The model applies to relevant visitors, not arbitrary page views. Relevant
traffic includes people arriving from purchase-adjacent searches, product
demonstrations, reviews, recommendations, and product-specific discussions.
Broad informational traffic may convert at a different rate.

## External conversion reference

ChartMogul's 2026 SaaS Conversion Report analyzed 200 B2B software products.
Its free-trial path shows:

- 4.5% of website visitors starting a trial.
- 8% of trial users becoming paid.
- 3.6 paid customers per 1,000 website visitors, or 0.36%.

The sample is not directly representative of a new consumer or prosumer email
client. It is used only as a directional reference.

## Acquisition economics

```text
customer acquisition cost = visitors per purchase × cost per visitor
```

Gross break-even cost per relevant visitor at the €149 annual price:

| Funnel | Gross break-even cost per visitor |
| --- | ---: |
| One purchase per 300 visitors | €0.50 |
| One purchase per 500 visitors | €0.30 |
| One purchase per 1,000 visitors | €0.149 |

These ceilings exclude VAT, payment fees, refunds, support, infrastructure, and
other operating costs. The sustainable amount is therefore lower.

At one purchase per 500 visitors:

| Cost per visitor | Acquisition cost | Customers funded by €149 gross cash |
| --- | ---: | ---: |
| €0.10 | €50 | 2.98 |
| €0.15 | €75 | 1.99 |
| €0.20 | €100 | 1.49 |
| €0.30 | €150 | 0.99 |

Reinvesting revenue increases growth only when the acquisition cost is below
the available cash per customer.

## Search and content arithmetic

Nobody should be expected to search for `Tecotype` before encountering the
product elsewhere. Initial search traffic would need to come from unbranded,
purchase-adjacent queries.

Publishing two to three articles per week would produce:

| Publishing rate | Pages after one year | Average visits per page required for 90,000 monthly visits |
| --- | ---: | ---: |
| 2 articles per week | 104 | 865 |
| 2.5 articles per week | 130 | 692 |
| 3 articles per week | 156 | 577 |

This calculation assumes all pages contribute equally and are mature. Neither
assumption should be expected in practice.

Relevant external observations:

- Ahrefs reported that 1.74% of newly published pages in its 2025 study reached
  Google's top ten within one year.
- Ahrefs reported in February 2026 that an AI Overview correlated with a 58%
  lower average click-through rate for the top-ranking page in its study.
- Ahrefs estimated Mailbird at 148,500 monthly organic visits in October 2025,
  ranking for approximately 60,000 keywords and linked from approximately 6,400
  websites. These are third-party estimates, not Mailbird analytics.
- YouTube states that growth in views is not correlated with uploading daily or
  weekly and recommends quality over quantity.

There is no evidence that publishing two to three Tecotype articles per week
would produce 90,000 relevant monthly visits.

## Unknowns to measure

- Total monthly search demand for purchase-adjacent Tecotype topics.
- Tecotype's actual visitor-to-paid conversion rate.
- Conversion rates by traffic source.
- Cost per relevant visitor and customer for paid placements.
- The number of visitors who start installation or onboarding.
- Retention and renewal by acquisition source.
- Whether product demonstrations produce qualified traffic.
- Whether external reviews and recommendations produce repeatable purchases.

## References

- [ChartMogul SaaS Conversion Report](https://chartmogul.com/reports/saas-conversion-report/)
- [Ahrefs ranking study](https://ahrefs.com/blog/how-long-does-it-take-to-rank-in-google-and-how-old-are-top-ranking-pages/)
- [Ahrefs AI Overview click-through study](https://ahrefs.com/blog/ai-overviews-reduce-clicks-update/)
- [Ahrefs estimate for Mailbird](https://ahrefs.com/websites/getmailbird.com)
- [YouTube performance FAQ](https://support.google.com/youtubecreatorstudio/answer/141805)

## Related documents

- [Product description](./product.md)
- [Positioning](./positioning.md)
- [Pricing](./pricing.md)
- [Project source](../tecotype)
