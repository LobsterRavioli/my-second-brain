---
tags:
  - commands
type: gnu_and_unix_commands
description: make a check sum using sha256 algorithm.
Date: 2024-09-15 16:35
weight: "2"
---

___
# sha256sum

sha256sum make the checksum of a file.

- Calculate the checksum
```bash
sha256sum ftu.txt
```

- Check the integrity of the file (calculate the checksum of the file and then see if its is equal to the content of the file text)
```bash
sha256sum ftu.txt > sha256.txt
sha256sum -c sha256.txt
```

___
## References
[[LPIC-1 Exam 101.pdf#page=]]