2024-09-20 14:44
Status:
Tags:
___
# Filesystem superblock

A file system superblock contains all information about the file system and is written in block 1 of the partition.
If this are is corrupted the whole filesystem is inaccesile.
Becouse of the importance of the superblock, copies of this block are made in the folesystem at regular interval.
[[fsck]] use the information in the superblock copies to restore the main superblock.

___
## References
