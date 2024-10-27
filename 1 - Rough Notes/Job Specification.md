2024-09-18 12:29
Status:
Tags:
___
# Job Specification

The Job specification is a way to identify jobs.
It is used in various job controls utilities, like:
- [[jobs]]
- [[bg]]
- [[kill]]
It follows a notation
- `%n`
```bash
jobs %1
```
- `%str` job whose command line contains str
```bash
jobs %1
```

- `%?str` job whose command line start with str
```bash
jobs %1
```
- `%-`  previous job
```bash
jobs %1
```
-  `%%` or `%+`  Current job (the one that was last started in the backgroud or suspended from the foreground)
```bash
jobs %sl
```



___
## References
[[LPIC-1 Exam 101.pdf#page=]]