---
tags:
  - commands
type: 
description: 
Date: 2024-09-18 14:25
weight:
---

___
# kill

## Syntax
```bash
kill [-s sigspec | -sigspec] [pids] 
kill -l [signum]
```

## Description
Terminate the jobs using [[Job Specification]].
## Option

| Option | functionallity             |
| ------ | -------------------------- |
| `-s`   | specify the signal to send |
|        |                            |


## Examples
- kill by name
```bash
kill -SIGHUP 1247
```
- Kill by number
```bash
kill -1 1247
```
- kill by option
```bash
kill -s SIGHUP 1247
```
- Send a sigkill
```bash
kill -9 1247
```
```bash
kill -KILL 1247
```

___
## References
[[LPIC-1 Exam 101.pdf#page=]]