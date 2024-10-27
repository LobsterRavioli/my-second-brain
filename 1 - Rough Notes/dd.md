---
tags:
  - commands
type: gnu_and_unix_commands
description: copy content from a file to another.
Date: 2024-09-16 17:26
weight: "4"
---

___
# dd

dd is used for copying data from a location to another.


- Copy content from a file to another
```bash
dd if=oldfile of=newfile
```

- Copy test and capitalize it
```bash
dd if=oldfile of=newfile conv=ucase
```

- Backup the hardisk
```bash
dd if=/dev/sda of=backup.dd bs=4096
```



___
## References
[[LPIC-1 Exam 101.pdf#page=]]