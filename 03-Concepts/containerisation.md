---
tags: [linux, docker, lxc, containers]
module: Linux Fundamentals
---

# Containerization

Packages applications and their dependencies into lightweight, isolated environments (containers) that run consistently across any system.

- **Resource Efficiency** — containers share the host OS kernel (unlike VMs), making them faster, lighter, and easier to scale for microservices.
- **Consistency & Portability** — applications perform identically across dev/test/prod since dependencies are self-contained.
- **Core Technologies** — Docker, Docker Compose, Linux Containers (LXC).
- **Security & Isolation** — application-level isolation limits security risk, but offers weaker isolation than VMs; needs proper configuration to prevent privilege escalation or container escapes.

## Docker
Open-source platform for automating deployment of applications as self-contained containers. Uses a layered filesystem and resource isolation for flexibility and portability.

## LXC (Linux Containers)
Lightweight virtualization technology allowing multiple isolated Linux systems (containers) to run on a single host. Uses `cgroups` and `namespaces` for isolation, sharing the host kernel — more efficient than full VMs.

## Docker vs LXC
| Category | Description |
|---|---|
| Approach | LXC is system-level, creating isolated Linux environments like lightweight VMs. Docker is application-focused, optimized for packaging/deploying single apps or microservices. |
| Image building | Docker uses a standardized image format with everything needed to run an app. LXC needs more manual setup. |
| Portability | Docker images are easily shared via Docker Hub/registries. LXC is more tightly tied to host configuration. |
| Ease of use | Docker has a user-friendly CLI and large community. LXC requires more Linux sysadmin knowledge. |
| Security | Docker is generally more secure out of the box (AppArmor, SELinux, read-only filesystem). LXC needs extra config to match. Both can be a local privilege escalation vector if misconfigured. |

## Related
- [[lxc-commands]] (cheatsheet)