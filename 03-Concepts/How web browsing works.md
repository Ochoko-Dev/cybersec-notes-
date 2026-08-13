1. **DNS Lookup** — domain name (`example.com`) resolves to an IP (`93.184.216.34`).
2. **Encapsulation** — Application layer builds an HTTP/HTTPS request → wrapped in a TCP segment (port 80 or 443) → packed into an IP packet with the destination IP → Data Link layer uses ARP to find the gateway router's MAC address.
3. **Transmission** — frame goes to the router's MAC locally; router forwards the IP packet; intermediate routers do hop-by-hop forwarding.
4. **Server processing** — destination server passes the packet to the app listening on port 80/443, processes the request, generates a response.
5. **Response** — sent back to the client's source IP and the ephemeral port opened for that session, following the reverse path back.