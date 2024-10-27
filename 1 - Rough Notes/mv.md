---
tags:
  - commands
type: gnu_and_unix_commands
description: move the file from a location to another
Date: 2024-09-16 15:08
weight: "4"
---

___
# mv

The move utility is used for moving files.
It follows this pattern.
```bash
mv FILENAME DESTINATION_DIRECTORY
```

- For secure moving, it will seek you a confirmation for overwrite files.
```bash
mv -i old_file_name new_file_name
```

- For force moving.
```bash
mv -f old_file_name new_file_name
```


___
## References
[[LPIC-1 Exam 101.pdf#page=]]