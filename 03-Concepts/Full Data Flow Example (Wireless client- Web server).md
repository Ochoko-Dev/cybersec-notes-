**Related Notes:** [[Networking-MOC]], [[DHCP]], [[DNS-Resolution-Process]], [[NAT]] 
---
## Core Mechanics
1. **WLAN connection & DHCP** — laptop authenticates (SSID/WPA), DHCP assigns private IP, subnet mask, gateway, DNS.
2. **DNS resolution** — browser resolves the domain to a public IP. 
3. **Encapsulation** — HTTP/HTTPS request (App) → TCP segment, port 80/443 (Transport) → IP packet (Internet) → framed with ARP-resolved gateway MAC (Link).
4. **NAT & transit** — router NATs the private IP to its public IP, forwards across intermediate routers.
5. **Server processing** — destination firewall validates traffic; web server builds the response.
6. **Response, decapsulation, render** — response routes back through NAT to the private IP; browser decapsulates and renders the page.
## Practical Impact / Security Relevance
Ties every layer covered today — DHCP, DNS, NAT, encapsulation, and the firewall check at the destination — into one real request lifecycle.