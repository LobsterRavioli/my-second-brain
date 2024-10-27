---
tags:
  - commands
type: create_partitions_and_filesystems
description: create an hard link or symbolic link
Date: 2024-09-23 16:49
weight: "2"
---

___
# ln

## Syntax
```bash
ln [options] file link 
ln [options] files directory
```

## Description

## Option
Create an hard link of the file.

| Option | functionallity                          |
| ------ | --------------------------------------- |
| -f     | force                                   |
| -i     | prompt interactively before overwriting |
| -s     | Create a symbolic link                  |

## Examples
- Creating an hard link
```bash
ln file linkozzo
```
- Create a soft link
```bash
ln -s file linkozzo_soft
```
___
## References
[[LPIC-1 Exam 101.pdf#page=]]