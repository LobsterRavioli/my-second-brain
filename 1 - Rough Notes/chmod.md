---
tags:
  - commands
type: create_partitions_and_filesystems
description: change permissions of files or directories.
Date: 2024-09-23 10:06
weight: "3"
---

___
# chmod

## Syntax
```bash
chmod [options] symbolic_mode[,symbolic_mode]...files 
chmod [options] octal_mode files 
chmod [options] --reference=rfile files
```

## Description

Chmod stands for change mode and it is used for modify and controlling [[Access permissions]].

We have 2 types of notation:
## Octal format
It takes in input the permission notation and the file.
• **Read (r)** = 4
• **Write (w)** = 2
• **Execute (x)** = 1

We can sum it up for gain each number of each permission group:
Let's make an example, let's set some permission:
- We want w+r on user: 2+1 = 3
- we want on group r+ex on group: 5+1 = 5
- we want on others w+ex: 2 + 1 = 3

So the in put its: `chmod 353`
## Symbolic format

Symbolic mode can follow this notation.
![[Pasted image 20240923104754.png|500]]


## Option

| Option | functionallity                                                       |
| ------ | -------------------------------------------------------------------- |
| `-c`   | Verbose mode but reporting only the changes.                         |
| `-R`   | Recursive change all the files in the hierarchy making modification. |
| `-v`   | use verbose behaviour.                                               |

## Examples
- change afile for: user(rw-), group(r--), others(r--)
```bash
chmod 644 afile
```
- Remove all permission for others for every file recursively contained in adir.
```bash
chmod -R -v o-rwx adir
```
- Set a sticky bit
```bash
chmod -v +t adir
```
___
## References
[[LPIC-1 Exam 101.pdf#page=]]