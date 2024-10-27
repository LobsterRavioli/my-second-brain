---
tags:
  - "#path"
type: create_partitions_and_filesystems
description: config file that contains filesystem to be mounted.
Date: 2024-09-20 16:23
path: /etc/fstab
---

___
# fstab

The file /etc/fstab contains description about the filesystem that can be mounted.
This is a text file, where each line describes a filesystem to be mounted..
The rows are in this format:

```bash
FILESYSTEM MOUNTPOINT TYPE OPTIONS DUMP PASS
```

Where:
- **FILESYSTEM**: specify the filesystem to be mounted, the UUID or label of the partition.
- **MOUNT-POINT**: Where the filesystem will be mounted.
- **OPTION**: Mount options that will be passed to mount.
- **TYPE**: Type of filesystem
- **DUMP**: Indicate the backup filesystem, zero will be ignored.
- **PASS**: When non-zero, defines the order in which the filesystems will be checked on boot-up, zero will be ignored.

### Mount option parameters

| **Option** | **Description**                                                                                                                   |
| ---------- | --------------------------------------------------------------------------------------------------------------------------------- |
| `atime`    | Updates the access time every time a file is read.                                                                                |
| `noatime`  | Disables updating the access time, which can speed up disk I/O.                                                                   |
| `auto`     | Allows the filesystem to be mounted automatically with `mount -a`.                                                                |
| `noauto`   | Prevents the filesystem from being mounted automatically with `mount -a`.                                                         |
| `defaults` | Applies default options: `rw`, `suid`, `dev`, `exec`, `auto`, `nouser`, and `async`.                                              |
| `dev`      | Allows character or block devices in the filesystem to be interpreted.                                                            |
| `nodev`    | Prevents character or block devices in the filesystem from being interpreted.                                                     |
| `exec`     | Permits execution of binaries on the filesystem.                                                                                  |
| `noexec`   | Prevents execution of binaries on the filesystem.                                                                                 |
| `user`     | Allows an ordinary user to mount the filesystem.                                                                                  |
| `nouser`   | Prevents an ordinary user from mounting the filesystem.                                                                           |
| `group`    | Allows a user to mount the filesystem if the user belongs to the group that owns the device.                                      |
| `owner`    | Allows a user to mount the filesystem if the user owns the device.                                                                |
| `suid`     | Allows the `SETUID` and `SETGID` bits to take effect.                                                                             |
| `nosuid`   | Prevents the `SETUID` and `SETGID` bits from taking effect.                                                                       |
| `ro`       | Mounts the filesystem as read-only.                                                                                               |
| `rw`       | Mounts the filesystem as writable.                                                                                                |
| `remount`  | Remounts an already mounted filesystem. Used with `mount -o remount,ro` to change the mount options without unmounting.           |
| `sync`     | Performs all I/O operations synchronously, which can slow down operations but may be useful in specific scenarios.                |
| `async`    | Performs I/O operations asynchronously (default). Be cautious when using `sync` on flash drives, as it may reduce their lifespan. |
# Example

```
# <file system>                             <mount point>  <type>  <options>         <dump>  <pass>
UUID=123e4567-e89b-12d3-a456-426614174000   /               ext4    defaults          0       1
UUID=890f1111-c678-90ab-d456-789012345678   /home           ext4    defaults          0       2
UUID=bcde2345-6789-4abc-9012-def34567890f   /mnt/backup     ext4    noatime           0       2
/dev/sda1                                   /boot           ext4    defaults          0       2
/dev/sdb1                                   none            swap    sw                0       0
/dev/cdrom                                  /mnt/cdrom      iso9660 ro,user,noauto    0       0
```

___
## References
[[LPIC-1 Exam 101.pdf#page=]]