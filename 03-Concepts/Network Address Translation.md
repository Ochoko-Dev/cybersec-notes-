**Related Notes:** [[Networking-MOC]], [[DHCP]], [[Wireless-Networks]], [[Full-Data-Flow-Example]] 
--- 
## Core Mechanics
Allows multiple devices on a private network to share a single public IP address.
- **Public IP** — globally unique, assigned by ISPs, reachable from anywhere on the internet.
- **Private IP** — used within local networks; not routable on the internet.
**How it works:** 
1. Device with a private IP (`192.168.1.15`) sends data to a website.
2. At the router, NAT swaps the private source IP for the router's public IP (`203.0.113.5`) and assigns a temporary port.
3. Router logs the mapping: `[192.168.1.15:5001] <--> [203.0.113.5:5001]`.
4. Response returns to `203.0.113.5:5001` — router checks the table, translates back, forwards to `192.168.1.15`.

**Types:** 
- **Static NAT** — one-to-one private↔public mapping.
- **Dynamic NAT** — public IP pulled from a pool as needed.
- **PAT** — many devices share one public IP via unique source ports (common in home/small office).
-[!warning] Trade-offs 
> - Hosting a public server behind NAT needs extra config (port forwarding).
> - Breaks protocols that need true end-to-end connectivity.
> - Adds troubleshooting complexity. 
## Practical Impact / Security Relevance
Conserves the limited pool of public IP addresses and adds a layer of security to the internal network by hiding private addressing from the outside.