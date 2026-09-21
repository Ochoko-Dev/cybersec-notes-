---
tags: [cheatsheet, linux, processes]
module: Linux Fundamentals
---

# Process Signals Cheatsheet

| Signal | Name — Description                                       |
| ------ | -------------------------------------------------------- |
| `1`    | `SIGHUP` — sent when the controlling terminal is closed. |
| `2`    | `SIGINT` — sent on `Ctrl+C` to interrupt a process.      |
| `3`    | `SIGQUIT` — sent on `Ctrl+D` to quit.                    |
| `9`    | `SIGKILL` — immediately kills a process, no cleanup.     |
| `15`   | `SIGTERM` — program termination.                         |
| `19`   | `SIGSTOP` — stops the program; cannot be handled.        |
| `20`   | `SIGTSTP` — sent on `Ctrl+Z`; suspends, can be resumed.  |