---
tags:
  - commands
type: linux_installation_and_package_management
description: advanced packet manager.
Date: 2024-09-15 04:59
weight: "3"
---

___
# APT

APT stands for "Advanced Packet Manager" make more simple the management of the packages.

## apt-get

Command for interact with apt for downloading, installing and update or removing a package from a file system

- For install packages and their dependencies:
```bash
apt-get install package_name
```

- For remove the package and their dependencies:
```bash
apt-get remove package_name
```

- For a clean deletion
```bash
apt-get remove --purge package_name
```

- For removing the associated configuration file
```bash
apt-get purge package_name
```

- For fixing broke dependencies
```bash
apt-get install -f
```

- For update the [[Index of packages]] (metadata from the packages):
```bash
apt-get update package_name
```

# apt-cache

apt-cache command interact with the [[Index of packages]]

- Make a local search:
```bash
apt-cache search package_name
```

- Give infos about package:
```bash
apt-cache show package_name
```

# apt-file

- For searching a file from a packages:
```bash
apt-file list package_name
```

- For search for the package owner
```bash
apt-file search libSDL2.so
```


## apt

Update system packages, resolve dependencies 
apt full-update

Update meta information about packages\
apt upgrade

Remove unusued packages
apt autoremove
___
## References
[[LPIC-1 Exam 101.pdf#page=]]