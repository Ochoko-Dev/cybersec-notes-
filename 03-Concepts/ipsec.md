---
tags: [networking, ipsec, vpn]
module: Introduction to Networking
---

# IPsec

**IPsec (Internet Protocol Security)** is a network security protocol that provides encryption and authentication for internet communications. It encrypts the data payload of each IP packet and adds an **Authentication Header (AH)** to verify the packet's integrity and authenticity.

## Two Core Protocols
1. **AH (Authentication Header)** — provides integrity and authenticity, but **no encryption**. Adds a cryptographic checksum to each IP packet to verify it hasn't been tampered with.
2. **ESP (Encapsulating Security Payload)** — provides **encryption** and optional authentication. Encrypts the payload of each IP packet and can optionally add an authentication header, similar to AH.

## Related
- [[ip-addressing-subnetting]]
- [[cryptography-basics]]