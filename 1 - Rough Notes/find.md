---
tags:
  - commands
type: 
description: find files.
Date: 2024-09-16 16:00
weight: "4"
---

___
# find

The find files find files in the file system.
It follows this pattern:

```bash
find STARTING_PATH OPTIONS EXPRESSION
```

Where:
- STARTING_PATH: is the pattern where the search start. 
- OPTIONS: is the flag for optimize the search.
- EXPRESSION: the expression used for search it could be a wildcard too.

Option used for optimizing the search
- `-type`
	- `-type f`: search for files
	- `-type d`: search for directories
	- `-type l`: search for symbolic link

- `-name`: perform a search based on a name
- `-iname`: perform a search based on a nome not case sensitive
- `-not`: return the files that did not match the test case
- `-maxdepth N`: searches from the current directory and search for a maximum child folders of N.

- `-mtime N`: where N stands for the last modify. 
- `-size N`: where n stands for the size of the file
	- `-size 100b`: file of 100 byte
	- `-size +100k`: file size of more then 100 kbytes
	- `-size -20M`: file size less then 20 megabytes
	- `-size + 2G`: file size less the 2 gigabytes.

- -`delete`: used for remove the file finded.

There's a really fucking strong option!
The -exec god function.
Yeah you got it you can execute fucking commands on the searched file like this:
```bash
find . -name "*.conf" -exec chmod 644 '{}' \;
```

Here's there another example:
```bash
find . -type f -exec grep "lpi" '{}' \; -print
```

So, every time find locates a file, it uses that file in place of {} and runs grep on that file.
if in the current directory you have two files named file1.txt and file2.txt, and you want to search for the string “lpi” inside those files, the braces would be replaced like this:
• grep "lpi" file1.txt
• grep "lpi" file2.txt
In summary: the curly braces {} in the command represent the file found by find.



___
## References
[[LPIC-1 Exam 101.pdf#page=]]