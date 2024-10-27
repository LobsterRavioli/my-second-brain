---
tags:
---

2024-09-17 16:35
Status:
Tags:
___
# Channel descriptor redirection

The channel descriptor redirection is an action done by the shell done when it changes file channel's descriptor.

So here happen that with > symbol we are telling echo to using another stream flux a stream that referres to prova.txt.
```bash
echo "prova" > prova.txt
```
so prova.txt it becomes a new target

We can redirect the stdout


| Stream                                                             | Redirection |
| ------------------------------------------------------------------ | ----------- |
| redirect stdout                                                    | 1> or >     |
| redirect stderr                                                    | 2>          |
| redirect stout and stderr                                          | &>          |
| redirect stdout to stdout                                          | 1>&1        |
| redirect redirect stdout to stderr                                 | 1>&2        |
| Pass the string to stdin                                           | <<<         |
| Pass a document you will creare at runtime                         | <<          |
| Connect the output from a command to the input from another commad | \|          |
|                                                                    |             |

Here some examples:

- Here doc redirection usage
```bash
wc -c <<EOF
> How many characters
> in this Here document?
> EOF
43
```

```bash
wc -c <<<"How many characters in this Here string?"
41
```


___
## References
[[LPIC-1 Exam 101.pdf#page=]]