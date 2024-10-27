---
tags:
  - commands
type: gnu_and_unix_commands
description: watch the c
Date: 2024-09-18 15:52
weight: "4"
---

___
# watch

## Syntax
```bash
watch [-option] command
```

## Description
The watch command is used to execute a command periodically and display its output on the terminal. It’s useful for monitoring the output of commands that change over time, such as system resource usage, file changes, or the status of a process.

## Option

| Option | functionallity                                      |
| ------ | --------------------------------------------------- |
| -n     | specifies the time to wait for exacute the command. |


## Examples
- Open vim and write some stuff
```bash
vim prova.txt
```
Then use watch to see the editings of a file changing during time
```bash
watch cat prova.txt
```
___
## References
[[LPIC-1 Exam 101.pdf#page=]]