**Related Notes:** [[Networking-MOC]]
---
## Overview
The network topology space splits into three areas:
1. **Connections** - Wired: coaxial cabling, glass fiber cabling, twisted-pair cabling. - Wireless: Wi-Fi, cellular, satellite.
2. **Nodes** — Network Interface Controllers (NICs), repeaters, hubs, bridges, switches, routers/modems, gateways, firewalls.
3. **Classifications** — 8 basic types, covered below.
---
## Point-to-Point
A direct, straightforward physical link exists only between two hosts.
## Bus
All hosts connect via a shared transmission medium (e.g. coaxial cable). Every host has access to the medium and the signals on it. No central network component controls the process. Since the medium is shared, only one host can send at a time — all others can only receive and check whether the data is meant for them.
![[Screenshot from 2026-08-18 10-54-31.png]]
## Star
A central network component (usually a router, hub, or switch) maintains a connection to all hosts — each host connects to it via a separate link. The central component handles forwarding: receiving data packets and forwarding them to their destination. Data traffic through the central component can be very high, since all data and connections pass through it.
![[Screenshot from 2026-08-18 10-55-32.png]]
## Ring 
**Physical ring:** each host connects with two cables — one for incoming signals, one for outgoing. Typically doesn't require an active network component; access to the medium is regulated by a protocol all stations adhere to.
**Logical ring:** based on a physical star topology, where a distributor at the node simulates the ring by forwarding from one port to the next. Information transmits in a predetermined direction, typically accessed sequentially station to station using a **token** — a bit pattern that continually passes through the ring in one direction, per the **claim token process**. 
![[Screenshot from 2026-08-18 10-56-22.png]]
## Mesh
Devices (nodes) connect directly to one another without relying solely on a central switch or hub.
![[Screenshot from 2026-08-18 11-02-48.png]]
## Tree 
An extended star topology used in more extensive local networks — especially useful when combining several topologies. Common in larger company buildings. Has both logical tree structures (per the **spanning tree** protocol) and physical ones. Modular modern networks, based on structured cabling with a hub hierarchy, also follow a tree structure. Also used for broadband networks and city networks (**MAN**).
![[Screenshot from 2026-08-18 11-03-53.png]]
## Hybrid 
Combines two or more topologies so the resulting network doesn't present a standard topology. Example: a tree network can be a hybrid if star networks are connected via interconnected bus networks. Note: a tree network linked to another tree network is still topologically a tree network — a hybrid is created specifically when **two different** basic topologies are interconnected.
![[Screenshot from 2026-08-18 11-04-24.png]]
## Daisy Chain
Multiple hosts connect by running a cable from one node to the next, forming a chain. Multiple hardware components connect in series. Often found in automation technology (**CAN**). Based on the physical arrangement of nodes, in contrast to token procedures, which are structural but can be made independent of physical layout. The signal travels to and from a component via its previous nodes to the computer system.
![[Screenshot from 2026-08-18 11-05-08.png]]
## Practical Impact / Security Relevance 
Star's central component is a single point of failure/bottleneck — worth flagging when assessing network resilience. Not otherwise covered explicitly in today's notes.