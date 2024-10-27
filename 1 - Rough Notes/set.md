---
tags:
  - commands
type: gnu_and_unix_commands
description: show local variables and functions.
Date: 2024-09-15 11:35
weight: "4"
---

___
# set

set is like [[env]] command and will show the local variables and function in an other format.
Unlike [[env]] set shows the local variable:

```bash
$ ynewvar=goodbye
$ env | grep mynewvar
					# It shows nothing

$ set | grep mynewvar
mynewvar=goodbye
```


___
## References
[[LPIC-1 Exam 101.pdf#page=]]