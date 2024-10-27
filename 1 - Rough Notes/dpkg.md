---
tags:
  - commands
type: linux_installation_and_package_management
description: commands for manage .deb packages (debian packet manager).
Date: 2024-09-14 08:42
weight: "3"
---

___
# DPKG

DPKG is used for call the Package Manager and manages packages.

- For **install** the package
```bash
dpkg -i PACKAGENAME
```
Dove package name e' il path del file `.deb` da installare.

- For remove the package
```bash
dpkg -r PACKAGENAME
```

- For gain info from the package
```bash
dpkg -I PACKAGENAME
```

- For list package files.
```bash
dpkg -L PACKAGENAME
```

- Show the package owner of the file
```bash
dpkg -S PACKAGENAME
```

- To re launch the scipt of the package reconfiguration.
```bash
dpkg-reconfigure PACKAGENAME
```



___
## References
[[LPIC-1 Exam 101.pdf#page=]]