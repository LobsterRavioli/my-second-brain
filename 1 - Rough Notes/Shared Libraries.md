---
tags:
---

2024-09-13 15:43
Status:
Tags:
___
# Shared Libraries

Shared Libraries are [[Dependencies]] are program dependencies.
They are dynamically called by a dynamic linker when the program is calling some code owned my this library.
They're used to reduce the over head on the system reducing the size of the program file, only one copy of the library is loaded in memory when it used by multiple programs.
They're also called soname, their name follow a pattern.
- lib (normallu prefixed by lib)
- so (stands for "shared object")
- Version number of the library

Here an example: Libpthread.so.0

Common location of shared Libraries are:
- /lib
- /lib32
- /lib64
- /usr/lub
- /usr/local/lib


___
## References
[[LPIC-1 Exam 101.pdf#page=]]