---
tags:
  - commands
type: gnu_and_unix_commands
description: decompress to stdout
Date: "{{date}} {{time}}"
weight:
---
___
# `bzcat`

## Syntax
```bash
bzcat [options] filename.bz2
```

## Description
`bzcat` is a command used to decompress files that have been compressed using the `bzip2` algorithm. Unlike `bzip2 -d`, which decompresses files to disk, `bzcat` decompresses the file and writes the output directly to standard output, allowing users to view or manipulate the content without creating a decompressed file on the filesystem.

## Options

| Option | Functionality              |
| ------ | -------------------------- |
| `-q`   | Quiet mode; suppress warnings. |
| `-v`   | Verbose mode; display more detailed information. |
| `-k`   | Keep the original compressed file. |

## Examples
- Decompress a `.bz2` file and display its contents:
```bash
bzcat file.bz2
```

- Use `bzcat` to pipe the decompressed output into another command (e.g., viewing the contents of a compressed file using `less`):
```bash
bzcat file.bz2 | less
```

___
## References
[[LPIC-1 Exam 101.pdf#page=]]