![[Screenshot from 2026-08-13 17-37-10 1.png]]![[Screenshot from 2026-08-13 17-37-10.png]]![[Screenshot from 2026-08-13 17-21-01.png]]- **Tags:** #htb #journal #networking - **Module:** Junior SOC Analyst Path — Network Foundations (4 sections completed)
## Basics
A network moves data between **nodes** connected by **links**. Two main scopes: **LAN** (local area network) and **WAN** (wide area network). Understanding networking models (OSI, TCP/IP) matters as an analyst because most attacks and defenses are described in terms of which layer they operate at.
## OSI Model
![[Screenshot from 2026-08-13 16-30-03.png]]

Walked through it via a file-transfer example, top to bottom: 
7. **Application** — initiates the file transfer request. 
8. **Presentation** — encrypts the file for secure transmission. 5. 
9. **Session** — establishes a communication session with the receiving device. 
10. **Transport** — breaks the file into segments for error-free delivery. 
11. **Network** — determines the best route across the network. 
12. **Data Link** — encapsulates data into frames for node-to-node delivery. 
13. **Physical** — handles actual transmission of bits over the medium.

should be 7 6 5 4 3 2 1

## TCP/IP Model
![[Screenshot from 2026-08-13 16-36-05.png]]

Condensed to 4–5 layers — this is what's actually used in practice, not OSI.
-Session + Presentation → merge into **Application** 
- Data Link + Physical → merge into **Network Access**
## Network Components 
Component & Role
End devices (computers, phones, IoT)- Ultimately send/receive data Intermediary devices (switches, routers, modems)- Move data between end devices, forward packets
NIC-Hardware enabling a device to connect to a network
Router- Forwards packets between networks; uses OSPF, BGP
Switch- Connects devices within one LAN; reduces congestion
Hub-Connects devices in a segment, broadcasts to all ports regardless of destination
Server- Provides services to clients — resource sharing, data management, authentication. 
## Network Protocols 
Rules controlling how data is formatted, transmitted, received, interpreted. Cover: data segmentation, addressing, routing, error checking, synchronization.
Common ones: `TCP/IP`, `HTTP/HTTPS`, `FTP`, `SMTP`

**Network management software** monitors/controls network components: performance monitoring, configuration management, fault analysis, security management.

**Software firewalls** — per-device app that monitors/controls in/outbound traffic based on rules. 
![[Screenshot from 2026-08-13 17-21-01 1.png]]

## Network Communication — MAC, IP, Ports
Unique identifier on a device's NIC, used only within the same local network (LAN/Wi-Fi)
![[Screenshot from 2026-08-13 17-37-10 2.png]]

How it's used: 
1. **ARP** — device knows the destination IP but not its MAC, so it broadcasts "who has this IP?" and gets a MAC address back. 
2. **Framing** — data is wrapped in a frame with source and destination MAC addresses. 
3. **Switch routing** — the switch reads the destination MAC and sends the frame to the exact port that device is plugged into.
### IP Address 
Numerical label for a device on an IP-based network.
- Data is split into **packets**, each with a Source IP and Destination IP in the header.
- Routers inspect the destination IP and use routing tables to forward packets hop-by-hop.
- An IP (e.g. `192.168.1.50`) splits into **Network ID** (which network) and **Host ID** (which device on it).
### Ports
Number assigned to a process/service so traffic gets sorted correctly.