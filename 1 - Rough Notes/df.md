---
tags:
  - commands
type: create_partitions_and_filesystems
description: check for disk free spacke
Date: 2024-09-20 12:51
weight: "2"
---

___
# df

## Syntax
```bash
df [options] [file [file...]]
```

## Description

## Option
The command df will provide a list of all the avaible filesystems on your system, including their total size, how much space has been used, how much space is avaible, the usage percentage and where is mounted.

| Option    | functionallity                   |
| --------- | -------------------------------- |
| `-h`      | human readable output.           |
| `-i`      | show the inodes block            |
| `-T`      | print the type of the filesystem |
| `-x TYPE` | exclude a filesystem             |

## Output option
You can specify the output format with `--output`.

| **Option** | **Description**                                |     |
| ---------- | ---------------------------------------------- | --- |
| `source`   | The device corresponding to the filesystem.    |     |
| `fstype`   | The filesystem type.                           |     |
| `size`     | The total size of the filesystem.              |     |
| `used`     | How much space is being used.                  |     |
| `iavail`   | How much space is available.                   |     |
| `pcent`    | The usage percentage of the filesystem.        |     |
| `target`   | Where the filesystem is mounted (mount point). |     |
| `itotal`   | Number of inodes                               |     |
## Examples
- Customise the output
```bash
$ df -h --output=target,source,fstype,pcent
Mounted on                    Filesystem     Type     Use%
/dev                          udev           devtmpfs   0%
/run                          tmpfs          tmpfs      1%
/                             /dev/sda1      ext4      25%
/dev/shm                      tmpfs          tmpfs     32%
/run/lock                     tmpfs          tmpfs      0%
/sys/fs/cgroup                tmpfs          tmpfs      0%
/run/user/119                 tmpfs          tmpfs      1%
/run/user/1000                tmpfs          tmpfs      1%
/media/carol/part1            /dev/sdb1      ext4       2%
/media/carol/part3            /dev/sdb3      ext4       3%
/media/carol/part2            /dev/sdb2      ext4       3%
/media/carol/Samsung Externo  /dev/sdc1      fuseblk   75%
```
- Print all the Filesystem and their type in human readable format.
```bash
df -hT
Filesystem     Type      Size  Used Avail Use% Mounted on
udev           devtmpfs  2.9G     0  2.9G   0% /dev
tmpfs          tmpfs     582M  2.5M  580M   1% /run
/dev/sda1      ext4      106G   25G   76G  25% /
tmpfs          tmpfs     2.9G  930M  2.0G  32% /dev/shm
tmpfs          tmpfs     5.0M     0  5.0M   0% /run/lock
tmpfs          tmpfs     2.9G     0  2.9G   0% /sys/fs/cgroup
tmpfs          tmpfs     582M   24K  582M   1% /run/user/119
tmpfs          tmpfs     582M  116K  582M   1% /run/user/1000
/dev/sdb1      ext4       88M  1.6M   79M   2% /media/carol/part1
/dev/sdb3      ext4       82M  1.6M   74M   3% /media/carol/part3
/dev/sdb2      ext4       89M  1.9M   81M   3% /media/carol/part2
/dev/sdc1      fuseblk   299G  223G   76G  75% /media/carol/Samsung Externo
```


___
## References
[[LPIC-1 Exam 101.pdf#page=]]