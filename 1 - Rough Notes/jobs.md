---
tags:
  - commands
type: gnu_and_unix_commands
description: list all processes started from a terminal
Date: 2024-09-18 10:29
weight: "4"
---

___
# jobs

## Syntax
```bash
jobs [options] [jobspecs]
```

## Description
List all active [[Job Processes]].

## Option

| Option | functionallity                                                            |
| ------ | ------------------------------------------------------------------------- |
| -`l`   | list also the pid                                                         |
| -n     | List only processes that have changed status since the last notification. |
| -p     | List process IDs.                                                         |
| -r     | List only running jobs in background.                                     |
| -s     | List only stopped jobs                                                    |


## Examples
- Show running jobs
```bash
jobs -r
```
- Show
```bash


```
___
## References
[[LPIC-1 Exam 101.pdf#page=]]