---
tags:
  - commands
type: gnu_and_unix_commands
description: parse text in input and execute command on that.
Date: 2024-09-17 18:35
weight: "4"
---

___
# xargs

## Syntax
```bash
xargs [options] [command] [initial-arguments]
```

## Description
Execute command follower the initial arguments of the commadn.
The xargs command parse the input received in stdin and execute for every parsed word the command indicated in the parameters.

## Option

| Option       | functionallity                                       |
| ------------ | ---------------------------------------------------- |
| `-n maxargs` | Limits the number of additional arfuments to ma      |
| `-p`         | interactive mode                                     |
| -0           | parse the words considering the blank characters too |


## Examples
- 
```bash


```
- 
```bash


```
___
## References
[[LPIC-1 Exam 101.pdf#page=]]