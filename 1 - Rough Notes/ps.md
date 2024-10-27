---
tags:
  - commands
type: gnu_and_unix_commands
description: list all current processes associated to bash and user.
Date: 2024-09-18 11:26
weight: "4"
---

___
# ps

## Syntax
```bash
ps [options]
```

## Description
It shows a snapshot or the current processes.

## Option

| Option    | functionallity                                                                                                |
| --------- | ------------------------------------------------------------------------------------------------------------- |
| `-a`      | Show processes that are running on the system associated that are running by user on the respictive terminals |
| `-f`      | Full format of the ps ouput, shows the PID too.                                                               |
| -u        | User format of the ps ouput, it shows username and start time of the process                                  |
| `-w`      | Wide format of the ps output                                                                                  |
| `-x`      | shows all the processes not related to the current bash session, stuff like daemon.                           |
| `-C cmd`  | display instances of commands                                                                                 |
| _U user_  | display processes owned by username user.                                                                     |
| `-e`      | show all system processes                                                                                     |
| `-o`      | custom the output and specify the fields.                                                                     |
| `--sort=` | sort processes by a field.                                                                                    |
## Output interpretation

### Process Information

- **USER**: Owner of process
- **PID**: Process identifier
- **%CPU**: Percentage of CPU used
- **%MEM**: Percentage of physical memory used
- **VSZ**: Virtual memory of process in KiB
- **RSS**: Non-swapped physical memory used by process in KiB
- **TT**: Terminal controlling the process (tty)
- **STAT**: State of the process and any additional modifiers
- **STARTED**: Time at which the process started
- **TIME**: Accumulated CPU time
- **COMMAND**: Command that started the process

---
### Description of `STAT` codes:

- **S**: Sleeping
- **R**: Running
- **Z**: Zombie
- **D**: Uninterruptible sleep (usually waiting for I/O)
- **T**: Stopped (normally by a control signal)
- **<**: High-priority (not nice to other processes)
- **N**: Low-priority (nice to other processes)
- **+**: Foreground​

___

## Examples
- Show a snapshot of processes
```bash
ps -a
```
- Options do not follow any leading dash
```bash
ps p 811
```
- Option s are followed by double dashes:
```bash
ps --pid 811
```
- Check the process of a user:
```bash
ps U user
```
- Show processes that are attached to a tty or terminal, Display user-oriented format, show processes that are no attached to a tty terminal.
```bash
ps aux
```

## References
[[LPIC-1 Exam 101.pdf#page=]]
[[Lpi Linux Certification In A Nutshell 3rd Edition.pdf#page=129]]