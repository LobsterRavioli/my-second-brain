---
tags:
  - commands
type: gnu_and_unix_commands
description: concatenate input files
Date: 2024-09-15 11:52
weight: "2"
---

___
# cat

cat concatenate input files.

Pretty much all of your text manipulation programs will get text from a standard input (_stdin_), output it to a standard output (_stdout_) and send eventual errors to a standard error output (_stderr_).

You could do some tricks with redirection, you could redirect the input taken from stdin to the file.txt
```bash
cat > file.txt
This is a test
I hope cat is storing this to mytextfile as I redirected the output
I will hit ctrl+c now and check this
^C
```

or just tell to cat to redirect the file to stdout like this:

```bash
cat file.txt
```

or you can copy a content from a file to another.

```bash
cat mytextfile > newfiletext
```


___
## References
[[LPIC-1 Exam 101.pdf#page=]]