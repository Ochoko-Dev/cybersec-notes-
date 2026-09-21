---
tags: [linux, monitoring, troubleshooting, remote-desktop]
module: Linux Fundamentals
---

# Monitoring, Troubleshooting & Remote Desktop Protocols

## Network Monitoring
Capturing and analyzing traffic to detect security threats, performance issues, and unauthorized activity.
- **Primary objective** — identify vulnerabilities, malicious traffic, and suspicious behavior.
- **Credential exposure** — unencrypted protocols (e.g. FTP) let attackers intercept plain-text credentials for lateral movement/privesc.
- **Behavioral insights** — visibility into network activity helps spot patterns indicating risk.
- **Standard tools** — Wireshark, `tshark`, `tcpdump`.

## Troubleshooting
Diagnosing and resolving network issues affecting performance/reliability. Common tools: `ping`, `traceroute`, `netstat`, `tcpdump`, `wireshark`, `nmap`.

## Remote Desktop Protocols
- **RDP (Remote Desktop Protocol)** — primarily Windows; connects and interacts with a remote desktop as if sitting in front of it.
- **VNC (Virtual Network Computing)** — popular in Linux (cross-platform); graphical access to remote desktops, similar role to RDP.

### X Server
The display server component of the X Window System (X11), managing GUIs on Unix/Linux.
- Uses client-server protocols (even locally, via TCP/IP or Unix sockets) to draw/display windows.
- **Network transparency** — can run apps on a remote host while rendering locally, without VNC/RDP.
- **Ports** — TCP 6000 for display `:0`, up through 6001–6009 for further displays.
- **Security** — transmits unencrypted by default; needs SSH tunneling or similar.

### XDMCP
X Display Manager Control Protocol — used by the X Display Manager over UDP port 177 to manage remote X Window sessions. Insecure; should not be used where high security is required.

### VNC (detail)
Remote desktop sharing based on the RFB protocol.
- Supports sharing the active screen or launching isolated virtual sessions per login.
- **Ports** — TCP 5900 for display `:0`, incrementing per display (5901, 5902...).
- **Common software** — UltraVNC, RealVNC, TightVNC, TigerVNC.
- Commonly paired with lightweight desktop environments (e.g. XFCE4) due to instability running VNC over GNOME.

## Related
- [[network-configuration]]
- [[firewall-iptables]]