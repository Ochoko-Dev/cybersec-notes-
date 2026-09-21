---
tags: [linux, systemd, cron, task-scheduling]
module: Linux Fundamentals
---

# Task Scheduling

Task scheduling allows users and administrators to automate tasks by running them at specific times or regular intervals, eliminating the need for manual initiation.

## Systemd Timers
`systemd` can start processes and scripts at a specific time.

**Steps:**
1. Create a timer (schedules when `mytimer.service` should run)
2. Create a service (executes the commands or script)
3. Activate the timer

### Create a Timer
```
sudo mkdir /etc/systemd/system/mytimer.timer.d
sudo vim /etc/systemd/system/mytimer.timer
```
The script must contain `[Unit]`, `[Timer]`, and `[Install]` sections:
```
[Unit]
Description=My Timer
[Timer]
OnBootSec=3min
OnUnitActiveSec=1hour
[Install]
WantedBy=timers.target
```
Use `OnBootSec` to run a script once after boot; use `OnUnitActiveSec` to run it at regular intervals.

### Create a Service
```
sudo vim /etc/systemd/system/mytimer.service
```
```
[Unit]
Description=My Service
[Service]
ExecStart=/full/path/to/my/script.sh
[Install]
WantedBy=multi-user.target
```
`multi-user.target` is the unit activated during normal multi-user startup — it defines the services that should start on a normal system boot.

Reload systemd to pick up changes:
```
sudo systemctl daemon-reload
```

### Start the Timer and Service
```
sudo systemctl start mytimer.timer
sudo systemctl enable mytimer.timer
```
This launches `mytimer.service` automatically according to the intervals/delays set in `mytimer.timer`.

## Cron
Another tool for scheduling/automating tasks, with a different setup process than systemd. Tasks are stored in a file called `crontab`, and the cron daemon runs them according to a defined schedule.

## Related
- [[cron-schedule-fields]] (cheatsheet)
- [[service-process-management]]