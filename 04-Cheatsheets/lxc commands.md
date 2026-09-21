---
tags: [cheatsheet, lxc]
module: Linux Fundamentals
---

# LXC Container Management Cheatsheet

| Command                                       | Description                                       |
| --------------------------------------------- | ------------------------------------------------- |
| `lxc-ls`                                      | List all existing containers                      |
| `lxc-stop -n <container>`                     | Stop a running container                          |
| `lxc-start -n <container>`                    | Start a stopped container                         |
| `lxc-restart -n <container>`                  | Restart a running container                       |
| `lxc-config -n <container> -s storage`        | Manage container storage                          |
| `lxc-config -n <container> -s network`        | Manage container network settings                 |
| `lxc-config -n <container> -s security`       | Manage container security settings                |
| `lxc-attach -n <container>`                   | Connect to a container                            |
| `lxc-attach -n <container> -f /path/to/share` | Connect to a container and share a directory/file |