---
tags:
  - commands
type: 
description: read from sdout and write to input files and stoud.
Date: 2024-09-17 18:17
weight: "4"
---

___
# tee

## Syntax
```bash
tee [option] files
```

## Description
Read from standard input and write both to one or more files and to stdout.

## Option

| Option | functionallity                               |
| ------ | -------------------------------------------- |
| `-a`   | Append to files rather then overwriting them |


## Examples
- show log of a command and store to a file(first we print stderr to sdout then we pipe it)
```bash
make 2>&1 | tea log.txt
```

- Results trough a pipeline of commands
```bash
cmd1 | tee file_cmd1 | cmd2 | cmd3
```
___
## References
[[LPIC-1 Exam 101.pdf#page=]]