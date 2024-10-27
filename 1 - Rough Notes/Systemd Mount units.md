---
tags:
  - "#path"
type: 
description: 
Date: 2024-09-22 15:40
path:
---

___
# Systemd Mount units

The systemd mount unit is a config file used by systemd for mounting disks or partition to the os.

The config file are in this format:

```bash
[Unit]
Description=External data disk

[Mount]
What=/dev/disk/by-uuid/56C11DCC5D2E1334
Where=/mnt/external
Type=ntfs
Options=defaults

[Install]
WantedBy=multi-user.target
```

- **Description**: short description about mount unit.
- What: what to mount it follows a format
- Where: the folder where the device will be mounted
- Type: type of filesystem
- Options: same option like [[mount]]
- Wantedby: the dependency management.

> [!WARNING]
> The mount unit should have the same name of the mount poin.
>  In this case, the mount point is `/mnt/external`, so the file should be named `mnt-external.mount`.

For mounting the partition we need to reload systemd like this:
```bash
systemctl daemon-reload
systemctl start mnt-external.mount
```

To enable on every boot:
```bash
systemctl enable mnt-external.mount
```

___
## References
[[LPIC-1 Exam 101.pdf#page=]]