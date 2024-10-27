---
tags:
  - commands
type: 
description: check for filesystem error and correct them specifically designed for xfs filesystem.
Date: 2024-09-20 15:10
weight: "2"
---

___
# xfs_repair

## Syntax
```bash
xfs_repair [option] /dev/sdb1
```

## Description
Scan and repair in XFS filesystem.

## Option

| Option      | functionallity                                        |
| ----------- | ----------------------------------------------------- |
| `-l LOGDEV` |                                                       |
| `-m N`      | limit memory usage to N butes                         |
| `-d`        | dangerous mode, repair filesystems in reads only mode |
| `-v`        | verbose mode.                                         |
| `-n`        | check for errors but not repair                       |


## Examples
- Check  for errors but not repair
```bash
xfs_repair -n /dev/sdb1
c```

___
## References
[[LPIC-1 Exam 101.pdf#page=]]