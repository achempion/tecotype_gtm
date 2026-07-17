# Castellum public history

Research date: **2026-07-17**

Scope: **observable changes to the public site, releases, manifests, and legal
pages**

The repository was created on June 29, 2026. Its Git history is therefore more
useful than web archives for this 18-day-old public surface. It shows what
changed, not why it changed or whether a change improved acquisition.

## Timeline

| Time (UTC) | Public change | Acquisition or funnel implication |
| --- | --- | --- |
| 2026-06-29 20:55 | `joanmarcriera/castellum-releases` created | Public site/release container begins; product source remains private |
| 2026-06-29 21:06 | v0.1.0 published | First direct Apple Silicon disk image; release claims signed/notarized build |
| 2026-06-29, initial site history | Landing page uses fortress/manager/local-AI/keyboard/privacy frame and “Free download” | Core positioning was present at first public capture in Git, not added after visible market feedback |
| 2026-06-29 21:54 | v0.1.1 published | Critical packaging fix: v0.1.0 crashed at launch because SQLite native module used the wrong Electron ABI |
| 2026-06-30 07:24 | Homepage adds product screenshot, Ollama steps, FAQ, and “free in early access” | More product proof and setup disclosure; offer changes from generic free download to temporary early-access framing |
| 2026-06-30 08:31 | v0.2.0 published | Adds automatic update checks, sample/connect/skip choices, guided AI setup, and problem reporting |
| 2026-06-30 09:00 | v0.2.1 published | Fixes Gmail token exchange but discloses Google test-user gate |
| 2026-06-30 10:31 | v0.2.2 published | Adds guided configuration for 31 providers and Thunderbird autoconfig fallback |
| 2026-06-30 10:55 | Homepage provider section added | Broadens the visible story from Gmail/local AI to Gmail plus guided IMAP/SMTP breadth |
| 2026-07-17 | Privacy, Terms, and Google Limited-Use pages added | Trust/compliance surface appears; public commit says the pages support Google OAuth verification |

No later binary release was public at capture.

## Release sequence

### v0.1.0: first availability

[v0.1.0](https://github.com/joanmarcriera/castellum-releases/releases/tag/v0.1.0)
described the first public build as signed and notarized. The asset received
three requests.

The next release’s note establishes that the installed build crashed on
launch. No public telemetry shows how many people encountered it or whether
any recovered.

### v0.1.1: emergency packaging repair

[v0.1.1](https://github.com/joanmarcriera/castellum-releases/releases/tag/v0.1.1)
arrived 48 minutes later. It says the packaged SQLite native module had been
built for the wrong Electron version and caused a launch-time ABI error.

This asset received nine requests, the most of any release. That count is
compatible with replacements and retries as well as new interest; it is not
proof that the repair retained nine people.

### v0.2.0: onboarding and updater

[v0.2.0](https://github.com/joanmarcriera/castellum-releases/releases/tag/v0.2.0)
arrived the next morning. Its notes add:

- automatic update checks;
- a choice to explore sample data, connect email, or skip;
- guided local-AI setup;
- `Report a Problem`.

This is the first public updater manifest. The disk image had two requests and
the manifest one at capture.

### v0.2.1: Gmail repair with public-access caveat

[v0.2.1](https://github.com/joanmarcriera/castellum-releases/releases/tag/v0.2.1)
arrived 29 minutes later. It says Gmail’s authorization-code exchange had
failed because the client secret was not included. The fix did not remove the
Google testing-mode restriction: only developer-approved testers could sign
in.

The disk image and manifest each had two and one requests, respectively.

### v0.2.2: provider breadth

[v0.2.2](https://github.com/joanmarcriera/castellum-releases/releases/tag/v0.2.2)
arrived 91 minutes later and remains current. It adds 31 guided provider
setups, including the qualified label “Proton (Bridge),” and a Thunderbird
autoconfig fallback.

The asset had eight requests and its manifest two. No public result ties those
requests to the expanded provider message.

## Landing-message changes

The first public Git version already contained the durable positioning:

```text
manager who runs projects from email
→ fortress/command metaphor
→ local AI
→ keyboard operation
→ data stays local
```

The material changes were proof and offer detail:

- screenshot added;
- Ollama dependency and setup made explicit;
- FAQ added;
- “Free download” changed to “Free in early access”;
- broad provider compatibility added after v0.2.2.

No public A/B framework, campaign tags, or analytics script was visible.
Repository history contains no conversion result. These changes therefore
cannot be labeled winning tests.

## Compliance and commercial preparation

On July 17, one public commit added:

- [Privacy Policy](https://castellummail.com/privacy);
- [Terms](https://castellummail.com/terms);
- [Google API Services Limited-Use disclosure](https://castellummail.com/google-limited-use).

The commit message says the pages were added to support Google OAuth
verification. The terms keep early access free while reserving future paid
licensing. The privacy page describes optional cloud AI and names future
payment/license tooling.

This is evidence of preparation, not:

- completed Google verification;
- a public checkout;
- an active license service;
- a privacy or security audit;
- legal review.

The commit itself says the policy text had no attorney review and was
co-authored with Claude. The dossier treats the pages as the maker’s current
public commitments, not independent assurance.

## Archive result

The Wayback CDX request for `castellummail.com` returned an empty result set.
No successful archived page capture was available.

Consequences:

- there is no independent archived snapshot of the launch page;
- deleted or briefly published variants may be missing;
- current Git history is the best public change ledger found;
- Git history can be rewritten and does not capture non-repository server-side
  behavior.

## What the sequence can and cannot show

It can show:

- the first public binary date;
- release ordering and timing;
- public asset and manifest counts at capture;
- disclosed launch, OAuth, and packaging defects;
- visible page and policy changes.

It cannot show:

- acquisition source;
- unique visitors or installers;
- clean launches;
- mailbox connections;
- feature use;
- why each change was made;
- which message or release retained users;
- whether Google approval later changed without a release note;
- revenue or satisfaction.

## Tecotype interpretation

The useful lesson is operational, not “ship five times in a day.”

- A direct download amplifies packaging errors immediately. Validate the exact
  release candidate through clean first launch before making it public.
- An updater is valuable only after its signed/notarized route and recovery
  behavior are verified end to end.
- Do not let a homepage provider promise get ahead of OAuth approval or
  representative connection testing.
- Preserve an honest release ledger that distinguishes repaired defects from
  new capability.
- Add policy, commercial, and data-flow clarity before inviting a broad
  cohort, not on the day a required provider review needs it.
- Record source-to-activation evidence from the first invited cohort so later
  copy and provider expansion can be evaluated.

Tecotype is under active development. Its release infrastructure being
implemented does not mean the public website, licensing/payment, first-run,
Gmail audit, signed/notarized release candidate, safe-send experience, or
activation measurement has passed its release gate.
