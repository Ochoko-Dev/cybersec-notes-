**Related Notes:** [[Networking-MOC]], [[Wireless-Networks]] 
---
## Core Mechanics
### Firewalls
1. **Packet filtering** — Layer 3/4; checks IP/port/protocol. E.g. router ACL allowing only 80/443.
2. **Stateful inspection** — tracks connection state. E.g. only allows inbound replies to an established outbound request. 
3. **Application layer (proxy) firewall** — up to Layer 7; inspects actual content. 
4. **NGFW** — stateful inspection + deep packet inspection + IDS/IPS + application control.
### IDS / IPS
- **IDS** — detects and alerts, doesn't block.
- **IPS** — detects and actively blocks in real time.
- **Signature-based** — matches known exploit patterns.
- **Anomaly-based** — flags deviation from normal activity.
- Suricata can act as both.
- **NIDS/NIPS** — network-based, at strategic points (e.g. core switch sensor).
- **HIDS/HIPS** — host-based, on individual machines (e.g. endpoint agent).
## Practical Impact / Security Relevance
> [!info] Goal
>  > Network security exists to uphold the **CIA triad**.
>  > 
> [!warning] Best practices
>  > 1. Clear policies — least privilege.
>  > 2. Regular updates — firewall/IDS signatures/OS patched.
>  > 3. Monitor and log — review firewall/IDS/system logs regularly.
>  > 4. Defense in depth — layered controls (firewall + IDS/IPS + AV + endpoint).
>  > 5. Periodic pen testing — validate policies against real attack simulation.