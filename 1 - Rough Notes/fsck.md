---
tags:
  - commands
type: create_partitions_and_filesystems
description: check for filesystem error and correct them
Date: 2024-09-20 14:04
weight:
---

___
# fsck

## Syntax
```bash
fsck [options] [-t type] [fs-options] filesystems
```

## Description

Check for filesystem errors andoptionally correct them.
By default, fsck assumes the ext2/3/4 filesystem by default filesystem type and runs interactively, pausing to ask for permission before applying fixes.

## Option

| Option    | functionallity                                              |
| --------- | ----------------------------------------------------------- |
| `-t type` | specify the type of filesystem to chck the default is ext2. |
| `-A`      | This will check all filesystem listed in /etc/fstab         |
| -N        | Don't execute, but show what would be done.                 |
| -R        | with A will  skil the root filesystem.                      |
| -C        | Show progression bar                                        |
| -V        | Verbose mode                                                |


## Examples
- Check the ext3 filesystem on /dev/sda1, which is not mounter
```bash
fsck /dev/sda1
```
- 
```bash

```
___
## References
[[LPIC-1 Exam 101.pdf#page=]]