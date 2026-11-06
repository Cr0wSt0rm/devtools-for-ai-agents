# Privacy Policy: DevTools for AI Agents

**Effective date:** November 6, 2026

DevTools for AI Agents is a free Chrome extension built and supported by an individual developer. It turns AI agent traces you provide into a visual tool-call flow so you can inspect the arguments, results, and timing of a run.

## The short version

- The extension operates locally and does not make external network requests for its own operation, including when importing traces, loading bundled samples, or exporting files.
- It only reads what you explicitly paste, drop, or choose as a local file, or a bundled synthetic sample you load yourself. It does not capture agent traffic or collect logs silently.
- Your traces are stored locally in your browser and nowhere else.
- We do not sell, share, or transfer user data. The extension has no analytics, tracking, advertising identifiers, or remote telemetry.
- There are no paid plans or payment flows in the extension, and no external service is required to use it.

## What the extension accesses

You choose what to import by pasting text, dropping a file, or picking a local file in the side panel. The extension parses that content locally to build the visualization. It does not read your browsing history, page content, or other tabs, and it does not capture live agent traffic.

The extension requests two Chrome permissions:

- `storage`, to remember trace history and the last active run on your device.
- `sidePanel`, to show the visualizer in Chrome's side panel.

The packaged extension does not request host permissions for remote sites.

## Local storage and retention

Imported traces are stored in IndexedDB on your device. The extension keeps up to **50** local traces; when you go past 50, the oldest trace is removed. The last active run id is remembered in `chrome.storage.local` so the current run can be restored when you reopen the side panel.

You can delete individual traces or clear your history in the extension. Uninstalling the extension or clearing its browser storage also removes your locally stored traces.

Stored values are not encrypted by the extension. Treat the device and browser profile as the trust boundary.

## Bundled samples and user logs

Built-in sample traces are synthetic fixtures bundled with the extension. Loading a sample does not fetch a trace from the internet or send your data anywhere. We do not collect real user logs through the extension.

Agent logs can contain prompts, tool arguments, results, credentials, or personal information. Only import data you are allowed to inspect. Do not import secrets that should not be on this device, and check any view or file before sharing it.

## Redaction: best-effort, not a guarantee

Redaction is local. It is **not** complete secret removal and does **not** encrypt stored content.

- **Inspector display redaction defaults on** for recognized sensitive values.
- **JSON and Markdown export redaction defaults on.** When enabled, it targets recognized API keys, Bearer tokens, and JWTs and includes redaction information and scrubbed-field metadata. You can turn export redaction off for data that was not already redacted.
- **Import redaction is optional and off by default.** When enabled, it scrubs those recognized patterns before storing the run.

Not every secret form is recognized. Review the displayed payload and exports yourself before sharing them. The extension also warns that redaction does not completely remove secrets.

## Local exports

At your request, the extension saves files on your device. It never shares exports automatically.

- **JSON + Markdown:** a re-importable `trace.json` and a `bug-report.md`. You can export the whole trace or a selected call. The same default-redacted view is used for both formats. There is no raw stored-run export that bypasses this view.
- **PNG:** a local snapshot of the on-screen graph. Font embedding is skipped and cache-busting is disabled so PNG generation does not re-fetch remote resources.

Imported traces may contain URLs. The extension treats them as data, not instructions to fetch remote resources.

## Support email

Support is handled by email at **agentdevtools@proton.me**, hosted by Proton Mail. Proton encrypts stored mail, and [Proton's privacy policy](https://proton.me/legal/privacy) covers how messages are transmitted and stored. We keep support threads only as long as needed to reply, never use them for marketing, and delete them on request. Please don't send raw traces, keys, or other secrets in a support email.

Email support and visiting this public privacy page are separate from the extension's local operation. Neither is required to use the extension.

## Changes

If this policy changes, the updated version and its effective date will be posted at this same address.

## Contact

Questions about this policy: **agentdevtools@proton.me**
