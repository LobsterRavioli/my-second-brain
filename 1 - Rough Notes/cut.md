---
tags:
  - commands
type: gnu_and_unix_commands
description: cut is used for cut bytes by position, fields or characters.
Date: 2024-09-15 17:46
weight: "2"
---

___
# cut

the cut command is used for filter text files.
He can manipulate columns veri easily.

- Cut a column from a file text with -c.
```bash
cut -c1 file.txt
```

- Cut a known portion from the columns
```bash
cut -c1-4 file.txt
```

- Cut the rest of the column after the third column.
```bash
cut -c3- file.txt
```

- Cut the rest before the range the third column
```bash
cut -c-3 file.txt
```

- Cut the third field from the splitting with ":" delimiter
```bash
cut -d : -f3 file.txt
```

- Cut the third and fourth field from the splitting with ":" delimiter
```bash
cut -d : -f3,4 file.txt
```

- Cut the third and fourth field from the splitting with "U" delimiter, when there's no "U" delimiter just skip.
```bash
cut -d U -s -f3,4 file.txt
```

- Cut all fields except the third (complementary) field from the splitting with "U" delimiter, when there's no "U" delimiter just skip.
```bash
cut -d U --complements -s -f3 file.txt
```

___
## References
[[LPIC-1 Exam 101.pdf#page=]]