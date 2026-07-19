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
| Capacity        | Observed monthly unique views and comparable client-choice clicks on the exact host surface support 10 paid users/month at the 0.2% working rate, or at a current observed Tecotype conversion rate from a tightly matched audience. Fleet totals and invented traffic guesses do not pass. Do not add weak routes together. |
| Paid bridge     | Current evidence from the exact or a tightly matched acquisition audience shows the same person continues into a recurring full-client job and pays for, or actively evaluates, comparable clients near Tecotype's price. Plausible adjacency is not evidence.                                                               |
| Economics       | The complete channel-specific cost can remain below USD 50 incremental CAC.                                                                                                                                                                                                                                                  |
| Privacy         | Mailbox credentials, content, addresses, domains, messages, queries, and derived mailbox data do not enter acquisition systems.                                                                                                                                                                                              |
| Product control | Tecotype keeps its normal signed application, licensing, release policy, and updater. No partner SDK, repackaging, or managed desktop build is required.                                                                                                                                                                     |

If any requirement is unknown, the route is **Parked**, not an experiment.
Modeled assumptions may reject a route. The defined 0.2% working rate may pass
only pre-launch capacity when exact surface traffic is observed; it cannot
establish an **Excellent channel**.

Use only four statuses:

- **Parked:** at least one hard gate is still unknown.
- **Rejected:** a hard gate failed and no current fact can repair it.
- **Experiment:** all pre-launch gates pass and a bounded live test is defined.
- **Excellent channel:** a live route sustains at least 10 attributable new paid
  users/month on a rolling three-month average, incremental CAC remains below
  USD 50, at least 60% remain paid at 90 days or first renewal, and the privacy
  and updater boundaries remain intact.

“Distribution” is narrower: a partner must introduce zero-existing-user
prospects through permanent pre-install discovery and an attributable
first-use-to-paid path. Tecotype currently has no qualified distribution.

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
payment from product usefulness.

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
