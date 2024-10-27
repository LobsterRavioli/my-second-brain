---
tags:
  - commands
type: gnu_and_unix_commands
description: replace end line character and format in columns.
Date: 2024-09-16 09:18
weight: "2"
---

___
# paste

the utility paste is used for default is used for make columns or replace the endline character character.

- List the files in the current directory in three columns:  
```bash
ls | paste - - -
```
- Replace end line character with ,
```bash
paste -s -d , file.txt
```

___
## References
[[LPIC-1 Exam 101.pdf#page=]]