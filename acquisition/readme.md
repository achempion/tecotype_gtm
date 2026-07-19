# Acquisition research

Purpose: canonical acquisition method and decision gate.

This directory contains competitor and channel research. It does not define
the product, price, or current acquisition decision:

- [Product](../product.md) owns product facts.
- [Positioning](../positioning.md) owns the message.
- [Pricing](../pricing.md) owns the €15/month and €149/year decision.
- [Current acquisition decision](../next-acquisition-funnel.md) owns the active
  channel verdict.

## One hard gate

A route is an acquisition experiment only when every requirement passes:

| Requirement     | Pass condition                                                                                                                                                                                                                                                                                                               |
| --------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Exact discovery | A person with no Tecotype history encounters Tecotype on a named, host-controlled surface before installation. A possible listing or generic audience does not count.                                                                                                                                                        |
| Capacity        | Observed unique views and comparable client-choice clicks on the exact host surface support 100 attributable first-time paid customers over an evidenced useful life. Roughly one/week is the planning benchmark, not a second hard gate. The 0.2% working rate may be used before launch; use observed Tecotype conversion after launch. Fleet totals and invented traffic guesses do not pass. Do not add weak routes together. |
| Paid bridge     | Current evidence from the exact or a tightly matched acquisition audience shows the same person continues into a recurring full-client job and pays for, or actively evaluates, comparable clients near Tecotype's price. Plausible adjacency is not evidence.                                                               |
| Economics       | The complete channel-specific cost can remain at or below USD 61 incremental CAC. This is the whole channel allowance, not the commission alone.                                                                                                                                                                               |
| Privacy         | Mailbox credentials, content, addresses, domains, messages, queries, and derived mailbox data do not enter acquisition systems.                                                                                                                                                                                              |
| Product control | Tecotype keeps its two standard products: the Mac App Store build and the website-licensed direct desktop builds. No partner SDK, reviewer-specific binary, repackaging, or managed desktop build is required.                                                                                                                        |

If any requirement is unknown, the route is **Parked**, not an experiment.
Modeled assumptions may reject a route. The defined 0.2% working rate may pass
only pre-launch capacity when exact surface traffic is observed; it cannot
establish an **Excellent channel**.

Use only four statuses:

- **Parked:** at least one hard gate is still unknown.
- **Rejected:** a hard gate failed and no current fact can repair it.
- **Experiment:** all pre-launch gates pass and a bounded live test is defined.
- **Excellent channel:** a live route produces 100 attributable first-time paid
  customers, incremental CAC remains at or below USD 61, and the privacy and
  updater boundaries remain intact. Report 90-day or first-renewal retention
  separately; at least 60% is the continuation-health target. Roughly one paid
  customer/week is the planning pace, not an additional success requirement.

For the independent-reviewer route, the approved offer is USD 50 per
attributable first-time annual customer after the refund window. That leaves an
average of up to USD 11 per customer for channel-specific attribution, payout,
administration, and support. A monthly subscriber earns commission only as
revenue is collected, never USD 50 against the first EUR 15 payment, and total
commission remains capped at USD 50.

For a Mac App Store annual customer using a creator-specific paid offer code,
the commission is 40% of the paid first-year customer price after the refund
window, capped at USD 50. Apple offer-code reporting is the attribution source.
For a website customer, use an explicit checkout referral code. Neither path
requires third-party advertising cookies or a consent-banner tracking system.

“Distribution” is narrower: a partner must introduce zero-existing-user
prospects through permanent pre-install discovery and an attributable
first-use-to-paid path. An integration install by an existing Tecotype customer
is activation or retention, not acquisition. Marketplace install totals count
only when the host separates first-time Tecotype discovery from customers who
arrived to connect a product they already use. Tecotype currently has no
qualified distribution.

The only current status table and exact next fact request are in the
[current acquisition decision](../next-acquisition-funnel.md). Confirmed pain
evidence is in
[confirmed-pain-opportunities.md](../confirmed-pain-opportunities.md).

## Research workflow

For each candidate:

1. Identify the exact discovery surface and the zero-user path to Tecotype.
2. Inspect the public offer, CTA, installation path, activation, and price.
3. Find observed traffic or partner data. Label modeled numbers as assumptions.
4. Find current evidence that the same person would buy a comparable full
   client near Tecotype's price.
5. Apply the hard gate before proposing product work.
6. Record a clear verdict and the single missing fact that could change it.

Never infer traffic from a backlink, marketplace audience, cumulative install
counter, page-view total, keyword volume, or platform user count. Never infer
new-user acquisition from integration connections. Never infer payment from
product usefulness, a trial, or a deal-claim counter.

Use [DataForSEO](../tools/dataforseo.md) only after public research produces a
specific query hypothesis. Search volume can reject a channel on capacity; it
does not prove pain, conversion, or willingness to pay.

## Research archive

Completed competitor work remains in the individual directories. Cross-client
summaries:

- [Wave 1](./wave-1.md): emerging direct competitors.
- [Wave 2](./wave-2.md): established clients and visible acquisition surfaces.
- [Wave 3](./wave-3.md): emerging signals, failures, and adjacent models.

The sealed customer-pain evidence and audit trails are under:

- [Initial discovery ledger](../tmp/pain-discovery/registry.md)
- [Second-pass ledger](../tmp/pain-discovery-next/registry.md)
- [Outlook audit](../tmp/pain-discovery/audit-msg-search.md)
- [Superhuman audit](../tmp/pain-discovery-next/audit-unified-inbox.md)
- [Reply-aware audit](../tmp/pain-discovery-next/audit-reply-aware.md)
