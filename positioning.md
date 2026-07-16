# Tecotype positioning

Status: Working positioning hypothesis

Last reviewed: 2026-07-16

This document turns the Better search design report into positioning guidance
for the broader product. It describes the current hypothesis, not a permanent
decision. Customer research should determine whether the audience, category,
and lead promise are correct.

## Positioning summary

### Category

Keyboard-first desktop email client.

### Primary audience

Email-heavy professionals who value speed, focus, and control. The initial
audience likely includes founders, developers, consultants, and other
independent operators who:

- Work from email throughout the day.
- Prefer keyboard-driven software.
- Manage confidential correspondence.
- Use several email accounts or providers.
- Search imperfectly, often from a vague memory of a message.
- Work across languages or unreliable network connections.

This audience overlaps with Superhuman's, but the emotional promise is
different.

### Customer situation

Email pulls attention in too many directions. Existing clients either feel
slow and cluttered or turn productivity into another source of pressure.
Intelligent features often require sending private correspondence to another
cloud service.

Tecotype should not dramatize this problem in public copy. Positioning should
show the relief and let people recognize the problem themselves.

### Competitive alternatives

- Default provider clients such as Gmail and Outlook.
- Premium keyboard-first clients such as Superhuman.
- General-purpose clients with cloud-hosted AI features.
- Personal systems built from labels, filters, reminders, and separate search
  tools.

### Unique point of view

Email software should create composure.

Speed should feel immediate without becoming a performance contest.
Intelligent features should be useful without becoming a permanent assistant.
The interface should state what matters, offer the next action, and step back.

### Positioning statement

For professionals who spend much of their day in email, Tecotype is the calm,
keyboard-first email client that makes mail fast to process, easy to find, and
precise to organize. Unlike clients built around urgency, decoration, or
cloud-dependent intelligence, Tecotype combines a restrained interface with
local-first operation and optional on-device search.

### Brand promise

Calm control over your mail.

## Strategic thesis

Three qualities support the product, but they do not have equal positioning
roles:

1. Speed is expected. Keyboard-first interaction proves the product is serious.
2. Privacy is structural. Local processing makes the product trustworthy.
3. Calm is the emotional differentiation. It determines how the product feels.

Marketing should not lead with a checklist of speed, privacy, and AI features.
It should lead with the experience of composure and use concrete product
behavior as proof.

## Message hierarchy

### 1. Calm control

Tecotype helps people move through mail without pulling their attention in more
directions.

Proof:

- Minimal, text-led interface.
- No attention-seeking decoration or gamification.
- Clear actions and pressure-free exits.
- Predictable, reversible workflows where possible.

### 2. Keyboard speed

Frequent work stays close to the keyboard without hiding the application behind
memorized shortcuts.

Proof:

- Direct shortcuts for navigation, search, compose, and triage.
- A command palette for discovery and less frequent actions.
- Dense thread lists and split-pane workflows.
- Local storage that keeps the interface responsive.

### 3. Find mail naturally

People should be able to search using the way they remember a message, even
when their words differ from the original.

Canonical demonstration:

```text
Find mail the way you remember it

"train ticket to copenhagen" finds "Din togbillet til København"
```

Proof:

- Local full-text search.
- Optional meaning-based search.
- Multilingual retrieval.
- Search remains usable without the optional model.

### 4. Private intelligence

Smart features should not require sending mailbox content to an AI service.

Proof:

- Better search runs on the user's device.
- The model download is explicit and optional.
- The product states concrete resource costs before asking.
- Credentials use operating-system-backed protection.

### 5. Precise organization

Users should be able to shape the inbox around their work rather than accept
one fixed provider view.

Proof:

- Unified account views.
- Split Inboxes based on custom rules.
- Reminders that return mail at the appropriate time.
- Local drafts and provider-independent mail workflows.

## Competitive frame

The useful comparison is:

> Similar commitment to keyboard speed, different emotional contract.

Superhuman commonly represents energy, achievement, and performance. Tecotype
should represent composure, restraint, and control.

Do not imitate a louder competitor's register. Claims such as "blazing fast,"
"master your inbox," or "crush email" would weaken the distinction even if they
were technically defensible.

Public copy does not need to name a competitor unless comparison materially
helps the reader make a decision.

## Product description

Tecotype is a keyboard-first desktop email client designed for people who work
from email. It brings Gmail and IMAP accounts into a focused interface for fast
triage, precise organization, and local search. Optional Better search finds
messages by meaning and runs entirely on the user's device.

## Candidate positioning lines

These are hypotheses, not approved taglines:

- The calm email client.
- Your mail, quietly handled.
- Calm control over your mail.
- Find mail the way you remember it.

"Find mail the way you remember it" is shipped product copy and the strongest
current feature-level line. Whether it can carry the whole product position
still needs validation.

## Voice principles

### Demonstrate, do not describe

Use a concrete example instead of adjectives.

- Prefer: `"train ticket to copenhagen" finds "Din togbillet til København"`
- Avoid: "Powerful multilingual AI search understands the meaning of your
  emails."

### Name the benefit, not the technology

The user-facing feature is "Better search," not "semantic search,"
"AI-powered search," or an embedding model.

Technology can appear in technical documentation when it helps someone make an
informed decision. It should not be the product promise.

### Use specifics as reassurance

Concrete facts feel calmer and more trustworthy than vague comfort.

- Prefer: "One-time 318 MB download."
- Avoid: "A small additional download."

Any number must be verified against the current release before publication.

### Put facts in prose and verbs in controls

Body copy states what happened. Buttons provide the next action.

- Prefer: "The download didn't finish." followed by "Try again" and "Later."
- Avoid: "An error occurred. Check your connection and click below to retry."

### Do not poke at pain

Do not dramatize overwhelm or create anxiety to sell relief.

- Avoid: "Drowning in email?"
- Avoid: "Your inbox is stealing hours from your life."

Show the calmer experience instead.

### Always provide a pressure-free exit

Use "Later," not "Skip," "No thanks," or copy designed to make declining feel
like a mistake.

No countdowns, false urgency, or fear of missing out.

## Copy mechanics

- Use sentence case.
- Do not use exclamation marks or superlatives.
- Avoid em dashes. Prefer commas, colons, and periods.
- Headlines act as labels and do not need terminal periods.
- Messages are complete sentences and include periods.
- Use "email" for a countable message and "mail" for the collection.
- Lowercase belongs to human input, ambient statuses, and the `tecotype_` mark.
- Use lowercase, comma-separated status copy when it may be safely ignored:
  `setting up better search, 42%`.
- Use a capitalized sentence when the product needs to be read:
  `Better search is ready.`
- State failures without blame, then offer a way forward.

## Visual positioning

Public-facing design should feel continuous with the product:

- Text on a ground, not collections of cards.
- Whitespace as the primary layout tool.
- Hierarchy through size and muted color.
- One dominant element per view.
- Regular type weight by default.
- Motion only when it communicates state.
- Stable layouts with no decorative movement.
- Icons, illustrations, and charts only when they communicate information that
  words cannot.
- Product screenshots shown with minimal art direction.

The screenshot should often be the advertisement because the product itself
demonstrates the position.

## Claims boundary

Marketing may currently say:

- Keyboard-first desktop email client.
- Supports Gmail and generic IMAP accounts.
- Search and optional Better search run locally.
- Better search is optional.
- Tecotype stores a local working copy of synced mail.
- Split Inboxes, reminders, drafts, and sending are product capabilities.
- The current release is Mac-first.

Marketing should not currently say:

- "Your email never leaves your device." Mail still travels through the user's
  email provider.
- "End-to-end encrypted" or "encrypted mailbox." Credentials are protected, but
  the complete local mail store is not currently marketed as application-level
  encrypted storage.
- "Works fully offline." Be specific about which local operations remain
  available and which require provider synchronization.
- "AI email assistant." The product does not position itself as a chat
  assistant.
- "Automate your inbox with any AI." MCP integration is future work.
- "Available everywhere." Distribution is currently Mac-first.
- Any unverified performance, privacy, or resource claim.

## The never list

- Hype, superlatives, exclamation marks, and emoji in copy.
- Urgency, countdowns, limited offers, and fear of missing out.
- Guilt-based decline actions.
- Technology-first headlines.
- Claims that exaggerate privacy or offline capability.
- Dramatizing the user's anxiety.
- Vague reassurance when a concrete fact is available.
- Decoration that carries no information.
- Copy that sounds generated rather than observed.

## Positioning questions to validate

1. Is calm a reason people would switch and pay, or only an aesthetic
   preference?
2. Which audience feels the problem most strongly: founders, developers,
   consultants, executives, or another group?
3. Is keyboard speed the acquisition hook while calm drives preference and
   retention?
4. Does on-device Better search materially change trust or willingness to pay?
5. Is multilingual retrieval a meaningful segment-level advantage?
6. Do Split Inboxes strengthen the same position or make the product feel too
   technical?
7. Does explicit comparison with Superhuman clarify the product or constrain
   it?
8. Which message best earns a download: calm, speed, search, privacy, or inbox
   control?

## Related documents

- [Product description](./product.md)
- [Project source](../tecotype)
- [Keyboard-first architecture](../tecotype/architecture/keyboard-first.md)
- [Search](../tecotype/architecture/search.md)
- [Better search onboarding](../tecotype/architecture/semantic-search-onboarding.md)
- [Split Inbox](../tecotype/architecture/split-inbox.md)
