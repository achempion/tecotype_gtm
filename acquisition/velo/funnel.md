# Public funnel

Research date: **2026-07-17**

No Velo binary was downloaded, installed, or launched. No account was created, mailbox connected, Google Cloud project configured, OAuth flow begun, form submitted, trial started, or purchase made. This reconstruction uses public pages, source, documentation, manifests, workflow logs, release metadata, and third-party discussion.

## Observable acquisition path

```text
founder post, community discussion, video, article, backlink, or search
→ velomail.app
→ “Download for Free”
→ generic GitHub releases page
→ user identifies a release and platform asset
→ asset request
→ install and operating-system trust checks
→ Gmail custom-OAuth setup or IMAP/SMTP credential setup
→ mailbox connection and initial sync
→ first meaningful email action
→ repeat use or contribution
```

Only the path through the asset request is publicly countable, and even that counter is not unique or source-attributed. Everything from successful installation onward is unknown.

## Stage audit

| Stage | Public evidence | Friction | Measurement status |
| --- | --- | --- | --- |
| Discovery | Social posts, GitHub, branded search, small publications, package/community links | Story often concerns AI development more than email need | Public counters only |
| Landing | Clear free/open-source hero and three platform claims | Broad promise and absolute privacy language | No recognizable product analytics/source tags |
| CTA | Every prominent download CTA opens GitHub releases | No platform preselection or message continuity | CTA clicks unknown |
| Asset selection | Multiple current Windows, macOS, and Linux assets | Developer-oriented filenames and release history | GitHub request counter only |
| Install | Public packages exist | Current macOS artifact was uploaded unsigned | Completion unknown |
| Update | Updater exists in source | Configured latest manifest returned `404` | Working update adoption unknown |
| Gmail setup | README documents PKCE and no client secret | User must configure a Google Cloud project and APIs | Start/completion unknown |
| IMAP setup | README documents auto-discovery plus manual fallback | Provider passwords/app passwords and server details may be required | Start/completion unknown |
| AI setup | User supplies a provider API key | Separate provider account/cost/privacy relationship | Use and value unknown |
| First value | Many candidate actions exist | No declared activation event | Unknown |
| Retention | Desktop client can sync and work locally according to source | Reliability and support quality untested | Unknown |
| Revenue | Free Apache-2.0 offer | No commercial conversion path | Not applicable publicly |

## Landing to release page

The homepage’s header and hero download actions both target:

`https://github.com/avihaymenahem/velo/releases`

The GitHub-oriented secondary action targets the repository root. No visible link carries:

- source or campaign;
- hero-message variant;
- detected platform;
- target release;
- intended asset;
- referral identity.

The current homepage therefore cannot publicly distinguish a Reddit visitor from a search visitor or a Windows prospect from a macOS prospect.

## Current release handoff

The latest release is [`velo-v0.4.21`](https://github.com/avihaymenahem/velo/releases/tag/velo-v0.4.21), published 2026-02-27. Its release note describes improved IMAP sync error handling and reliability.

It exposes nine assets, including:

- macOS universal DMG and app archive;
- Windows setup executable and MSI;
- Debian, AppImage, Flatpak, and RPM variants.

The release had 1,088 aggregate asset requests at the research snapshot. This is not a count of people reaching the next stage.

## Distribution trust boundary

### macOS signing and notarization

The public [workflow run for the current release](https://github.com/avihaymenahem/velo/actions/runs/22496174782) is decisive:

| Workflow step | Result |
| --- | --- |
| Check if Apple signing is configured | Success |
| Import Apple signing certificate | Skipped |
| Build/upload signed + notarized | Skipped |
| Build/release signed + notarized | Skipped |
| Build and upload unsigned | Success |

Velo’s automation supports a signed path conditionally, but the latest macOS artifact did not use it. No binary inspection was performed.

Earlier release notes explicitly called several macOS builds unsigned and suggested `xattr -cr /Applications/Velo.app`. The principal Reddit thread contains a “damaged and can’t be opened” report for v0.1.0. The comment cannot establish a general failure rate; the current workflow does establish current signing status.

### Update channel

The current Tauri manifest configures:

`https://github.com/avihaymenahem/velo/releases/latest/download/latest.json`

A metadata-only request on 2026-07-17 followed the redirect to `velo-v0.4.21` and returned **404**. The release asset list also lacked `latest.json`.

Source includes update-check logic and workflow signing variables, but the public latest-release endpoint did not supply its required manifest. A source-level updater is not the same as a working, safe update channel.

## Account connection

### Gmail

Velo does not require a Velo account or retain a client secret. Its README nevertheless instructs a Gmail user to:

1. create Google Cloud OAuth credentials;
2. enable Gmail API and Calendar API;
3. enter the resulting client ID in Velo settings;
4. complete the provider authorization flow.

This likely filters for technically confident users. It is also a major discontinuity from “ready in two minutes.” No account connection was attempted.

Two post-release main-branch commits dated 2026-03-12 include a fix binding the OAuth callback server to `127.0.0.1` and a sync-status UX improvement. They are after the latest release and therefore must not be presented as packaged in `0.4.21`.

### IMAP/SMTP

The README says users can add an IMAP account with an email address and password, with automatic server discovery for common providers and manual server entry as fallback. Public source and releases show substantial IMAP implementation and repair work.

No provider was connected. Auto-discovery coverage, credential acceptance, sync time, sent-mail behavior, and provider-specific reliability remain unknown.

## AI activation and privacy

AI is optional. The user must bring an Anthropic, OpenAI, Google Gemini, GitHub Models, or compatible local-provider credential/configuration.

The public security model says cloud requests go directly to the chosen provider, not through Velo servers. That lowers one intermediary risk but creates a separate external-provider flow. Any AI activation event must record only safe, non-content metadata and distinguish:

- fully on-device/local-model use;
- direct cloud-provider use;
- AI disabled.

The landing page currently blurs these cases with “Your data never leaves your machine.”

## Product and business conversion

Observed:

- price is `0 USD`;
- license is Apache 2.0;
- no Velo account is described;
- no trial, license key, checkout, subscription, or donation CTA appears on the current page;
- no purchase path was tested because none was observed.

The current public funnel is adoption/contribution oriented, not a revenue funnel. Velo therefore cannot directly validate Tecotype’s intended paid conversion.

## Instrumentation audit

The inspected homepage HTML and bundle contained no recognizable:

- Google Analytics or Tag Manager;
- PostHog;
- Segment;
- Mixpanel;
- Amplitude;
- source-preserving redirect;
- experiment assignment;
- email capture.

Velo’s first-party security documentation also says “No telemetry, analytics, or tracking.” Server/CDN logs and conditional behavior are unknown.

This is a coherent privacy choice, but it means public acquisition claims cannot be joined to product outcomes.

## A defensible activation definition

For a product like Velo, “download” is too early. A useful non-content activation sequence would be:

```text
landing CTA
→ correct signed artifact
→ verified first launch
→ provider setup started
→ provider setup completed
→ initial sync completed
→ first user-initiated useful action
→ second active day
→ seventh active day
```

Possible first useful actions include:

- search finds and opens a target message;
- keyboard triage completes a small inbox batch;
- reply is safely sent;
- reminder/snooze is created and later resolved.

The event design must avoid message content, addresses, subjects, or tokens. Source, landing variant, platform, build, provider type, and coarse step result are sufficient for acquisition diagnosis.

## Funnel conclusion

Velo removed a Velo-specific account and purchase step but left substantial distribution and provider-setup friction. Its public system is optimized for inspectability and developer attention, not observable activation. For Tecotype, signed distribution, safe setup, truthful data-flow copy, and source-to-first-value measurement belong inside the release gate.
