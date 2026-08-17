**Related Notes:** [[Networking-MOC]], [[Full-Data-Flow-Example]] 
---
## Core Mechanics
DNS is the internet's phonebook — resolves a domain name to an IP address.
![DNS hierarchy]
![[Screenshot from 2026-08-17 09-58-15 1.png]]
1. **Local cache check** — browser/OS checks if the IP is already cached.
2. **Recursive DNS server** — if not cached, query goes to a resolver (ISP or public, e.g. `1.1.1.1`, `8.8.8.8`). 
3. **Root server** — points the resolver to the right TLD server. 
4. **TLD name server** (e.g. `.com`, `.org`) — directs to the domain's authoritative server. 
5. **Authoritative name server** — returns the actual IP. 
6. **Response & caching** — resolver caches the result and returns it to your device. 
## Practical Impact / Security Relevance 
Not covered explicitly in today's notes — worth revisiting when DNS spoofing/poisoning comes up in labs.