---
tags:
  - commands
type: 
description: 
Date: 2024-09-18 16:15
weight:
---

___
# top

## Syntax
```bash
top
```

## Description
The top utility is used for process monitoring
![[Screenshot 2024-09-18 alle 16.19.24.png]]
You can sort this table by:
- **M**: memory usage.
- **N**: PID.
- **T**: running Time.
- **P**: percentage Usage: CPU usage.
- **?**: help.
- k: kill a process.
- **u**: list by user.
- **c**: show programs absolute path and differentiate between userspace processes.
- **V**: Forest view of processes.
- **t**: Change the look of CPU and memory readings in four stage cycle.
- **W**: show top configuration.

## Summary area
- top - 11:10:29 up 2:21, 1 user, load average: 0,11, 0,20, 0,14
	- current time
	- uptime (how much time the system has been up running)
	- number of user logged in
	- number of users logged in and load average of the CPU for the last 1, 5 and 15 minutes, respectively.
- Tasks: 73 total, 1 running, 72 sleeping, 0 stopped, 0 zombie
		- total number of processes in active mode: `73 total`
		- running: number of processes in running state.
		- sleeping: number of processes in sleeping state.
		- stopped: number of processes in stopped state.
		- zombie: number of processes in zombie state.
- KiB Mem : 1020332 total, 909492 free, 38796 used, 72044 buff/cache (memory information in kilobyes)
		- total amount of memory
		- unused memory
		- memory use
		- the memory which is buffered and cached
- KiB Swap: 1046524 total, 1046524 free, 0 used. 873264 avail Mem
	- the total amount of swap space: `1046524 total`
	- unused swap space: `1046524 free`
	- swap space in use: `0 used`
	- the amount of swap memory that can be allocated to processes without causing more swapping: `873264 avail Mem`
	

## Task area
- `PID`:  [[Process ID]] of the process.
- `USER` User who issued the process.
- `PR` Priority of process of the kernel
- `NI` nice value of process
- `VIRT`: Total amount of memory used by process
- `RES`: Ram memory used by proces
- `SHR` Shared memory of the process with other process.
- `S` Status of process: S for sleep, R for runnable, Z for zombie.
- `%CPU`: CPU usage.
- `%MEM`: Percentage of RAM used by proces.
- `TIME+` Total time activity of process
- `COMMAND`: name of the command/program generated the process



## Option

| Option | functionallity                           |     |
| ------ | ---------------------------------------- | --- |
| -p     | to show specific processes with the pid. |     |
| -d     | set refresh rate                         |     |


## Examples


___
## References
[[LPIC-1 Exam 101.pdf#page=]]