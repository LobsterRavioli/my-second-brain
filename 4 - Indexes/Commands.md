2024-09-12 22:49
Status:
Tags:
___
# Commands

# System architecture
```dataview 
TABLE description, weight
FROM #commands  
WHERE type="system_architecture"
SORT weight desc
```
___
# Linux installation and Package Management

```dataview 
TABLE description, weight
FROM #commands  
WHERE type="linux_installation_and_package_management"
SORT weight desc
```

# GNU AND UNIX COMMANDS

```dataview 
TABLE description, weight
FROM #commands  
WHERE type="gnu_and_unix_commands"
SORT weight desc
```


# CREATE PARTITION AND FILE SYSTEM

```dataview 
TABLE description, weight
FROM #commands  
WHERE type="create_partitions_and_filesystems"
SORT weight desc
```

# Temporary Files

Temporary files are files used by programs to store data that are only needed for a short time.
Crash logs, running processes, intermediary files used during a file conversion, cache files and such.
### Temporary files location
- `/tmp`: programs assume that files written ehere will be preserved between invocations of a program. This directory can be cleared duting system boot-up.
- `/var/tmp`: Another location for temporary files, this should no be cleared during system boot-up. Files store here usually persist between reboots.
- `/run`: Contain all run-time variable data used by running processes, such .pid files, this should be cleared during system boot-up.
## References
[[LPIC-1 Exam 101.pdf#page=]]