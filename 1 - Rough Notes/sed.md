---
tags:
  - commands
type: gnu_and_unix_commands
description: filter text file in place or to stdout.
Date: 2024-09-15 16:02
weight: "2"
---

___
# sed

## Syntax 

```bash
sed [options] 'command1' [files]
sed [options] -e 'command1' [-e 'command2' ...] [files]
sed [options] -e 'command1'
sed [options] -f script [files]
```
# Description
Stream editor is an editor for transforming text in files using predefined patterns.
The command string are addresses where addresses could be:
- A line number, last in line indicated with $ or a range like this $1,$$.
- A regular expression is represents like this `/regex/` 

After presenting the address you could specify the file editing operation.
- `d` : delete lines
- `s`: make substitutions, where the syntax is as follows:
	- `s/pattern/replacement/flag`
	- Where the flag could be:
		- `g`: replace all instances of pattern
		- `n`: replace nth instance of pattern
		- `p`: print the line if a succesfull substitution is done.
		- `w` file
		- `y`: translate characters.




Is like the inverse of grep its kinda equal at this command

```bash
zcat ftu.txt.gz | grep -v cat
```

Here is its some use cases.

- Alternative from [[grep]]
```bash
sed -n /cat/p < ftu.txt
```

- Inverse of [[grep]]
```bash
sed -n /cat/p < ftu.txt
```

- Substitute words 
```bash
sed s/cat/dog/ < ftu.txt
```

- In place substitution with the backup file
```bash
sed -i.backup s/cat/dog/ ftu.txt
ls ftu
ftu.txt  ftu.txt.backup
```





___
## References
[[LPIC-1 Exam 101.pdf#page=]]