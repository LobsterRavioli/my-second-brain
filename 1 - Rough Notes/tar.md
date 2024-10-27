---
tags:
  - commands
type: gnu_and_unix_commands
description: tar command used for compress and uncompress file.
Date: 2024-09-16 16:47
weight: "4"
---

___
# tar

tar is used  for compress and uncompress file.
It follows this pattern:

```bash
tar [OPERATION_AND_OPTIONS] [ARCHIVE_NAME] [FILE_NAME(S)]
```

# OPERATION

## `-create` (`-c`)
Create a new tar archive

## `-extract` (`-e`)
Extract the entire archive or one or more files from an archive

## `-list` (`-t`)
Display a list of the files included the archive.

# OPTIONS

## `--verbose` (`-v`)
Show the progress od the operation

## `--file=archive-name` (`-f archive-name`)
Specifies the archive file name
## `-z`
use gzip algorithm
## `-j`
use bzip2 algorithm

## ARCHIVE_NAME
Name of the archive

## FILE_NAME
Name of the file

## Some example

- Creating an archive
```bash
tar -cvf archive_name file_to_zip1 file_to_zip2 file_to_zip3
```

- Extract archive
```bash
tar -xvf archive.tar
```
___
## References
[[LPIC-1 Exam 101.pdf#page=]]