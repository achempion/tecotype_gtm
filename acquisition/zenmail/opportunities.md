# Opportunities for Tecotype

ZenMail is useful as a positioning, trust, and measurement case. It is not a
validated acquisition playbook: public evidence shows activity and a waitlist,
not activated or retained users.

The experiments below respect Tecotype's current product boundary. Split
Inbox, a complete first-run flow, website, licensing/payment, Gmail audit,
signed public distribution, reply threading, and scheduled-compose UI must not
be presented as shipped before they are.

## Immediate research: before public acquisition

### 1. Test calm control against speed

Compare two accurate research messages:

- **Calm control:** “A keyboard-first Mac email client built for calm, clear
  triage.”
- **Concrete capability:** “Find mail the way you remember it, then act
  without leaving the keyboard.”

Use interviews, small prototype sessions, or a research sign-up—not a product
availability claim. Segment Gmail-only users from people who need generic
IMAP.

Success signal:

- a participant can restate the promise accurately;
- the message attracts the intended workflow and provider mix;
- participants choose a concrete task they want to solve.

Do not use clicks alone as evidence.

### 2. Build a public-claim inventory

Before any launch, create one source of truth for:

- supported providers and account types;
- local storage and network behavior;
- credential storage;
- telemetry;
- search behavior;
- sending/reply boundaries;
- macOS requirements;
- installer/signing status;
- pricing and trial state.

Require homepage, metadata, structured data, legal pages, comparisons, and help
content to reference that inventory. ZenMail's Swift/Rust and encryption drift,
along with unsupported size and startup claims, shows why this is an
acquisition control, not editorial polish.

### 3. Validate three search intents, not a content batch

Research:

- `keyboard first email client mac`;
- `gmail and imap email client mac`;
- queries expressing remembered-message retrieval, such as finding an email by
  person, phrase, or approximate memory.

For each, inspect the result-page intent and interview searchers before
publishing. A landing page should demonstrate one shipped behavior with a
reproducible visual. Do not begin with 15 comparison/listicle pages.

## Release gate

Public acquisition should wait until all of these exist:

- usable no-account first run;
- safe Gmail and IMAP account connection;
- public website with accurate platform/provider claims;
- Gmail audit/verification appropriate to requested scopes;
- license and payment behavior for the decided Individual price;
- signed/notarized installer and update path on the initial platform;
- privacy-minimal source handoff;
- chosen activation event;
- reliable connection, initial sync, and error recovery;
- safe send, failure, and recovery paths;
- reply threading and scheduled-compose UI resolved or clearly excluded from
  public claims;
- Split Inbox suitable for any public Split Inbox claim;
- support and legal contact with an identified operator.

The gate protects both conversion and trust. A waitlist can hide product
friction, but it cannot measure first value.

## First public funnel

Use a privacy-minimal sequence:

```text
source-tagged page
→ download
→ first launch
→ provider selected
→ account connected
→ initial sync usable
→ one qualifying action
→ retained return
```

Candidate qualifying actions:

- complete a keyboard triage action;
- retrieve an older message with local search;
- send a new message successfully;
- set a reminder and later return to it.

Choose one primary activation event before launch. Connection alone is setup;
download alone is distribution.

Measure by source:

- page-to-download;
- download-to-first-launch;
- first-launch-to-account-connected;
- connected-to-activation;
- time to activation;
- day-1 and day-7 retained return;
- support/privacy failure reasons.

Avoid sending email addresses or message-derived content to analytics. Use a
short-lived source token and coarse event taxonomy.

## Channel experiments after the gate

### Search: proof-led pages

Publish at most three initial pages:

1. keyboard-first Mac email client;
2. Gmail and IMAP support with an exact compatibility table;
3. local remembered-message search with a short, reproducible demo.

Each page should:

- cite external comparisons;
- state the test environment for performance claims;
- distinguish shipped, beta, and planned behavior;
- link directly to download;
- preserve source through activation;
- be reviewed whenever architecture changes.

Decision rule: continue only if a page produces activated accounts at a
credible rate, not merely impressions.

### Community: transparent workflow help

Run a four-week founder-led test in a small number of relevant Mac/email
threads:

- disclose the relationship;
- answer the problem before mentioning Tecotype;
- link only to a directly relevant proof/demo;
- tag the source;
- record unique independent replies separately from founder activity.

Decision rule: require connected and activated users plus qualitative task fit.
Do not count repeated comments from one account as customer advocacy.

### Launch concentration

Only after the funnel is stable, coordinate one bounded launch around:

- an installable signed build;
- a 30–60 second accurate product demonstration;
- a named operator and support route;
- a privacy explanation matching actual network behavior;
- source-to-activation reporting.

Keep Product Hunt, community, founder audience, and search sources separate so
their effects can be compared.

### Comparisons

Publish a competitor comparison only when:

- the audience repeatedly asks for it;
- every material competitor claim has a current primary source;
- Tecotype's own feature is shipped and reproducible;
- the page names limitations and update date;
- a review owner is assigned.

ZenMail's uncited comparisons and stack drift are the failure mode to avoid.

## What not to copy

- “best,” “fastest,” “most private,” or precise RAM/startup claims without a
  public method;
- an unexplained security badge;
- a large SEO corpus before exact intent and conversion are validated;
- comparison pages without citations;
- many recommendation-shaped comments from one unidentified account;
- email addresses as analytics identities without explicit disclosure;
- crawler allowlists as a success metric;
- inbox-zero counters or gamification simply because ZenMail presents them;
- a waitlist count as product activation;
- Gmail-only positioning if Tecotype's actual value includes IMAP;
- any claim that planned release-gate work already exists.

## Decision table

| Opportunity | Start | Stop or revise |
| --- | --- | --- |
| Calm vs concrete message research | Now | Audience cannot restate the distinction or task fit is weak |
| Claim inventory | Now | Never stop; make it a release control |
| Three-intent search research | Now | SERP intent does not match a product/download page |
| Proof-led SEO pages | After website + distribution + activation | Impressions do not become activated accounts |
| Transparent community participation | After a relevant proof/demo exists | Links create attention but no qualified activation |
| Concentrated public launch | After the full release gate | Onboarding/support is not stable |
| Pricing/trial test | After licensing/payment exists | Do not simulate checkout or price availability |

The strategic distinction is simple: ZenMail demonstrates how to make a sharp
promise and a broad acquisition surface. Tecotype should demonstrate that the
promise, product, privacy model, and downstream measurement all agree.
