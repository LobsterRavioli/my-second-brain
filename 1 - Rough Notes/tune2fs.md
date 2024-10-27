---
tags:
  - commands
type: create_partitions_and_filesystems
description: tune filesystem parameters.
Date: 2024-09-20 14:25
weight: "2"
---

___
# tune2fs

## Syntax
```bash
tune2fs [option] device
```

## Description
Modify the tuning paramets or ext2 and ext3 filesystem.

## Option

| Option       | functionallity                                                                                                                                                                              |
| ------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| -l           | list all the parameters on a device                                                                                                                                                         |
| -c n         | Set maximum mount, if 0 it's unlimited.                                                                                                                                                     |
| -i n         | Set maximum time between checks, if is 0 disable this value.                                                                                                                                |
| -L           | set the volume label.                                                                                                                                                                       |
| -U           | set the UIID for the filesystem.                                                                                                                                                            |
| -e BEHAVIOUR | set the behaviour of a kernel when filesystem error is found, like continue (continue the execution) , remount-ro (remount filesystem as read only), panic (cause a kernel panic).          |
| -j           | if the filesystem is ext3 add a jornal to the filesystem and set has_journal feature flag                                                                                                   |
| -J parameter | customize -j execution with paramete, -size (size of the journal) , -location (location of the journal), device (device of the journal), example`-J size=10,location=100M,device=/dev/sdb1` |


## Examples
- List the contents of the [[Filesystem superblock]] on `/dev/sda1`.
```bash
tune2fs -l /dev/sda1
```
- Turn off the maximum mount count and check interval tests on `/dev/sda1`.
```bash
tune2fs -c 0 -i 0 /dev/sda
```
___
## References
https://learning.lpi.org/en/learning-materials/101-500/104/104.2/104.2_01/