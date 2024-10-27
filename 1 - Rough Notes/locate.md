---
tags:
  - commands
type: create_partitions_and_filesystems
description: search on the cache created by updatedb
Date: 2024-09-23 17:21
weight: "2"
---

___
# locate

## Syntax
```bash
locate string_pattern
```

## Description
It's like the [[find]] command but the search is done on the index created on [[updatedb]].


## Option

| Option | functionallity                             |
| ------ | ------------------------------------------ |
| -e     | check if the file exist in the file-system |


## Examples
- 
```bash
locate -c .jpg
```
- 
```bash
locate -A .jpg .zip
```
___
## References
[[LPIC-1 Exam 101.pdf#page=]]