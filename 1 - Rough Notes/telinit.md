---
tags:
  - commands
type: system_architecture
description: change the runlevel of the system
Date: 2024-09-13 09:44
weight:
---

___
# telinit

This command can be used for alternate between various [[SysVinit]] Runlevels.

- Change to run level 2
```bash
telinit 2
```

- Power off
```bash
telinit 0
```

- Enter rescue mode
```bash
telinit 1
```

- Reload init configuration
```bash
telinit q
```
___
## References
[[LPIC-1 Exam 101.pdf#page=]]