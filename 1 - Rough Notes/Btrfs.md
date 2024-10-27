2024-09-20 11:54
Status:
Tags:
___
# Btrfs

The B-Tree Filesystem is [[Filesystem]] that has been developed for Linux by the Oracle Corporation.

There are many features that make Btrfs attractive on modern systems where massive amounts of storage are common. Among these are multiple device support (including striping, mirroring and striping+mirroring, as in a RAID setup), transparent compression, SSD optimizations, incremental backups, snapshots, online defragmentation, offline checks, support for subvolumes (with quotas), deduplication and much more.

As it is a _copy-on-write_ filesystem it is very resilient to crashes. And on top of that, Btrfs is simple to use, and well supported by many Linux distributions. And some of them, like SUSE, use it as the default filesystem.

# Create a btrfs Filesystem

```bash
mkfs.btrfs /dev/sdb1
```


___
## References
