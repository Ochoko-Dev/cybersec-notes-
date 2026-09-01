---
tags: [networking, ip-addressing, subnetting, ipv6]
module: Introduction to Networking
---

# IP Addressing & Subnetting

## IP vs MAC (analogy)
- **IPv4 / IPv6** — the postal address and district of the receiver's building
- **MAC address** — the exact floor and apartment number

## Subnet Mask
Splits an IP address into two parts: the **network address** and the **host address**. This lets routers determine whether a destination IP is on the local network or needs to be routed to an external network — this process is called **subnetting**.

## IPv6 Advantages over IPv4
- **Massive address space** — 128-bit addresses (3.4 × 10^38 total), permanently solves IPv4 exhaustion
- **No NAT required** — direct end-to-end connectivity, less latency/router overhead, fewer P2P issues
- **Faster packet routing** — fixed 40-byte headers, no header checksum, faster hardware processing
- **Auto-configuration (SLAAC)** — devices can self-assign IPs without a DHCP server
- **Built-in IPsec** — native end-to-end encryption/authentication support
- **No broadcast traffic** — uses multicast/anycast instead, reducing network noise

## Related
- [[packet-encapsulation]]
- [[ipsec]]