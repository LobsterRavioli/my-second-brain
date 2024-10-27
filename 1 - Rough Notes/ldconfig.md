---
tags:
  - commands
type: manage_shared_libraries
description: 
Date: 2024-09-13 16:14
Status:
---

___
# ldconfig

ldconfig is a command for updating the cache of Linker after edited the[[Linked Dependencis| /etc/ld.so.conf]] config file.

- Display all the linked dependencies created
```bash
sudo ldconfig -v
/usr/local/lib:
/lib/x86_64-linux-gnu:
    libnss_myhostname.so.2 -> libnss_myhostname.so.2
	libfuse.so.2 -> libfuse.so.2.9.7
	libidn.so.11 -> libidn.so.11.6.16
	libnss_mdns4.so.2 -> libnss_mdns4.so.2
	libparted.so.2 -> libparted.so.2.0.1
	(...)
```

- Display all the dependencies in the current cache:
```bash
sudo ldconfig -p
1094 libs found in the cache `/etc/ld.so.cache'
    libzvbi.so.0 (libc6,x86-64) => /usr/lib/x86_64-linux-gnu/libzvbi.so.0
	libzvbi-chains.so.0 (libc6,x86-64) => /usr/lib/x86_64-linux-gnu/libzvbi-chains.so.0
	libzmq.so.5 (libc6,x86-64) => /usr/lib/x86_64-linux-gnu/libzmq.so.5
	libzeitgeist-2.0.so.0 (libc6,x86-64) => /usr/lib/x86_64-linux-gnu/libzeitgeist-2.0.so.0
	(...)
```

- Caches use the sonoma of the links
```bash
$ sudo ldconfig -p | grep libfuse
	  libfuse.so.2 (libc6,x86-64) => /lib/x86_64-linux-gnu/libfuse.so.2
```

___
## References
[[LPIC-1 Exam 101.pdf#page=]]