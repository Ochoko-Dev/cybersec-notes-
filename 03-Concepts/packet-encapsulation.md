---
tags: [networking, osi-model, encapsulation]
module: Introduction to Networking
---

# Networking Models & Packet Transfer

## Networking Models
(Already familiar with this from prior study — diagram kept for reference.)

![[Pasted image 20260901111704.png]]

## Protocol Data Units (PDU)
In a layered system, devices in a layer exchange data in a different format called a **Protocol Data Unit (PDU)**.

## Encapsulation
Occurs during transmission: each protocol layer adds its own header to the upper layer's PDU, wrapping the data step-by-step down to the Physical layer for delivery.

## Decapsulation
Occurs at the receiving end: the receiver strips off the header at each layer to process and unpack the original data, until it reaches the receiving application.

## Related
- [[ip-addressing-subnetting]]