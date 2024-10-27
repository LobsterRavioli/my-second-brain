2024-09-23 16:59
Status:
Tags:
___
# Filesystem Hierarchy Standard

The Filesystem Hierarchy Standard is an effort by Linux Foundation to standardize the structure and directory contents on Linux systems.

The basic directory structure is as follows:


| Path   | Directory                                                                                                                                |
| ------ | ---------------------------------------------------------------------------------------------------------------------------------------- |
| /      | Root directory every folder of the system is contained here                                                                              |
| /bin   | Essential binaries avaible to all users.                                                                                                 |
| /boot  | Files needed by the boot process, including initial RAM Disk and the Linux [[kernel]].                                                   |
| /dev   | Device folders where physical devices and virtual devices are connected to the system provided by the kernel.                            |
| /etc   | Here's there's configuration files                                                                                                       |
| /home  | The home directory contains the folder of every user for store they're files.                                                            |
| /lib   | Share libraries needed to boot the operating system and for run binaries under /bin and /sbin                                            |
| /media | Use-mountable removable media, like flash drives, CD and CVC-ROM readers, gloppy disks, memory cards and extenal disks are mmounted here |
| /mnt   | Mount point for temporarily mounted filesystems.                                                                                         |
| /opt   | Application software packages                                                                                                            |
| /root  | Home directory for the superuser (root)                                                                                                  |
| /run   | Run-time variable data                                                                                                                   |
| /sbin  | System binaries                                                                                                                          |
| /srv   | Data served by the system                                                                                                                |
| /tmp   | Temporary files                                                                                                                          |
| /usr   | Read only user data needed by applications and utilities                                                                                 |
| /proc  | Viruatl filesystem containig data related to running processes.                                                                          |
| /var   | Variable data written during system operation                                                                                            |
| /usr   | installed softwarre                                                                                                                      |



___
## References
