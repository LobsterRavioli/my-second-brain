---
tags:
  - commands
type: create_partitions_and_filesystems
description: create file partitions on PGPT and MBR disks.
Date: 2024-09-20 11:59
weight: "2"
---

___
# parted

## Syntax
```bash
parted [options] [device [command [options...]...]]
```

## Description
Parted is a disk partitioning and partition resize program it has a cli for doing the partition creation process.

### Getting infos
```bash
(parted) print
Model: ATA CT120BX500SSD1 (scsi)
Disk /dev/sda: 120GB
Sector size (logical/physical): 512B/512B
Partition Table: msdos
Disk Flags:

Number  Start   End    Size    Type     File system     Flags
 1      2097kB  116GB  116GB   primary  ext4
 2      116GB   120GB  4295MB  primary  linux-swap(v1)
```

```bash
(parted) print devices
 2      116GB   120GB  4295MB  primary  linux-swap(v1)
```

```bash
(parted) print free
```

### Creating a Partition Table on an Empty Disk
- Decide the partition table as msdos.
```bash
(parted) mklabel msdos
```
- Decide the partition table tye as [[GUID partition table]].
```bash
(parted) mklabel gpt
```

### Creating a Partition
The command to give in input at this stage will follow this format:
```bash
mkpart PARTTYPE FSTYPE START END
```

| **Parameter** | **Description**                                                                                                                                                        |
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `PARTTYPE`    | The partition type, which can be **primary**, **logical**, or **extended** (for MBR partition table).                                                                   |
| `FSTYPE`      | Specifies the filesystem for the partition. Parted does not create the filesystem but sets a flag indicating the type of data expected by the OS.                        |
| `START`       | Specifies where the partition begins on the device. You can use units like **s** (sectors), **m** (megabytes), **B** (bytes), or **%** (percentage of the disk).         |
| `END`         | Specifies the end of the partition. This is the point on the disk where the partition finishes, using the same units as the START parameter (e.g., 100m, 50%).           |
Example:
```bash
(parted) mkpart primary ext4 1m 100m
```
### Removing a Partition
To remove a partition, use the command `rm` followed by the partition number, which you can display using the `print` command. So, `rm 2` would remove the second partition on the currently selected disk.

### Recovering a partition

```bash
(parted) rescue 90m 210m
Information: A ext4 primary partition was found at 99.6MB -> 200MB.
Do you want to add it to the partition table?

Yes/No/Cancel? y
```

## Option

| Option | functionallity |
| ------ | -------------- |
|        |                |

___
## References
[[LPIC-1 Exam 101.pdf#page=]]