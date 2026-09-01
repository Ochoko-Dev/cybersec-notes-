---
tags: [cheatsheet, authentication, security]
module: Introduction to Networking
---

# Authentication Protocols Cheatsheet

| Protocol | Description |
|---|---|
| `Kerberos` | Key Distribution Center (KDC)-based authentication protocol that uses tickets in domain environments. |
| `SRP` | A password-based authentication protocol that uses cryptography to protect against eavesdropping and MITM attacks. |
| `SSL` | A cryptographic protocol used for secure communication over a computer network. |
| `TLS` | A cryptographic protocol providing communication security over the internet — successor to SSL. |
| `OAuth` | An open standard for authorization, letting users grant third-party access to web resources without sharing passwords. |
| `OpenID` | A decentralized authentication protocol allowing a single identity to sign in to multiple websites. |
| `SAML` | An XML-based standard for securely exchanging authentication and authorization data between parties. |
| `2FA` | An authentication method using a combination of two different factors to verify identity. |
| `FIDO` | A consortium of companies developing open standards for strong authentication. |
| `PKI` | A system for securely exchanging information using public/private keys for encryption and digital signatures. |
| `SSO` | Allows a user to use a single set of credentials to access multiple applications. |
| `MFA` | Uses multiple factors — something you know, have, or are — to verify identity. |
| `PAP` | A simple authentication protocol that sends a user's password in clear text over the network. |
| `CHAP` | An authentication protocol that uses a three-way handshake to verify identity. |
| `EAP` | A framework supporting multiple authentication methods/technologies. |
| `SSH` | Network protocol for secure client-server communication — remote command-line access, remote execution, and secure file transfer. Uses encryption against eavesdropping. |
| `HTTPS` | Secure version of HTTP using SSL/TLS to encrypt communication and prevent interception. Widely used for secure web browsing. |
| `LEAP` | Cisco wireless authentication protocol; uses EAP for mutual auth and RC4 to encrypt traffic. Vulnerable to dictionary attacks — largely replaced by EAP-TLS/PEAP. |
| `PEAP` | Secure tunneling protocol for wireless/wired networks; based on EAP, uses TLS. Server cert authenticates the server; client can authenticate via password, cert, or biometrics. Widely used in enterprise networks. |

## Related
- [[wifi-security]]
- [[cryptography-basics]]