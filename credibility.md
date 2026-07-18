# Tecotype credibility

Status: Working strategy. No external review, certification, endorsement,
coverage, or distribution relationship is currently confirmed.

Last reviewed: 2026-07-18

## Goal

Tecotype cannot make a new-vendor claim trustworthy by repeating it.
Credibility should come from independent parties that control their own
conclusions and from evidence a prospective user can inspect.

The priority sequence is:

```text
accurate released product
→ platform and authorization verification
→ public data-flow and security boundaries
→ provider confirmation
→ independent security assessment
→ sustained reviewer and customer use
```

This supports the existing position rather than replacing it. Calm remains the
emotional differentiation; keyboard speed and Better search demonstrate value;
external evidence makes the local-first and privacy foundations believable.

## Current claim boundary

- The GTM evidence does not yet establish a public Tecotype release.
- Gmail, IMAP, local search, Better search, storage, encryption, platforms, and
  resource claims must be checked against the released build before use.
- Mail still travels through the user's email provider.
- Credentials have operating-system-backed protection.
- [Database encryption](../tecotype/architecture/database-encryption.md) is a
  proposed release requirement, not current public proof.
- No platform, assessor, provider, publication, or customer currently endorses
  Tecotype unless a later artifact explicitly establishes it.

See [positioning.md](./positioning.md) for the complete marketing boundary.

## Priority trust channels

| Channel | What to obtain | Credibility value |
| --- | --- | --- |
| Platform verification | Signed and notarized releases; Google restricted-scope verification; public version, checksum, requirements, updates, and release notes | Required baseline |
| Independent security assessment | Named assessor, published scope, tested version, findings, fixes, and retest | High |
| Email-provider trust | Provider-tested connection facts and, separately, a provider-controlled recommendation or permanent link | Very high at mailbox authorization |
| Independent editorial review | Sustained use with no payment for the conclusion and no copy approval | High |
| Named customer evidence | Specific role, workflow, duration, outcome, limitation, and disclosed relationship | High after real use |
| Ongoing operational proof | Security contact, disclosure policy, changelog, supported versions, corrections, and incident history | Required over time |
| Sponsorship or paid listing | Disclosed audience access | Reach, not independent trust |

### Platform verification

Before asking a public evaluator or customer to connect a mailbox or pay:

- sign and notarize the complete release;
- complete Google's applicable OAuth verification and any assigned assessment;
- publish the current version, checksum, requirements, release notes, update
  path, and support contact; and
- consider an App Defense Alliance
  [DASA desktop assessment](https://www.appdefensealliance.org/standards/dasa)
  once the release candidate is stable.

Use exact language. Apple notarization, Google verification, CASA, and DASA are
bounded checks, not endorsements or guarantees of product security.

### Independent security assessment

The first source-assisted macOS assessment should cover:

1. Electron renderer, preload, IPC, navigation, and native N-API boundaries.
2. Untrusted email HTML, remote content, links, inline images, and attachments.
3. OAuth, credential storage, IMAP/SMTP TLS, and endpoint validation.
4. Database encryption, keys, WAL, caches, exports, logs, and failure behavior.
5. Signing, packaging, notarization, updates, diagnostics, and data deletion.

Possible assessors:

- [Doyensec](https://doyensec.com/services/electronjs-based-applications.html),
  for direct Electron expertise.
- [Cure53](https://cure53.de/), for architecture, application, cryptography,
  and public-report experience.
- [7ASecurity](https://7asecurity.com/mobile-app-pentest), for desktop testing
  and code audits.
- [NCC Group](https://www.nccgroup.com/technical-assurance/application-security/code-review/),
  when a larger institutional assurance signal is justified.

Working budgets, not vendor quotes:

| Engagement | Budget |
| --- | ---: |
| Architecture and threat-model review | €4,000–€8,000 |
| Focused macOS assessment with retest | €15,000–€30,000 |
| Deep multi-platform assessment | €40,000+ |

Require a named team, source-assisted testing, one retest, and the right to
publish a substantive report. Do not market an automated scan as an audit.

### Email-provider trust

Ask one shortlisted provider to:

- test an ordinary production mailbox in the released client;
- verify endpoints, authentication, folders, aliases, sending, limitations,
  and support ownership;
- permit only the agreed name and logo use; and
- if comfortable, publish its own recommendation or permanent Tecotype link.

Runbox is the clearest candidate for an existing client-discovery surface; Nubo
is the values-led pilot; Migadu has strong overlap with developers and
multi-account operators. These remain research candidates.

Provider-confirmed facts are not a provider endorsement. A link becomes
distribution only when it creates permanent provider-controlled pre-install
discovery and an attributable first-action-to-paid funnel. See
[distribution/partnerships.md](./distribution/partnerships.md).

### Independent reviews and communities

Give reviewers the normal signed product, exact price and requirements,
data-flow and security documentation, known limitations, enough time for real
use, and freedom to criticize or decline coverage. Do not request copy
approval.

Priority candidates:

| Candidate | Fit |
| --- | --- |
| [MacStories](https://www.macstories.net/about/) | Independent Apple app reviews; reviews are not for sale |
| [TidBITS](https://tidbits.com/) and [Six Colors](https://sixcolors.com/) | Careful Mac coverage and long-use product opinions |
| [MacSparky](https://www.macsparky.com/about/) and Mac Power Users | Apple productivity, automation, and professional workflows |
| [Tool Finder](https://toolfinder.com/about) | Hands-on productivity and email-software comparisons |
| [Techlore](https://techlore.tech/) | Privacy scrutiny after the threat model and assessment are public |
| [Privacy Guides](https://www.privacyguides.org/en/about/criteria/) | Disclosed community evaluation after documentation, audit, cross-platform, and source decisions |

Hacker News, Product Hunt, `r/macapps`, provider forums, and privacy communities
can create discussion, not endorsement. Use only a small number of relevant
surfaces and disclose the founder relationship.

Mimestream's transferable pattern was repeated specialist use, precise
technical proof, and stable positioning rather than one badge. See
[acquisition/mimestream/readme.md](./acquisition/mimestream/readme.md).

### Customer and operational proof

Prefer a few named customer stories over undefined user totals. With permission,
state the role, workflow, length of use, specific outcome, remaining limitation,
and whether access was free, paid, advisory, or compensated.

Maintain:

- a security contact and `security.txt`;
- responsible-disclosure and safe-harbor policies;
- versioned security and privacy documentation;
- a changelog and supported-version policy; and
- visible corrections and material incident history.

Do not turn testers, waitlist members, downloads, connected mailboxes, or
historical trials into customers.

## Recommended sequence

1. Freeze a claim-to-evidence ledger and publish accurate data-flow and threat
   boundaries.
2. Complete release signing, notarization, updates, Google verification, and
   customer support paths.
3. Run one provider-confirmation pilot.
4. Commission one focused security assessment and publish the remediated result.
5. Give a small number of specialist reviewers enough time for real use.
6. Add named customer evidence after sustained use.
7. Add paid reach only after source-to-retained-paid measurement works.
8. Repeat platform-specific validation before Windows or Linux claims.

If only one material external credibility budget is available, prefer the
focused security assessment over creator sponsorship. If the release candidate
is not stable, commission the smaller architecture review first.

## Measurement

Measure each source through the decision it is meant to support:

```text
external source
→ signed download
→ successful mailbox authorization
→ first keyboard or search job
→ voluntary return
→ paid
→ retained paid milestone
```

Use only privacy-minimal source and coarse product events. Never send mailbox
content, address, domain, credentials, server hostname, search query, or
message-derived categories to marketing analytics.

## Claim rules

- State the exact version, date, scope, relationship, compensation, and
  limitation beside external proof.
- Obtain quote and logo permission.
- Link to the original external artifact.
- Remove or update stale proof.
- Never say “certified secure,” “unhackable,” “Apple approved,” “Google
  approved,” or “official provider client.”
- Never call an automated scan, self-assessment, private checklist, or unlinked
  badge an independent audit.
- Never present paid access, affiliate relationships, or sponsorship as an
  independent recommendation.
- Never present future review, certification, platform, provider, or
  integration work as current.

## Related documents

- [Product description](./product.md)
- [Positioning](./positioning.md)
- [Provider endorsements and distribution](./distribution/partnerships.md)
- [Mimestream acquisition report](./acquisition/mimestream/readme.md)
- [Database encryption architecture](../tecotype/architecture/database-encryption.md)
