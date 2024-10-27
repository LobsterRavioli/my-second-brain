---
tags:
  - commands
type: gnu_and_unix_commands
description: print the last 10 lines of the file.
Date: 2024-09-15 18:00
weight: "2"
---

___
# tail

tail commands print last 10 lines of the file.
You can use it for watching logs.

- to watch an existing file
```bash
tail -f text2.txt
```

- to watch a not existing file (when creating he will observe).
- to watch an existing file
```bash
tail -F text2.txt
```

- to watch multiple files.
```bash
tail -f text1.txt text2.txt
```
___
## References
[[LPIC-1 Exam 101.pdf#page=]]