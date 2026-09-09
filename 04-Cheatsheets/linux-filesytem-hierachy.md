---
tags: [cheatsheet, linux, filesystem]
module: Linux Fundamentals
---

# Linux Filesystem Hierarchy Cheatsheet

| Path     | Description                                                                                                                                                                                                                |
| -------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `/`      | The top-level directory (root filesystem) — contains all files required to boot the OS before other filesystems are mounted. After boot, other filesystems are mounted at standard mount points as subdirectories of root. |
| `/bin`   | Contains essential command binaries.                                                                                                                                                                                       |
| `/boot`  | Static bootloader, kernel executable, and files required to boot the Linux OS.                                                                                                                                             |
| `/dev`   | Device files to facilitate access to every hardware device attached to the system.                                                                                                                                         |
| `/etc`   | Local system configuration files; configuration files for installed applications may also be saved here.                                                                                                                   |
| `/home`  | Each user on the system has a subdirectory here for storage.                                                                                                                                                               |
| `/lib`   | Shared library files required for system boot.                                                                                                                                                                             |
| `/media` | External removable media devices (e.g. USB drives) are mounted here.                                                                                                                                                       |
| `/mnt`   | Temporary mount point for regular filesystems.                                                                                                                                                                             |
| `/opt`   | Optional files, such as third-party tools, can be saved here.                                                                                                                                                              |
| `/root`  | The home directory for the root user.                                                                                                                                                                                      |
| `/sbin`  | Executables used for system administration (binary system files).                                                                                                                                                          |
| `/tmp`   | Used by the OS and many programs to store temporary files. Generally cleared on boot and may be deleted at other times without warning.                                                                                    |
| `/usr`   | Contains executables, libraries, man files, etc.                                                                                                                                                                           |
| `/var`   | Variable data files — log files, email inboxes, web application files, cron files, and more.                                                                                                                               |