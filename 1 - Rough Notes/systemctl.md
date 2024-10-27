---
tags:
  - commands
type: system_architecture
description: Used for interact to systemd. Run, stop, restart services.
Date: 2024-09-12 22:48
weight:
---

Tags: [[System Architecture]]
___
# systemctl

Systemctl is a command for manage [[systemd]].
Systemctl can monitoring, run, stop, activate, execute ... a `unit.service`.

- Starting a service
```bash
systemclt start unit.service
```

- Stop a service
```bash
systemclt stop unit.service
```

- Restart a service
```bash
systemclt restart unit.service
```

- Show the state of the service
```bash
systemclt status unit.sevice
```

- Show if the unit.service is active.
```bash
systemclt is-active unit.sevice
```

- Enables unit during the system initialization.
```bash
systemclt enable unit.sevice
```

- Disable unit during the system initialization.
```bash
systemclt disable unit.sevice
```

- Disable unit during the system initialization.
```bash
systemclt is-enavled unit.sevice
```

- Set the run level at 3
```bash
systemctl isolate multi-user.target
```

- Get the current run-level
```bash
systemctl get-default
```

- You could shutdown the system too
```
systemctl poweroff
```

- You could reboot the system too
```
systemctl reboot
```
___
## References
[[LPIC-1 Exam 101.pdf#page=]]