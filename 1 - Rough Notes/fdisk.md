---
tags:
  - commands
type: 
description: 
Date: 2024-09-19 14:20
weight:
---

___
# fdisk

## Syntax
```bash
fdisk [device]
```

## Description
It start a command-driven interactive text interface Manipulate the partition table.
The command do take input letters followed by a carriage number.
For primary partitions the number is from 1 to 4.
For logical partitions the partition number is from 4 to 16.

| **Command** | **Description**                                                                                                                                                                       |
| ----------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `d`         | delete a partition, if you delete a logical partition when a higher-numbered logical partition exist the partition numbers are decremented to keep logica partition number contiguos. |
| `l`         | list the know partition types.                                                                                                                                                        |
| `m`         | Display the brief help menu for these commands                                                                                                                                        |
| `n`         | Add a new partition. The command will ask number of partition and type, starting cylinder end ending cylinder for the partition.                                                      |
| `p`         | Display partition table.                                                                                                                                                              |
| `q`         | quit                                                                                                                                                                                  |
| `t`         | Change partiotions system ID, number that indicates the type of the filesystem/                                                                                                       |
| `w`         | write (save) the partiotion table to disk and exit                                                                                                                                    |

## Option

| Option | functionallity |     |
| ------ | -------------- | --- |
|        |                |     |


## Examples
-  Display existing partition table on /dev/hda without making any changes.
```bash
fdisk /dev/hda
```

# Exam Tips

> [!TIP]
> You should understand disk partitions and the [[Process of creating partition using fdisk | process of creating them using fdisk ]].



___
## References
[[LPIC-1 Exam 101.pdf#page=]]