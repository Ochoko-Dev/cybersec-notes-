---
tags: [cheatsheet, linux, filesystem]
module: Linux Fundamentals
---

# Linux Filesystem Hierarchy Cheatsheet

| Path          | Description                                                                       |
| ------------- | --------------------------------------------------------------------------------- |
| `/`           | The root directory — contains all other directories and files in the file system. |
| `/bin`        | Essential command binaries required for booting and basic operations.             |
| `/boot`       | Boot-related files — bootloader, kernel images.                                   |
| `/dev`        | Device files representing physical and logical devices.                           |
| `/etc`        | System configuration files, startup scripts, user authentication data.            |
| `/home`       | Each user's home directory for storage.                                           |
| `/kernel`     | Kernel modules and other kernel-related files.                                    |
| `/lib`        | Shared libraries required by binaries in `/bin` and `/sbin`.                      |
| `/lost+found` | Used by fsck to store recovered files after a filesystem check.                   |
| `/media`      | External removable media (e.g. USB drives) are mounted here.                      |
| `/mnt`        | Temporary mount point for regular filesystems.                                    |
| `/opt`        | Optional/third-party software packages.                                           |
| `/proc`       | Virtual view into the system's process and kernel status, exposed as files.       |
| `/root`       | Home directory for the root user.                                                 |
| `/sbin`       | Executables for system administration tasks.                                      |
| `/tmp`        | Temporary files; generally cleared on boot, may be deleted anytime.               |
| `/usr`        | System-wide read-only data — executables, libraries, docs.                        |
| `/var`        | Variable data — logs, mail spools, print spools, cron files.                      |