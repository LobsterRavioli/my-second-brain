---
tags:
  - commands
type: system_architecture
description: list the logs of the system, from to bootup to the active processes and daemons.
Date: 2024-09-13 09:21
weight:
---

2024-09-12 14:54
Status:
Tags: [[Commands]]
___
# journalctl

The journalctl is a command used for manage the system log generated from systemd.
Journalctl can show kernel messages, daemon manager and processes.

The follow command will shows a list of boot numbers.
```bash
journalctl --list-boots
```
The output will be divided in the follow manner.


|     | Identification hash              | Timestamp                                               |
| --- | -------------------------------- | ------------------------------------------------------- |
| -4  | 9e5b3eb4952845208b841ad4dbefa1a6 | Thu 2019-10-03 13:39:23 -03—Thu 2019-10-03 13:40:30 -03 |
| -3  | 9e3d79955535430aa43baa17758f40fa | Thu 2019-10-03 13:41:15 -03—Thu 2019-10-03 14:56:19 -03 |
| -2  | 17672d8851694e6c9bb102df7355452c | Thu 2019-10-03 14:56:57 -03—Thu 2019-10-03 19:27:16 -03 |
| -1  | 55c0d9439bfb4e85a20a62776d0dbb4d | Thu 2019-10-03 19:27:53 -03—Fri 2019-10-04 00:28:47 -03 |
| 0   | 08fbbebd9f964a74b8a02bb27b200622 | Fri 2019-10-04 00:31:01 -03—Fri 2019-10-04 10:17:01 -03 |
This command will show logs for the current boot
```bash
journalctl -b 0
oct 04 00:31:01 ubuntu-host kernel: EXT4-fs (sda1): mounted filesystem with ordered data mode. Opts: (null)
oct 04 00:31:01 ubuntu-host kernel: ip_tables: (C) 2000-2006 Netfilter Core Team
oct 04 00:31:01 ubuntu-host systemd[1]: systemd 237 running in system mode.
oct 04 00:31:01 ubuntu-host systemd[1]: Detected architecture x86-64.
...
```



___
## References
[[LPIC-1 Exam 101.pdf#page=]]