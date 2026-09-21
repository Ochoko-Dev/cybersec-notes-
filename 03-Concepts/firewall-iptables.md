---
tags: [linux, firewall, iptables, netfilter]
module: Linux Fundamentals
---

# Firewall Setup & iptables

A Linux firewall controls and monitors traffic between network segments to enforce security based on pre-defined criteria.

- **Core purpose** — filters incoming/outgoing traffic by rules, protocols, IPs, and ports to guard against unauthorized access, DoS, port scans, and intrusions.
- **Netfilter** — the kernel component providing hooks to intercept/process network traffic.
- **Evolution** — `iptables` (Linux 2.4 kernel, 2000) replaced older tools like `ipchains`/`ipfwadm` as the de facto standard.

## iptables Components
| Component | Description |
|---|---|
| Tables | Organize and categorize firewall rules |
| Chains | Group a set of rules applied to a specific type of traffic |
| Rules | Define filtering criteria and the action to take on a match |
| Matches | Match specific criteria (source/dest IP, ports, protocols, etc.) |
| Targets | Specify the action on a match (accept, drop, reject, modify) |

## Chains
- **Built-in chains** (per table):
  - `filter` table: `INPUT`, `OUTPUT`, `FORWARD`
  - `nat` table: `PREROUTING`, `POSTROUTING`
  - `mangle` table: `PREROUTING`, `INPUT`, `FORWARD`, `OUTPUT`, `POSTROUTING`
- **User-defined chains** — custom chains to group/streamline rules by specific criteria (e.g. target ports, server roles).

## Related
- [[iptables-reference]] (cheatsheet)
- [[monitoring-troubleshooting]]