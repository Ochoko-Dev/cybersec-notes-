**Related Notes:** [[Networking-MOC]], [[Cloud-Architecture]] 
---
## Core Mechanics
1. **Peer-to-peer (P2P)** — decentralized; every node is both client and server. Files split into pieces, downloaded concurrently from multiple peers (via DHTs/trackers), no central intermediary. Scales naturally as more peers join. Used in BitTorrent, Bitcoin, WebRTC.
2. **Client-server** — centralized; server hosts/manages resources, clients request them (strict request-response). Backbone of most modern internet apps.
3. **Single-tier** — client, server, and database all on one machine. Simple, doesn't scale or secure well.
4. **Two-tier** — client tier (UI + logic) talks directly to a database tier. Fast for small local networks, hard to scale ("thick client").
5. **Three-tier** — adds an application tier between presentation and data tiers. Standard model for web apps. 
6. **N-tier** — three-tier expanded into specialized layers (caching, API gateway, microservices, DB). Max scalability for enterprise systems.
7. **Hybrid** — combines two models, e.g. Client-Server + P2P (centralized auth/discovery, direct peer data transfer) or On-Prem + Cloud (sensitive data stays local, scalable workloads run in the cloud).
## Practical Impact / Security Relevance
Client-server centralizes control, making access control, security enforcement, backups, and updates straightforward — but creates a single point of failure and traffic bottleneck under high load. Hybrid models balance this by keeping sensitive data local while gaining cloud/peer flexibility.