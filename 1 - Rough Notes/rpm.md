---
tags:
  - commands
type: linux_installation_and_package_management
description: command for manage .rpm file format
Date: 2024-09-15 07:04
weight: "3"
---

___
# rpm

RPM is the packet manager from redhat based systems.
With rpm command you could manage, install and remove packages.

- Install a package
```bash
rpm -i package_name
```

- update a package
```bash
rpm -U package_name
```

- Info about output processes
```bash
rpm -qi package_name
```

- Erase/Remove the package
```bash
rpm -e package_name
```

- List all the packages from the system (query-list)
```bash
rpm -qa package_name
```

- Info about a local package (query info)
```bash
rpm -qi package_name
```

- List files from a local package
```bash
rpm -ql package_name
```

- Info about a not local package
```bash
rpm -qip package_name
```

- List files from a not local package
```bash
rpm -qlp package_name
```

- See the package owner of the file.

```bash
rpm -qf /path/file
```

- Show in which path program will be installed.
qpl stands for *Query package list*
```bash
rpm -qpl program
```

Show all installed packages:
qa stands for*query all*
```bash
rpm -qa
```
___
## References
[[LPIC-1 Exam 101.pdf#page=]]