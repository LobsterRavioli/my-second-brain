---
tags:
  - commands
type: gnu_and_unix_commands
description: utility for copy in, copy out the files in archive modules.
Date: 2024-09-16 17:19
weight: "4"
---

___
# cpio

This utility is used for copy content from an archive or extract files from that.

Use cases:

- Create an archive
```bash
ls | cpoo -o > archive.cpio
```

- Extract an archive
```bash
cpio -ie < archive.cpio
```


___
## References
[[LPIC-1 Exam 101.pdf#page=]]