---
tags: [linux, network-access-control, dns, interfaces]
module: Linux Fundamentals
---

# Network Configuration & Access Control

## Network Access Control (NAC) Models
- **Discretionary Access Control (DAC)** — the resource owner sets permissions for who can access it.
- **Mandatory Access Control (MAC)** — permissions enforced by the OS, not the owner — more secure, less flexible.
- **Role-Based Access Control (RBAC)** — permissions assigned based on organizational roles, easier to manage at scale.

Tools for monitoring/analyzing network traffic:
- `ss` — socket statistics
- `lsof` — list open files

## Configuring Network Interfaces
`ifconfig` and `ip` configure local network interfaces on Ubuntu:
```
sudo ifconfig eth0 up
sudo ifconfig eth0 192.168.1.2
sudo ifconfig eth0 netmask 255.255.255.0
sudo route add default gw 192.168.1.1 eth0
```
DNS servers translate domain names into IP addresses — proper DNS configuration is crucial for devices to resolve domain names and access networked resources.

## Related
- [[monitoring-troubleshooting]]