---
tags: [networking, proxies]
module: Introduction to Networking
---

# Proxies

**Gateway vs Proxy:** a proxy can inspect the contents of the traffic. Proxies operate at **Layer 7** (Application layer).

## Proxy Types
- Dedicated / Forward proxy
- Reverse proxy
- (Non-)Transparent proxy

## Forward Proxy
A forward proxy sits between a client and the destination — the client sends a request to the proxy, and the proxy carries it out on the client's behalf. It filters **outgoing** requests.

Example: in a corporate network, sensitive machines may not have direct internet access. To reach a website they must go through a proxy (web filter) — a strong line of defense against malware. DNS activity in this setup can be monitored with **Sysmon**.

Burp Suite is a good example of a proxy — though it can also be configured to run as a reverse or transparent proxy.

## Reverse Proxy
A reverse proxy filters **incoming** requests. It listens on a public-facing address and forwards traffic to a closed-off internal network.

Many organizations use **Cloudflare** for this, since it has a network robust enough to withstand most DDoS attacks.

> ⚠️ If an attacker gains SSH access to the organization, a reverse proxy set up over that SSH tunnel can be used to send web requests and evade the IDS.

Examples: Cloudflare, ModSecurity

![[Pasted image 20260901111117.png]]

## Transparent Proxy
With a transparent proxy, the client doesn't know it exists. The proxy intercepts the client's requests to the internet and substitutes itself as the communication partner — to the outside world it behaves like a non-transparent proxy would.

## Related
- [[wifi-security]]
- [[ipsec]]