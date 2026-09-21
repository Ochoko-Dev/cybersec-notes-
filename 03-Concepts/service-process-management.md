---
tags: [linux, services, processes, systemctl]
module: Linux Fundamentals
---

# Service & Process Management

## Services (Daemons)
Services, also known as daemons, are fundamental components of a Linux system that run silently in the background without direct user interaction. They perform crucial tasks that keep the system operational and provide additional functionality. Services fall into two categories: **system services** and **user-installed services**.

`systemctl` starts a service and can list all services:
```
systemctl list-units --type=service
```
If a service fails to start, use `journalctl` to view logs:
```
journalctl -u ssh.service --no-pager
```

## Process States
A process can be in one of these states: **running**, **waiting**, **stopped**, **zombie**.

Processes are controlled using `kill`, `pkill`, `pgrep`, and `killall`. To interact with a process, a signal must be sent to it — view all signals with `kill -l`.

## Backgrounding a Process
`[Ctrl + Z]` suspends the current process (sends `SIGTSTP`), stopping further execution. To keep it running in the background, use `bg`.

## Foregrounding a Process
`fg <ID>` brings a background process back into the foreground to interact with it again.

## Executing Multiple Commands
Three ways to run several commands one after another:
- **`;`** (semicolon) — a command separator; executes commands regardless of previous results/errors.
- **`&&`** (double ampersand) — if a command errors, the following ones are not executed and the process stops.
- **`|`** (pipe) — depends not only on error-free execution of previous processes but also on their results.

## Related
- [[process-signals]] (cheatsheet)
- [[task-scheduling]]