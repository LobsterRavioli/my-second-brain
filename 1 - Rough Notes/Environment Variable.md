---
tags:
---

2024-09-15 11:20
Status:
Tags:
___
# Environment Variable

Environment Variable are key-value pairs used by the operating system to store configuration information for the shell, programs, and services running on a system. These variables help define the environment in which processes run and are commonly used to control the behavior of the system or individual applications.

To define an environment variable:

```bash
myvar=hello
```

This variable is visible only in the current shell.
For make this variable to child shells we need to export like this:
```bash
export myvar

```

___
## References
[[LPIC-1 Exam 101.pdf#page=]]