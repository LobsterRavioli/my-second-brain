---
tags:
  - commands
type: create_partitions_and_filesystems
description: check how much space is being used and how much left on a filesystem.
Date: 2024-09-20 12:42
weight: "2"
---

___
# du

## Syntax
```bash
du [options] [directories]
```

## Description

du stands for disk usage and is an utility for getting information for directories, if directories is omitted it's assumete that it will be ne current working directory

## Option

| Option | functionallity                               |
| ------ | -------------------------------------------- |
| -a     | show all files, not just directories.        |
| -c     | Produces a grand total for all listed items. |
| -h     | Display results in human readable format     |
| -s     | print a summary for earch directories        |
| -S     | excludes subdirectories from count           |
| -d     | specify the depht.                           |


## Examples
- Show individual count for all files.
```bash
du -ah
```
- 
```bash
du -h
```
___
## References
[[LPIC-1 Exam 101.pdf#page=]]