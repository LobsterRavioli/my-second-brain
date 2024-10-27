---
tags:
  - "#path"
type: linux_installation_and_package_management
description: folder for temporary files.
Date: 2024-09-13 12:09
Path: /var
---

___
# var folder

The var folder is located to `/var` stands for "variable data" and is used for storing temporary file, logs and caching files.

It should be a partition because this path could be access from many processes and a missleading process could write up all the space in this folder.

if this folder is under the root folder this can cause a kernel panic/

For a normal use this folder can takes a few of gb, it depends of the use case.
If there's a server running a database or a web server much more space is needed.

___
## References
https://learning.lpi.org/en/learning-materials/101-500/102/102.1/102.1_01/
[[LPIC-1 Exam 101.pdf#page=]]