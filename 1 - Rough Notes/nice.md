---
tags:
  - commands
type: 
description: influence task scheduler priority.
Date: 2024-09-19 11:24
weight: "2"
---

___
# nice

## Syntax
```bash
nice [command/process]
```

## Description

This command change the "nicer" value associated to the command or process we're gonna change.
In a range from 0-19 for normal used and -20-19 for sudo user.
By default it changes the nicer value to 10.
We can take a look using using `ps -el`,  there's a column dedicated to priority and to the nice value, the changes of the nicer value influence the priority value.
The more the nicer value is high the more it will be "nice" for giving resources to others processes in the scheduler.
![[Screenshot 2024-09-19 alle 11.33.55.png]]

## Option

| Option | functionallity          |
| ------ | ----------------------- |
| -n     | specify the nicer level |

## Examples
- Change the tar command task priority
```bash
nice -n 15 tar czf home_backup.tar.gz /home
```
___
## References
[[LPIC-1 Exam 101.pdf#page=]]