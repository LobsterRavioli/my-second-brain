---
tags:
  - commands
type: create_partitions_and_filesystems
description: Give UUID of a device or partition.
Date: 2024-09-20 16:59
weight: "3"
---

___
# lsblk

## Syntax
```bash
lsblk -f /dev/sda1
```

## Description
Get the UUID and the label from the filesystem.
This utility is used for setting uuid in the folder and predeterminate in a concise way the folder of mounting with an unique identificator.
## Option

| Option | functionallity |
| ------ | -------------- |
|        |                |


## Examples
-  list all filesystem of sda1
```bash
lsblk -f /dev/sda1
```
___
## References
[[LPIC-1 Exam 101.pdf#page=]]