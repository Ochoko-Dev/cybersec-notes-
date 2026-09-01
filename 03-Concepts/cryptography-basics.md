---
tags: [cryptography, security-fundamentals]
module: Introduction to Networking
---

# Cryptography Basics

**Cryptography** is the science of securing communication and data by converting plaintext into unreadable ciphertext, so that only authorized parties with the correct key can access it.

## Key Concepts
- **Symmetric Encryption** — a single shared key both encrypts and decrypts data (e.g. AES). Fast and efficient for large amounts of data.
- **Asymmetric Encryption** — a mathematically linked key pair: a **Public Key** encrypts data, a **Private Key** decrypts it (e.g. RSA, ECC).
- **Hashing** — a one-way function that turns input data into a fixed-length string (e.g. SHA-256) to verify data integrity. Cannot be reversed.
- **Digital Signatures** — combines asymmetric encryption and hashing to verify the authenticity and non-repudiation of a sender.

## Related
- [[ipsec]]
- [[authentication-protocols]] (cheatsheet)