---
tags:
  - commands
type: create_partitions_and_filesystems
description: make a file-system on a device.
Date: 2024-09-20 11:36
weight: "3"
---

___
# mkfs

## Syntax
```bash
mkfs [-t ftype] [fs_options] device
```

## Description
Make a [[File System | filesystem]] of type ftype on device.
If ftype is omitted, ext2 is used by default.
There are many aliases for this command and is common to omit the ftype options for commands like `mkfs.ext2`, `mkfs.ext4` or `mkfs.xfs`..

## Option

| Option   | functionallity                                             |
| -------- | ---------------------------------------------------------- |
| -c       | Check device for bad blocks before building the filesystem |
| -L label | set the volume label for the filesystem                    |
| -n lable | set the 11-character volume label for the filesystem       |
| -q       | Uses mkfs in quiet mode, resulting in very little output.  |
| -v       | Used to enter verbose mode                                 |
| -j       | Create an ext3 journal file                                |
| -b SIZE  | Sets the size of the data blocks in the device to SIZE     |
| -F       | This option will force mke2fs to create a filesystem.      |


## Examples
- Create an ext2 pariotion on /dev/hda3
```bash
mkfs -q /dev/hda3
```
- Create an ext2 filesystem labeled rootfs on existing parition `/dev/hda3`, checking for bad blocks and output in verbose mode.
```bash
mkfs -t ext2 -cv /dev/hda3
```

___
## References
[[LPIC-1 Exam 101.pdf#page=]]