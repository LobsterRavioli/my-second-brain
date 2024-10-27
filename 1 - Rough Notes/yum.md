---
tags:
  - commands
type: linux_installation_and_package_management
description: advanced packet manager for redhat based, fedora, centos based systems
Date: 2024-09-15 09:12
weight: "3"
---

___
# yum

yum is a [[Packet Manager]] similar to [[APT | apt]] for Fedora, CentOS, Red Hat Enterprise Linux e Oracle Linux.

- Search of packets

```bash
yum install p7zip
```

- Installing packets
```bash
yum install p7zip
```

- Update packets
```bash
yum update p7zip
```

- See packet owner
```bash
yum whatprovides p7zip
```

- Get packet information
```bash
yum info p7zip
```

- List all repolist
```bash
yum repolist all
```
- Show all installed packages
```bash
yum list installed
```
# Manage packet repository

You can manage repos addinf `.repo` files to `/etc/yum.repos.d/` .
The suggested way is to use the yum-config-manager.
```bash
yum-config-manager --add-repo https://rpms.remirepo.net/enterprise/remi.repo
```

- Disabling the repo auto-update.
```bash
yum-config-manager --disable updates
```


- Enabling the repo auto-update.
```bash
yum-config-manager --enable updates
```

___
## References
[[LPIC-1 Exam 101.pdf#page=]]