---
tags:
  - commands
type: create_partitions_and_filesystems
description: check for filesystem error and correct them specifically designed for ext2, ext3 and ext4.
Date: 2024-09-20 14:14
weight: "2"
---

___
# e2fsck

## Syntax
```bash
e2fsck [options] <filesystem>
```

## Description

e2fsck is a file system consistency checker for ext2/ext3/ext4 file systems. It checks the integrity of the file system and attempts to repair any inconsistencies found in interactive way.


## Option

| Option | functionallity                                          |
| ------ | ------------------------------------------------------- |
| -p     | Automatically fix                                       |
| -y     | yes to all question                                     |
| -n     | no to all questions                                     |
| -f     | force to check even if the disk is correctly unmounted. |


## Examples
- Check and repair a file system
```bash
e2fsck /dev/sda1
```
- Check for bad sectors without making changes
```bash
e2fsck -n /dev/sda1
```
___
## References
[[LPIC-1 Exam 101.pdf#page=]]