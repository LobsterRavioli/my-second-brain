---
tags:
  - commands
type: linux_installation_and_package_management
description: list the shared libraries of the program
Date: 2024-09-13 16:33
weight: "1"
---

___
# ldd

`ldd` command is used for listing the dependencies of a program:
```bash
$ ldd /usr/bin/git
    linux-vdso.so.1 =>  (0x00007ffcbb310000)
	libpcre.so.3 => /lib/x86_64-linux-gnu/libpcre.so.3 (0x00007f18241eb000)
	libz.so.1 => /lib/x86_64-linux-gnu/libz.so.1 (0x00007f1823fd1000)
	libresolv.so.2 => /lib/x86_64-linux-gnu/libresolv.so.2 (0x00007f1823db6000)
	libpthread.so.0 => /lib/x86_64-linux-gnu/libpthread.so.0 (0x00007f1823b99000)
	librt.so.1 => /lib/x86_64-linux-gnu/librt.so.1 (0x00007f1823991000)
	libc.so.6 => /lib/x86_64-linux-gnu/libc.so.6 (0x00007f18235c7000)
	/lib64/ld-linux-x86-64.so.2 (0x00007f182445b000)
```

we could use ldd for share the dependencies od shared objects too:

```
$ ldd /lib/x86_64-linux-gnu/libc.so.6
	/lib64/ld-linux-x86-64.so.2 (0x00007fbfed578000)
	linux-vdso.so.1 (0x00007fffb7bf5000)

```

Or the unused dependencies:

```
$ ldd -u /usr/bin/git
Unused direct dependencies:
	/lib/x86_64-linux-gnu/libz.so.1
	/lib/x86_64-linux-gnu/libpthread.so.0
	/lib/x86_64-linux-gnu/librt.so.1
```


___
## References
[[LPIC-1 Exam 101.pdf#page=]]