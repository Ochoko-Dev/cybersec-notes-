---
tags: [cheatsheet, iptables]
module: Linux Fundamentals
---

# iptables Tables, Targets & Matches Cheatsheet

## Tables
| Table | Description | Built-in Chains |
|---|---|---|
| `filter` | Filter traffic by IP, ports, protocols | INPUT, OUTPUT, FORWARD |
| `nat` | Modify source/destination IPs | PREROUTING, POSTROUTING |
| `mangle` | Modify packet header fields | PREROUTING, OUTPUT, INPUT, FORWARD, POSTROUTING |

## Targets
| Target | Description |
|---|---|
| `ACCEPT` | Allows the packet through to its destination |
| `DROP` | Silently blocks the packet |
| `REJECT` | Blocks the packet and sends an error back to the source |
| `LOG` | Logs the packet info to the system log |
| `SNAT` | Modifies source IP (NAT — private → public) |
| `DNAT` | Modifies destination IP (NAT — forwards traffic) |
| `MASQUERADE` | Like SNAT, for dynamic source IPs |
| `REDIRECT` | Redirects packets to another port/IP |
| `MARK` | Adds/modifies the Netfilter mark on a packet |

## Matches
| Match                  | Description                                        |
| ---------------------- | -------------------------------------------------- |
| `-p` / `--protocol`    | Match protocol (tcp, udp, icmp)                    |
| `--dport`              | Match destination port                             |
| `--sport`              | Match source port                                  |
| `-s` / `--source`      | Match source IP                                    |
| `-d` / `--destination` | Match destination IP                               |
| `-m state`             | Match connection state (NEW, ESTABLISHED, RELATED) |
| `-m multiport`         | Match multiple ports/ranges                        |
| `-m tcp` / `-m udp`    | Match protocol-specific options                    |
| `-m string`            | Match packets containing a string                  |
| `-m limit`             | Match at a specified rate limit                    |
| `-m conntrack`         | Match by connection tracking info                  |
| `-m mark`              | Match by Netfilter mark value                      |
| `-m mac`               | Match by MAC address                               |
| `-m iprange`           | Match by IP address range                          |