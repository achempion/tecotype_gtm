# Confirmed customer-pain evidence

Purpose: evidence archive, not a current channel decision or product
commitment.

Research date: 2026-07-19

## Evidence summary

Three narrow pains passed the evidence gate. None produced an
**Experiment**.

| Pain                                                              | Evidence                                                                                                                                                 | Acquisition verdict                                                                                |
| ----------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- |
| Classic Outlook omits a known locally present message from search | Five current authors with the same narrow failure and repeated repair or switching behavior                                                              | **Rejected:** 90 modeled US searches/month and modeled paid-search CAC of USD 208–375              |
| Superhuman separates active accounts into tabs                    | Five cap-compliant authors plus Superhuman's official workaround; behavior includes repeated checking, missed mail, payment, cancellation, and switching | **Rejected:** 40 modeled US searches/month and modeled paid-search CAC above USD 4,200             |
| Reply-aware follow-up                                             | Seven authors across five operated domains and four source types                                                                                         | **Rejected:** Spark Free already completes the job and no distinct same-user paid bridge was found |

Provider and CRM-marketplace placement are separate channel hypotheses, not
confirmed pains. Neither currently qualifies as acquisition. See
[next-acquisition-funnel.md](next-acquisition-funnel.md).

## Classic Outlook omits a known locally present message

The confirmed unit is deliberately narrow:

> A self-managed Classic Outlook user on Windows knows a message exists in a
> local PST or OST, but body, sender, or subject search remains incomplete
> after the applicable Microsoft scope and indexing checks.

Evidence:

| Source                                                                                                                                                     | Observed behavior                                                                                                              |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------ |
| [Microsoft Tech Community](https://techcommunity.microsoft.com/discussions/outlookgeneral/outlook-search-not-returning-results-from-body-of-email/4466377) | Two distinct authors report body-search omission; one repeats large rebuilds after reinstalling Windows and replacing storage. |
| [Microsoft Q&A](https://learn.microsoft.com/en-us/answers/questions/5616891/classic-outlook-search-not-working-for-html-format)                            | HTML and rich-text bodies are omitted while plain text and subjects work; rebuilds fail and Safe Mode changes the result.      |
| [Reddit: incomplete result counts](https://www.reddit.com/r/Outlook/comments/1na53vy/outlook_search_completely_broken_on_current/)                         | Another machine finds 103 matches where the affected machine returns 11; profiles, reinstalls, and repeated rebuilds fail.     |
| [Reddit: imported stores work elsewhere](https://www.reddit.com/r/Outlook/comments/1sodkzh/should_i_just_give_up_on_outlook/)                              | After extensive repair work, Outlook finds headers but not bodies; eM Client indexes the same stores.                          |

Important counterevidence:

- Microsoft's [troubleshooting path](https://support.microsoft.com/en-US/Outlook/troubleshooting-outlook-search-issues)
  resolves some broad Outlook-search complaints.
- Supported New Outlook configurations can
  [open and search PST content](https://support.microsoft.com/en-US/Outlook/open-and-find-items-in-an-outlook-data-file-pst).
- [MailStore Home](https://www.mailstore.com/en/products/mailstore-home/),
  [DocFetcher](https://sourceforge.net/projects/docfetcher/), and
  [eM Client](https://www.emclient.com/licensing?lang=en) are strong free or
  broader-client alternatives.

DataForSEO modeled `outlook search not finding emails` at 90 US searches/month
and USD 0.75 CPC. At the 0.2% working and 0.36% external visitor-to-paid
references:

- expected purchases are only 0.18–0.32/month at full search capture; and
- media CAC is approximately USD 208–375.

That fails both the one-new-paid/week capacity gate and the USD 61 CAC gate.
The pain is real; paid search is not a viable primary channel.

Full evidence: [Outlook audit](tmp/pain-discovery/audit-msg-search.md).

## Superhuman separates active accounts into tabs

The confirmed unit is:

> A Superhuman user with several active accounts must cycle account tabs to
> see and process all mail, creating repeated checking and missed-message risk.

Evidence:

| Source                                                                                                                                                     | Observed behavior                                                                                      |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------ |
| [Reddit: nine client accounts and paid three-account user](https://www.reddit.com/r/SuperhumanEmail/comments/1io7tcf/no_unified_inbox_how_do_you_survive/) | Two authors describe repeated tab cycling, missed messages, feature requests, and likely churn.        |
| [Reddit: executive with many accounts](https://www.reddit.com/r/SuperhumanEmail/comments/1htix3s/do_i_just_not_get_it/)                                    | The user pays for a month, compares the workflow with unified clients, cancels, and receives a refund. |
| [Capterra review](https://www.capterra.com/p/199278/Superhuman/)                                                                                           | A long-term user identifies cost and the missing unified inbox as material limitations.                |
| [App Store review](https://apps.apple.com/us/app/superhuman-mail/id1120837655?platform=iphone&see-all=reviews)                                             | A two-provider evaluator reports the same missing all-account view.                                    |
| [Superhuman workaround](https://help.superhuman.com/hc/en-us/articles/46005722297229-Unified-Inbox-Workaround)                                             | Superhuman documents a workaround rather than a true unified inbox.                                    |

[Spark](https://sparkmailapp.com/pricing) and
[Mailspring](https://www.getmailspring.com/) provide actionable unified inboxes
for free, weakening both differentiation and a paid bridge.

DataForSEO modeled `superhuman unified inbox` at 40 US searches/month and USD
15.19 CPC. At 0.2%–0.36% visitor-to-paid:

- expected purchases are only 0.08–0.14/month at full search capture; and
- media CAC is approximately USD 4,219–7,595.

Paid search is disqualified on capacity and cost.

Full evidence: [Superhuman audit](tmp/pain-discovery-next/audit-unified-inbox.md).

## Reply-aware follow-up

Seven cap-compliant authors confirmed the same conditional reminder job:
surface a sent message if no reply arrives by a chosen time.

This remains **Rejected** because:

- Spark Free already performs the complete job;
- no distinct paid Tecotype job was evidenced for the same person; and
- existing marketplace inventory does not establish Tecotype placement,
  traffic, or discovery.

Full evidence: [reply-aware audit](tmp/pain-discovery-next/audit-reply-aware.md).

## Research and product boundary

- Pain confirmation required five independent authors with the same actor,
  trigger, job, and failure mechanism, plus behavioral response and
  counterevidence.
- Search volume, CPC, platform audiences, cumulative views, and cumulative
  installs are discovery inputs, not traffic or customer counts.
- At research time, a public Apple Silicon macOS 0.5.1 artifact was verified;
  public Windows and Linux artifacts were not. Cross-platform readiness is a
  GTM planning premise, not a public-availability claim.
- PST/OST ingestion, MBOX/EML import, all named integrations, provider
  placement, permanent-free entitlements, end-to-end attribution, and partner
  agreements remain proposed.
- Product and privacy claims remain governed by [product.md](product.md) and
  [positioning.md](positioning.md).

## Research record

Detailed observations and exclusions remain in:

- [Initial discovery ledger](tmp/pain-discovery/registry.md)
- [Second-pass ledger](tmp/pain-discovery-next/registry.md)
- [Initial synthesis](tmp/pain-discovery/synthesis.md)

DataForSEO task creation was the only external write. Cumulative enumerated
spend through the acquisition decision was **USD 0.48776**; the conservative
maximum is **USD 0.48976**.
