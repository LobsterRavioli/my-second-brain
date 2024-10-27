---
tags:
---

2024-09-17 16:24
Status:
Tags:
___
# Linux system streams

Every process in linux has 3 communication channel opened by default:
- [[stdin]](standard input): the stream which programs read its input by default it's the keyboard.
- [[stdout]]: the stream which programs read its input by default it's the terminal/screen.
- [[stderr]]: the stream which programs read its input by default it's the terminal but can also redirected to another file.

The numerical file descriptors assigned to this file are:
- **stdin**: `0`
- **stdout**: `1`
- **stderr**: `2`

And these communication channels are also accessed from local devices:
- /dev/stdin/
- /dev/stdout
- /dev/stderr

The Bash shell can assign dinamically these channels when loading a program.
___
## References
[[LPIC-1 Exam 101.pdf#page=]]