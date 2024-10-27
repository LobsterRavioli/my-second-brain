---
tags:
---

2024-09-15 11:40
Status:
Tags:
___
# Quoting

Quoting is important when we have inputs for bash commands with special character like space.

In this kinda situation, this command will create 3 files.:
```
$ touch one two three
```

We can avoid that using double quotes like:

```
$ touch "one two three"
```

or using escape character

```bash
$ touch my\ big\ file
```
___
## References
[[LPIC-1 Exam 101.pdf#page=]]