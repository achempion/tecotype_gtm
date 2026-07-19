# Tecotype

Status: Working product description

Last reviewed: 2026-07-19

## In one sentence

Tecotype is the calm, keyboard-first desktop email client for professionals who
want to move through mail quickly, find what they remember, and stay in control
of how their inbox works.

## Product description

Email is where a large part of professional work happens. The software around
it should reduce pressure, not add another layer of alerts, achievement, and
attention-seeking interface.

Tecotype brings Gmail and IMAP accounts into one focused desktop client. It is
designed for fast keyboard operation, precise inbox organization, and reliable
local access to mail.

The interface stays restrained. Frequent actions are directly available from
the keyboard. A command palette makes less frequent actions discoverable
without keeping every control visible. The product states what matters, offers
the next action, and steps back.

Search works from a local copy of the mailbox. Optional Better search lets
people find messages using the way they remember them, even when their words or
language differ from the original message. The additional search model runs on
the user's device.

Tecotype is not trying to make email exciting. Its job is to make email feel
handled.

## Product promise

Calm control over your mail.

## The product thesis

Three qualities define Tecotype:

1. Speed is expected. Keyboard-first interaction should feel immediate.
2. Privacy is structural. Mail processing should happen locally whenever
   practical.
3. Calm is the experience. The product should reduce noise, pressure, and
   unnecessary decisions.

No individual feature creates this product. The value comes from these
qualities working together.

## Who it is for

The initial audience hypothesis is professionals who spend a significant part
of the day in email and care about focus, speed, and control.

This likely includes:

- Founders and independent operators managing several kinds of work.
- Developers and other keyboard-oriented professionals.
- Consultants and specialists handling confidential correspondence.
- People working across several email accounts or providers.
- People who regularly need to recover messages from an imperfect memory.
- People working across languages or unreliable network connections.

This audience remains a hypothesis. Customer research should determine which
group experiences the strongest problem and has the clearest reason to switch.

## The job Tecotype does

Tecotype helps a user:

- Move through incoming mail without creating more attention pressure.
- Complete frequent actions without reaching for the mouse.
- Find a message from a partial, approximate, or cross-language memory.
- Separate different kinds of mail without maintaining a maze of provider
  labels.
- Return a thread to the inbox when it becomes relevant.
- Work across several accounts from one consistent interface.
- Draft and process mail even when the network is unreliable.
- Use intelligent features without turning the inbox into a chat assistant.

## The experience

### Quiet by default

The interface is text-led and visually restrained. It avoids decorative panels,
gratuitous motion, and competing calls for attention. Each view should have one
clear purpose.

### Fast without performance theatre

Keyboard navigation, direct commands, dense lists, and local data make work
fast. Tecotype does not turn speed into streaks, scores, celebration, or a
measure of personal achievement.

### Clear without being simplistic

The product can expose powerful behavior, including custom Split Inbox rules,
without making every control permanent. The command palette and contextual
guidance allow depth to remain available without filling the screen.

### Intelligent without becoming intrusive

Better search solves a defined retrieval problem. It does not introduce an
assistant persona or interrupt normal mail workflows. Future intelligent
features should follow the same pattern: narrow purpose, high confidence, and
clear user control.

### Honest about tradeoffs

When a feature requires a download, time, storage, or network access, Tecotype
states the concrete fact before asking. Optional features offer a pressure-free
way to continue later.

## Core capabilities

### Move through mail

- Keyboard navigation through threads and messages.
- Inbox, Archive, Sent, Spam, Trash, and Reminders views.
- Archive, restore, mark read or unread, move, delete, and spam actions.
- Command palette for navigation and contextual actions.
- Split-pane reading and composing workflows.

### Find mail

- Local full-text search.
- Optional on-device Better search.
- Meaning-based and multilingual retrieval.
- Search that remains available when the optional model is not installed.

Canonical demonstration:

```text
Find mail the way you remember it

"train ticket to copenhagen" finds "Din togbillet til København"
```

### Organize the inbox

- Unified views across accounts.
- Account-specific filtering.
- Split Inboxes based on custom rules.
- The option to keep matching mail in Main or separate it.
- Thread reminders that return mail at a chosen time.

### Write and send

- Local drafts that are saved as the user works.
- Compose and reply workflows.
- Gmail and SMTP sending.
- A durable local outbox for queued work.

### Connect existing mail

- Gmail account connection through OAuth.
- Generic IMAP support for other providers.
- Local synchronization and provider-specific adapters behind one interface.

## Product principles

### Calm over engagement

Success is not time spent in the product. The interface should help the user
finish the task and leave.

### Keyboard first, not keyboard only

Frequent actions should be efficient from the keyboard. Mouse interaction
remains available, and commands should be discoverable rather than requiring
the user to memorize the product before benefiting from it.

### Local first

The local database is the application's working state. Reading, searching,
drafting, and supported mutations should remain responsive when connectivity is
slow, then synchronize with the email provider.

### Private by design

Mail content should not be sent to an additional AI or search service when the
work can happen on the user's device. Privacy claims must remain precise:
Tecotype still communicates with the user's email provider.

### Precise and predictable

Commands should produce understandable results. Automation should be
inspectable and reversible where possible. Intelligent behavior should not
silently guess when the user's intent is unclear.

### Facts before reassurance

Concrete information builds trust. State download sizes, progress, limitations,
and failures plainly instead of replacing them with marketing language.

## What Tecotype is not

Tecotype is not:

- An inbox-zero game.
- A productivity score or streak system.
- A chat assistant wrapped around email.
- A cloud AI service that requires uploading the mailbox for basic
  intelligence.
- A team ticketing or sales-operations platform.
- An automation platform that acts without clear user ownership.
- A replacement for the user's email provider.

Future features should not blur these boundaries without an explicit product
decision.

## Current state

Tecotype is under active development. The core desktop client, Gmail and IMAP
integration, local storage, mail synchronization, search, Better search,
reminders, Split Inboxes, drafts, and sending are implemented to varying levels
of completeness.

Important work still includes:

- First-run and no-account onboarding.
- Validation of the audience and positioning.
- The Tecotype account, entitlement service, and payment flows for the decided
  Individual price.
- The public website and acquisition experience.
- Continued compose and sending polish.
- Broader distribution beyond the current Mac-first release.

A local automation command API, MCP integration, broader local intelligence,
and agent-driven automation are future directions. They should not be
presented as current product capabilities.

## Related documents

- [Positioning](./positioning.md)
- [Pricing](./pricing.md)
- [Mac App Store distribution](./mac-app-store-distribution.md)
- [Traffic](./traffic.md)
- [Project source](../tecotype)
- [Technical overview](../tecotype/README.md)
- [Product and release status](../tecotype/architecture/README.md)
- [Keyboard-first architecture](../tecotype/architecture/keyboard-first.md)
- [Search](../tecotype/architecture/search.md)
- [Better search onboarding](../tecotype/architecture/semantic-search-onboarding.md)
- [Split Inbox](../tecotype/architecture/split-inbox.md)
