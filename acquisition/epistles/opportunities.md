# Epistles-derived opportunities for Tecotype

Research date: **2026-07-17**

These are test designs, not shipped Tecotype capabilities. They are constrained
by the current product truth in [product.md](../../product.md) and the message
boundaries in [positioning.md](../../positioning.md).

## What the evidence supports

Epistles suggests five useful hypotheses:

1. A provider-specific implementation proof earns better questions than a
   generic launch announcement.
2. A free, low-friction download can turn awareness into trial, but install
   breadth says nothing about activation or retention.
3. A small branded community can accelerate issue discovery and repairs while
   also exposing instability.
4. One precise alternative page can rank before a broad SEO inventory gains
   traction.
5. Security documentation is part of acquisition for a mail client; internal
   contradictions can negate feature novelty.

It does **not** establish that eight-platform distribution, a $35 annual
price, a lifetime counter, Reddit cross-posting, or 12 comparison pages are
profitable.

## Current release boundary

Tecotype remains under active development. Before any public download or paid
acquisition test, the release gate should include:

- a coherent first-run/no-account state;
- an accurate public site;
- licensing and payment;
- completion of the Gmail restricted-API/audit path;
- signed, notarized, updateable distribution;
- safe, predictable send behavior;
- release-accurate privacy and security claims; and
- source-to-activation measurement with a documented privacy boundary.

Until that gate is met, research may validate problems and language. It should
not invite people into an unfinished product or imply availability.

## Experiment 1: provider-and-job interviews

**When:** before the release gate.

**Question:** Which combination of account provider and daily job creates
enough friction for a Mac user to consider switching clients?

Recruit three small groups:

- Gmail plus one IMAP account;
- several Gmail/Google Workspace accounts; and
- an IMAP-heavy group using Apple Mail, Thunderbird, or another Mac client.

Ask each participant to reconstruct the last time they:

- searched for mail from partial memory;
- processed a busy inbox from the keyboard;
- switched accounts or providers to finish one task; and
- distrusted a client because its data path was unclear.

Capture the trigger, existing workaround, frequency, cost of failure, current
client, provider mix, and exact words used. Do not demo planned features as
working.

**Decision rule:** proceed only if at least 5 of 8–10 interviews describe the
same frequent job and at least 3 have recently tried to solve it.

## Experiment 2: one source-tagged community invitation

**When:** after the release gate.

**Question:** Can one precise, working claim create retained use from the
community that experiences the problem?

Choose one message supported by the release, such as:

- Gmail plus IMAP in one Mac client;
- find a message from remembered meaning; or
- calm keyboard triage for a real inbox.

Publish one transparent invitation in one relevant community. Disclose
affiliation, current platform, provider scope, price, privacy boundary, and
known limitations. Use a durable source ID through landing, download, and
first run.

Measure:

```text
qualified landing session
→ download
→ installation
→ first launch
→ account connected
→ first completed sync
→ message-matched first-value action
→ voluntary day-1 and day-7 return
→ paid conversion
```

**Decision rule:** do not repeat or broaden the channel unless at least three
non-team users complete the first-value action and at least two return on day
7. A vote, comment, or download alone does not pass.

## Experiment 3: one honest switching page

**When:** after release accuracy and support readiness.

**Question:** Can a narrow comparison page attract a user who is already
choosing?

The best Epistles search result is its Mimestream alternative page, not its
general category pages. A Tecotype test could address Mimestream only if it:

- accurately states Mimestream's current Gmail specialization;
- accurately states only the provider and Mac scope actually shipped at that
  future release point;
- avoids invented weaknesses or generic feature grids;
- distinguishes current product from roadmap; and
- uses a source token through activation and payment.

Primary success is a retained or paid user attributed to the page. Secondary
signals are qualified query impressions and organic click-through.

**Stop rule:** retire or revise after enough impressions to evaluate the title
and message if it produces no first-value users. Do not expand into 12
thin alternative pages from one rank.

## Experiment 4: executable trust page

**When:** before public acquisition.

**Question:** Can every sensitive claim be traced to current behavior, policy,
and an owner?

Create a claim ledger with:

| Claim | Product behavior | Policy / terms | Verification | Owner |
| --- | --- | --- | --- | --- |
| Mail storage boundary | Current implementation | Privacy page | Network/storage test | Engineering |
| Gmail data use | Current scopes and processing | Google disclosure | OAuth and audit artifacts | Engineering/legal |
| Analytics | Exact events and identifiers | Privacy page | Build and network inspection | Product |
| License/refund terms | Payment behavior | Terms | Checkout/refund test | Operations |
| Platform availability | Signed current build | Download page | Clean-machine install/update test | Release |

Block publication when any row disagrees. Epistles shows why prose volume is
not a substitute for consistency.

## Experiment 5: calm public repair loop

**When:** after launch.

**Question:** Can public support improve trust without turning the feed into an
unbounded promise surface?

Use one public changelog and one issue-intake path. For every material report,
record:

- affected released version;
- reproducible boundary;
- severity;
- current workaround, if safe;
- fixed version only after distribution is verified; and
- whether the acquisition claim that exposed the issue must be paused.

Measure median time to acknowledgement, verified fix, and repeat report—not
the number of posts. Pause the associated campaign for send, sync, data-loss,
authentication, or privacy failures.

## Economics guardrail

Tecotype's current acquisition model requires roughly **€0.149–€0.50 of
allowable pre-cost spend per relevant visitor**, depending on conversion
assumptions. Epistles' public $35 annual price and lifetime offer do not change
that model because its traffic, conversion, retention, refunds, and costs are
unknown.

For every post or page, retain:

- production time;
- distribution or ad cost;
- relevant sessions;
- first-value users;
- day-7 retained users;
- paid customers;
- net cash after tax/refund/fees where available; and
- support burden.

Scale only on retained-customer economics.

## Actions to avoid

- Do not match eight-platform breadth before the Mac product is reliable.
- Do not reactively match a competitor's low price without retention and cost
  evidence.
- Do not use a waitlist count, store band, lifetime counter, votes, or version
  count as product-market-fit proof.
- Do not say “local” or “private” more broadly than the actual data path.
- Do not publish source-release, refund, or continuity promises that are
  absent from the governing terms and operating plan.
- Do not seed apparently independent recommendations.
- Do not market future MCP support or other roadmap work as shipped.

## Recommended order

1. Complete the release and trust gates.
2. Run the provider-and-job interviews in parallel with that work, without
   offering access.
3. Launch one source-tagged community test.
4. Keep only the message that produces first value and voluntary return.
5. Turn that proven job into one accurate switching/search page.
6. Expand a channel only after retained-customer economics support it.

The evidence behind these choices is summarized in
[readme.md](./readme.md) and audited in [requests.md](./requests.md).
