---
tags: [linux, filesystems, inodes, swap]
module: Linux Fundamentals
---

# File System Management

## Choosing a File System
- **ext2** — older, no journaling; less suited to modern systems but useful for low-overhead scenarios (e.g. USB drives).
- **ext3 / ext4** — journaling support (helps recover from crashes); ext4 is the default for most modern Linux systems, balancing performance, reliability, and large file support.
- **Btrfs** — advanced features like snapshotting and built-in data integrity checks; ideal for complex storage setups.
- **XFS** — excels at large files and high I/O performance.
- **NTFS** — originally for Windows; useful for dual-boot or external drives shared between Linux and Windows.

## Inodes
Data structures storing metadata about each file and directory — permissions, ownership, size, timestamps. They don't store the actual filename or data, only pointers to the disk blocks holding it.

## File Types
- Regular files
- Directories
- Symbolic links

## Creating Swap Space
Swap can be set up during OS install or added later:
- `mkswap` — prepares a device/file as swap space
- `swapon` — activates the swap space

## Related
- [[containerization]]