---
tags:
  - commands
type: create_partitions_and_filesystems
description: change the owner or groups of the file.
Date: 2024-09-23 14:16
weight: "3"
---

___
# chown

## Syntax
```bash
chown USERNAME:GROUPNAME FILENAME
```

## Description
Change the ownership of a file, you can change the user or the group.
## Option

| Option | functionallity |
| ------ | -------------- |
|        |                |


## Examples
- Setting file ownership of a group
```bash
chown :student afile
```
- Setting a file ownershiop of an user
```bash
chown franscesco afile
```
- Setting a file ownershiop of an user and a group
```bash
chown francesco:ownership afile
```
___
## References
[[LPIC-1 Exam 101.pdf#page=]]