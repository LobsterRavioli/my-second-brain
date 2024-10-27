---
tags:
  - commands
type: linux_installation_and_package_management
description: packet manager for SUSE based systems.
Date: 2024-09-15 09:44
weight: "3"
---

___
# zypper

zypper is a packet manager forked from [[yum]] for SUSE Linux and OpenSUSE.

- zypper [[Index of packages]] update
```bash
zypper refresh
```

- Search for a package in repos and locally
```bash
zypper se gnumeric
```

- Search for a package only locally
```bash
zypper se -i firefox
```

- Install a package
```bash
zypper in unrar
```

- Installing local .rpm packages
```bash
zypper in /home/john/newpackage.rpm
```

- Remove a package (this will delete at cascade other dependencies package)
```bash
zypper rm unrar
```

- Get the owner package from the file
```bash
zypper se --provides /usr/lib64/libgimpmodule-2.0.so.0
```

- Get infos for from the package
```bash
zypper info gimp
```

- Get repos
```bash
zypper repos
```

- Enable/disable repos
```bash
zypper modifyrepo -d repo-non-oss
# Repository 'repo-non-oss' has been successfully disabled.

zypper modifyrepo -e repo-non-oss
# Repository 'repo-non-oss' has been successfully enabled.
```

- Add repo
```bash
zypper addrepo http://packman.inode.at/suse/openSUSE_Leap_15.1/ packman
```

- Remove repo
```bash
zypper removerepo packman
```
___
## References
[[LPIC-1 Exam 101.pdf#page=]]