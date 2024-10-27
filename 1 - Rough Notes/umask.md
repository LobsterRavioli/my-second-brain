---
tags:
  - commands
type: create_partitions_and_filesystems
description: define a mask that will be used for substract authorizations at creation of files and directories
Date: 2024-09-23 14:42
weight: "3"
---

___
# umask

## Syntax
```bash
umask number
```

## Description
Umask it's an utilities for removing by default shell access authorization.
The default authorizations for:
- **File**: 666
- **Directories**: 777
After that the mask is setted when we create a file or directory these octal numbers will be substracted the mask.

## Option

| Option | functionallity |
| ------ | -------------- |
|        |                |


## Examples
- Removing for all file created the read permission for users
```bash
umask 400
```
- See umask in symbolic mode
```bash
umask -S
```

- Setting umask with symbolic mode
```bash
umask u=r-x, g=rwx, o=rwx
```
___
## References
[[LPIC-1 Exam 101.pdf#page=]]