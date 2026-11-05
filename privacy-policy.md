# Privacy Policy: DevTools for AI Agents

**Effective date:** November 5, 2026

DevTools for AI Agents is a Chrome extension built and supported by an individual developer. It turns AI agent traces you provide into a visual tool-call flow so you can see the arguments your agent actually sent.

## The short version

- The free version makes no network requests. Nothing leaves your machine on free.
- The extension only reads what you explicitly paste or drop into it. It never collects logs silently.
- Your traces are stored locally in your browser and nowhere else.
- We do not sell, share, or transfer user data, and we do not use analytics or tracking.

## What the extension accesses

You choose what to import by pasting text or dropping a file into the side panel. The extension parses that content locally to build the visualization. It does not read your browsing history, page content, or other tabs.

The extension requests two Chrome permissions:

- `storage`, to keep your trace history and settings on your device.
- `sidePanel`, to show the visualizer in Chrome's side panel.

## Local storage and retention

Imported traces are stored in your browser's local storage (IndexedDB) on your device. The free version keeps up to **50** traces of history; when you go past 50, the oldest trace is removed. You can delete traces at any time, and uninstalling the extension or clearing your browser's site data removes them.

PNG and JSON exports are files saved to your device at your request. The extension never shares them automatically.

Agent logs can contain prompts, tool arguments, results, credentials, or personal information. Only import data you are allowed to inspect, and review exports before sharing them. Local processing does not redact or encrypt content for you.

## Sample logs and consent

We never collect real user logs. The built-in "Load sample" traces are synthetic. If we ever ask for sample logs to improve parsers, we will ask you first, explain what we need and why, and only use what you choose to send after you agree.

## Pro features

Pro ($9/month or $49 one-time) adds features such as cost dashboards, reports, and unlimited history. Any future Pro feature that sends data off your device, such as cloud sharing, will be opt-in, and this policy will be updated before it launches to describe exactly what is sent, where, and for how long. The free version will stay network-free.

## Support email

Support is handled by email at **agentdevtools@proton.me**, hosted by Proton Mail. Proton encrypts stored mail, and [Proton's privacy policy](https://proton.me/legal/privacy) covers how messages are transmitted and stored. We keep support threads only as long as needed to reply, never use them for marketing, and delete them on request. Please don't send raw traces, keys, or other secrets in a support email.

## Changes

If this policy changes, the updated version and its effective date will be posted at this same address.

## Contact

Questions about this policy: **agentdevtools@proton.me**
