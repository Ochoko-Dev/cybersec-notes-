---
tags: [linux, ssh, nfs, web-server, vpn, apache]
module: Linux Fundamentals
---

# Network Services

## SSH
A network protocol that allows secure transmission of data and commands over a network — widely used to securely manage and access remote systems. The most common SSH server is **OpenSSH**.

```
sudo apt install openssh-server -y
systemctl status ssh
```

## NFS (Network File System)
Allows storing and managing files on remote systems as if they were local — enables easy, efficient file/resource sharing across networks (e.g. replicating file systems between servers).

```
sudo apt install nfs-kernel-server -y
systemctl status nfs-kernel-server
```

## Web Server
Software that delivers data, documents, applications, and functionality over the internet. Uses **HTTP** to transmit data to clients (browsers) and receive requests, rendering the response as **HTML** for dynamic, interactive web pages.

**Apache** is one of the most widely used web servers, known for its modularity:
- `mod_ssl` — encrypts communication between browser and server
- `mod_proxy` — directs requests to the correct destination (proxy setups)
- `mod_headers` / `mod_rewrite` — fine control over HTTP headers and URLs

```
sudo apt install apache2 -y
```

## curl / Wget
- **curl** — transfers files from the shell over HTTP, HTTPS, FTP, SFTP, FTPS, SCP; lets you control and test websites remotely from the command line.
- **Wget** — alternative to curl; downloads and stores website content locally.

## VPN
A Virtual Private Network functions like a secure, invisible tunnel connecting to another network — as if physically present within it — by establishing an encrypted tunnel between client and server.

## Related
- [[nfs-access-permissions]] (cheatsheet)