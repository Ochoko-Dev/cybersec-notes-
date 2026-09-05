---
tags: [soc, threat-intel]
module: LetsDefend - Introduction to SOC
---

# Threat Intelligence Feed

Data (such as malware hashes, C2 — Command & Control — domain/IP addresses, etc.) provided by a third-party company.

## Common Mistakes Made by SOC Analysts
- **Over-reliance on VirusTotal (VT)** — a clean ("green") VT result alone can miss threats, since newly developed malware using AV-bypass techniques may go undetected. Treat VT as a supporting tool, not a definitive source.
- **Hasty sandbox analysis** — brief sandbox runs (3–4 min) often fail because malware can detect sandboxes and stay dormant, or delay execution by 10–15 min. Extend analysis time and test in real environments when possible.
- **Inadequate log analysis** — investigating an isolated incident isn't enough. When malware connects to a malicious domain, always search central Log Management tools to check if other devices across the network are communicating with the same indicator.
- **Overlooking VirusTotal dates** — VT can display cached historical data for previously searched items. Not checking the scan date risks basing analysis on outdated threat intelligence.

## Related
- [[soar]]
- [[soc-overview]]