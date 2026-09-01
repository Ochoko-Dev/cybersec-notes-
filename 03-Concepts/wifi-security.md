---
tags: [networking, wifi, wireless-security]
module: Introduction to Networking
---

# Wi-Fi Security

## Core Security Features
- **Encryption** — secures Wi-Fi traffic by converting plaintext into ciphertext as it travels through the air. WPA2 (AES-CCMP) and WPA3 (GCMP-256) prevent eavesdroppers from intercepting traffic, credentials, or session data. Older/weaker standards: WEP, WPA.
- **Access Control** — restricts which devices/users can join the network: MAC address filtering, Pre-Shared Keys (PSK) for home use, and 802.1X/Enterprise auth (individual credentials via a RADIUS server).
- **Firewall** — filters traffic between the Wi-Fi network and external networks (or between isolated Wi-Fi segments) using Stateful Packet Inspection (SPI) and rule-based filtering (IP/port/protocol).

## Wireless Authentication Protocols
- **LEAP** — Cisco-developed, uses EAP + RC4 encryption for mutual auth between client and server. Vulnerable to dictionary attacks — largely replaced by EAP-TLS and PEAP.
- **PEAP** — a secure tunneling protocol based on EAP, uses TLS to encrypt client-server communication. Server-side certificate authenticates the server; client can authenticate via password, cert, or biometrics. Widely used in enterprise networks.

## Wireless Hardening Checklist
- Disable SSID broadcasting
- Use WPA (WPA2/WPA3 in practice)
- MAC filtering
- Deploy EAP-TLS

## Related
- [[authentication-protocols]] (cheatsheet)
- [[ipsec]]