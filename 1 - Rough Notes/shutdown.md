---
tags:
  - commands
type: system_architecture
description: Used for shutdown the system and send messages to the users
weight:
---

2024-09-12 22:48
Status:
Tags: [[System Architecture]], [[1 - Rough Notes/Commands]]
___
# shutdown

The shut down command is used for shutting down the system.
The commands follow this syntax.
```
shutdown [option] time [message]
```
The shutdown command will notify all the user of the system that he will shutdown.
After shutdown is executed it will give a `SIGTERM` signal to all the processes of the system.
![[Pasted image 20240913111045.png | 200x 200]]

after that will follow a `SIGKILL`.
![[Pasted image 20240913111404.png | 200x200]]

___
## References
[[LPIC-1 Exam 101.pdf#page=]]