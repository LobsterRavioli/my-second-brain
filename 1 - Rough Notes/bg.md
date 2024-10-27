---
tags:
  - commands
type: gnu_and_unix_commands
description: start background job execution.
Date: 2024-09-18 12:45
weight: "4"
---

___
# bg

## Syntax
```bash
bg [jobspec]
```

## Description
bg is used for starting a jb in stop state.
It used [[Job Specification]] as input parameters.

## Option

| Option | functionallity |
| ------ | -------------- |
|        |                |

## Examples
- Resume sleep in background
```bash
sleep 100
^Z
zsh: suspended  sleep 100
bg %sleep or bg %1
```


___
## References
[[LPIC-1 Exam 101.pdf#page=]]