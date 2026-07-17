# Feature requests

Status: Discovery backlog; nothing here is shipped or committed.

Record credible user jobs, merge overlaps, and preserve the fully local mailbox
boundary. Compatibility or partner interest is a hypothesis, not evidence of
user pain.

| Request | Minimum behavior | Discovery hypothesis |
| --- | --- | --- |
| [Durable message links](./experiments/hookmark-message-links.md) | Copy and open an account-scoped `tecotype://` message link, using RFC `Message-ID` when available and resolving locally with a clear missing-message state. | Hookmark and linked task/note workflows |
| [Local integration commands](./experiments/local-automation-commands.md) | Let an authorized local tool discover and invoke stable commands with explicit parameters and deliberate results. Scope and revoke access; expose no credentials or general mailbox browsing; confirm content egress and irreversible actions. Covers task/CRM capture, scheduling links, aliases, timers, archives, attachment uploads, and partner-specific packs across desktop platforms. | Curated partner integrations with permanent discovery |
| [Local mailbox migration audit](./experiments/local-mailbox-migration-audit.md) | Locally compare user-authorized source and target mail and export a read-only exception report without modifying either mailbox. | Repeated migration-completeness evidence; named search demand remains unquantified |
| Local mail-file access | Safely open, search, and export standard mail files and attachments locally, including large archives. | [EML](./experiments/eml-local-viewer.md), [MSG](./experiments/msg-local-viewer.md), and [MBOX](./experiments/mbox-archive-access.md) acquisition paths |
| [Predictable search fallback](./experiments/gmail-search-missing-results.md) | Offer an explicit chronological literal-search path when relevance ranking hides a known message. | Existing Gmail search complaints |
