---
tags:
---

2024-09-17 18:29
Status:
Tags:
___
# Command Substitution

The command substitution is a method to capture the output from a command.
It happens using backticks and using `$()` backquotes.
```bash
mkdir `date +%Y-%m-%d`
```

```bash
mkdir $(date +%Y-%m-%d)
```

___
## References
[[LPIC-1 Exam 101.pdf#page=]]