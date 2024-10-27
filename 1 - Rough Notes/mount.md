---
tags:
  - commands
type: create_partitions_and_filesystems
description: attach a filesystem from a device or partition to a specific path of the current filesystem or print the currents attached filesystems.
Date: 2024-09-20 15:54
weight: "3"
---

___
# mount

## Syntax
```bash
mount [options] device 
mount [options] directory
mount [options] device directory
```

## Description
Used to mount filesystem into the filesystem hierarchy.
The first and second form consult the [[fstab]] config file for the mount information/
The third form is more independent.
## Option

| Option             | functionallity                                                                              |
| ------------------ | ------------------------------------------------------------------------------------------- |
| `-a`               | Mount all partiotion specified in [[fstab]] config file                                     |
| `-h`               | display help                                                                                |
| `-o mount_options` | specifies mount options on the command line, they're the same as the [[fstab]] config file. |
| `-r`               | Mounts the filesystem as read-only                                                          |
| `-v`               | Sets verbose mode                                                                           |
| `-w`               | Mount the filesystem in read/write mode                                                     |

## Examples
- Mount en exfat type of filesystem from partition sdb1 to flash folder
```bash
mount -t exfat /dev/sdb1 ~/flash/
```

- List all mounted filesystem attached in SOURCE on TARGET type TYPE OPTIONS output format
```bash
mount
```

- List all mounted filesystem attached from predetermined type
```bash
mount -t ext4,fuseblk
```



___
## References
[[LPIC-1 Exam 101.pdf#page=]]