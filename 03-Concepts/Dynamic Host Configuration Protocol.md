**Related Notes:** [[Networking-MOC]], [[NAT]], [[Full-Data-Flow-Example]] 
--- 
## Core Mechanics 
Network management protocol that automatically assigns each device on a network a unique IP address, preventing conflicts and duplicate addresses.
> [!tip] DORA
>  > 1. **Discover** — device broadcasts a DHCP Discover to find available DHCP servers. 
>  > 2. **Offer** — a DHCP server responds with a DHCP Offer, proposing an IP lease. 
>  > 3. **Request** — client replies with a DHCP Request, accepting the offered IP.
>  > 4. **Acknowledge** — server sends a DHCP Acknowledge, confirming the assignment.
## Practical Impact / Security Relevance 
Not covered explicitly in today's notes — revisit once a lab surfaces the security angle (e.g. rogue DHCP scenarios).