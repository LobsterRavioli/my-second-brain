---
tags:
  - commands
type: create_partitions_and_filesystems
description: unmount the filesystem from the device or directory
Date: 2024-09-22 11:46
weight: "3"
---

___
# umount

## Syntax
```bash
umount [options] device 
umount [options] directory
```

## Description
Unmount the filesystem from the device or directory.

## Option

| Option | functionallity                             |
| ------ | ------------------------------------------ |
| `-a`   | unmount all filesystem listed in [[fstab]] |
| `-f`   | force the unmouting.                       |
| `-r`   | make the filesystem in read-only mode      |


## Examples
- Unmount the `/dev/sdb1`
```bash
umount /dev/sdb1
```

___
## References
[[LPIC-1 Exam 101.pdf#page=]]