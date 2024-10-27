---
tags:
  - chapter
type: 
weight:
---

2024-09-20 11:06
Status:
Tags:
___
# Process of creating partition using fdisk

1. Check your current disk
```bash
fdisk -l
```

2. Use it as input.
```bash
fdisk /dev/sda
```

3. Printing current partition table of the disk
```bash
Command (m for help): p
Disk /dev/sda: 111.8 GiB, 120034123776 bytes, 234441648 sectors
Disk model: CT120BX500SSD1
Units: sectors of 1 * 512 = 512 bytes
Sector size (logical/physical): 512 bytes / 512 bytes
I/O size (minimum/optimal): 512 bytes / 512 bytes
Disklabel type: dos
Disk identifier: 0x97f8fef5

Device     Boot     Start       End   Sectors   Size Id Type
/dev/sda1            4096 226048942 226044847 107.8G 83 Linux
/dev/sda2       226048944 234437550   8388607     4G 82 Linux swap / Solaris
```

4. Check free space
```bash
Command (m for help): F
Unpartitioned space /dev/sdd: 881 MiB, 923841536 bytes, 1804378 sectors
Units: sectors of 1 * 512 = 512 bytes
Sector size (logical/physical): 512 bytes / 512 bytes

  Start     End Sectors  Size
2099200 3903577 1804378  881M
```

5. Create a new partition
```bash
Command (m for help): n
Partition type
   p   primary (0 primary, 0 extended, 4 free)
   e   extended (container for logical partitions)
Select (default p): **p**
Partition number (1-4, default 1): **1**
First sector (2048-3903577, default 2048): **2048**
Last sector, +/-sectors or +/-size{K,M,G,T,P} (2048-3903577, default 3903577): +1G
```

Once the partition is created you need you need to install a file system using [[mkfs]] utility.

___
## References
[[LPIC-1 Exam 101.pdf#page=]]