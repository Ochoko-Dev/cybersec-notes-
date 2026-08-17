**Related Notes:** [[Networking-MOC]], [[Cloud-Architecture]] 
---
## Core Mechanics
Management and control functions are decoupled from physical hardware and implemented entirely through software — separating the **control plane** (decision-making) from the **data/infrastructure plane** (execution).

**Key pillars:** 
- **SDC (Software-Defined Compute)** — virtualizes servers/CPU/memory into VMs or containers (e.g. via Kubernetes). - 
- **SDN (Software-Defined Networking)** — decouples network control from physical switches/routers; centralized controller handles routing and policy.
- **SDS (Software-Defined Storage)** — pools physical disks into a unified, policy-managed storage system.
- **Management & Automation Layer** — central orchestration; APIs provision/scale/monitor infrastructure without manual hardware changes.
## Practical Impact / Security Relevance
The centralized controller programmatically routes traffic, provisions policies, and applies micro-segmentation security across the network.