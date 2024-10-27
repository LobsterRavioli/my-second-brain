---
tags:
  - commands
type: gnu_and_unix_commands
description: translates, do conversion deletes characters from stdin to stdout.
Date: 2024-09-16 10:16
weight: "2"
---

___
# tr

The translate command translates or deletes characters from standard input and writes the result the stdout.
It is used to perform conversion, squeezing and deleting characters and basic text replacement.
tr command can't read the file directly and outputs the results in stdouts it is used with | pipes.

Practically you give him an input 2 sets like {abc} and {ABC} then he will swap the letters
in the text a->A, b->B, c->C.

- Character conversion
```bash
tr WWW www
```

- Convert uppercase character to lower case
```bash
cat file.txt | tr A-Z a-z
```

There's some default sets.
```bash
cat file.txt | tr [:upper:] [:lower:]
```

- Character deletion

```bash
cat file.txt | tr -d e
```


___
## References
[[LPIC-1 Exam 101.pdf#page=]]