---
tags:
  - commands
type: gnu_and_unix_commands
description: type is used for quickly get basic data from the command
Date: 2024-09-15 10:52
weight: "4"
---

___
# type

type will give you basic data from the command and the type of executable.

Like:

```bash
$ type uname cp kill which
uname is hashed (/bin/uname)
cp is /bin/cp
kill is a shell builtin
which is /usr/bin/which
```

the output of uname is this because it's already been used so the kernel for optimize the retrieval put that in an hash table for increase system efficiency.

# Options

| Options | Description                           |
| ------- | ------------------------------------- |
| -a      | Show all pathnames of the executable. |

___
## References
[[LPIC-1 Exam 101.pdf#page=]]