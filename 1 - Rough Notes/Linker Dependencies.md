---
tags:
---

2024-09-13 16:05
Status:
Tags:
___
# Linker Dependencies

The Dependencies are stored in a file called `/etc/ld.so.conf` .
This file point to a directory that contain `.conf` files.

```bash
$ cat /etc/ld.so.conf
include /etc/ld.so.conf.d/*.conf
```

The `.conf` files must include absolute paths to the shared library directory:

```bash
$ cat /etc/ld.so.conf.d/x86_64-linux-gnu.conf
# Multiarch support
/lib/x86_64-linux-gnu
/usr/lib/x86_64-linux-gnu
```

Every time we edit the /etc/ld.so.conf file we need to take care to update linker caches with [[ldconfig]] command.



___
## References
[[LPIC-1 Exam 101.pdf#page=]]