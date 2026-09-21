---
tags: [cheatsheet, nfs]
module: Linux Fundamentals
---

# NFS Access Permissions Cheatsheet

| Permission       | Description                                                                                              |
| ---------------- | -------------------------------------------------------------------------------------------------------- |
| `rw`             | Gives users/systems read and write permissions to the shared directory.                                  |
| `ro`             | Gives users/systems read-only access to the shared directory.                                            |
| `no_root_squash` | Prevents the client's root user from being restricted to normal-user rights.                             |
| `root_squash`    | Restricts the client's root user to normal-user rights.                                                  |
| `sync`           | Synchronizes data transfer — changes are only transferred after being saved on the file system.          |
| `async`          | Transfers data asynchronously — faster, but may cause inconsistencies if changes aren't fully committed. |