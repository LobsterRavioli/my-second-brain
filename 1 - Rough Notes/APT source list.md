---
tags:
---

2024-09-15 06:02
Status:
Tags:
___
# APT source list

APT ask to his sources for downloading packages.
The sources are listed into a specific config file called `sources.list` .
The format of the sources are:
> [!NOTE]
> archive, URL, Distribution o 1 or more Components
> 

- Archive: Repositories containing the packages. (deb)
- URL: URL of the repository (http://us.archive.ubuntu.com/ubuntu/)
- Distribution: nome of the distribution that distribute packages. (disco)
- Components: Every components rely on the linux version

Like this example:

```bash
deb http://us.archive.ubuntu.com/ubuntu/ disco main restricted universe multiverse
```




___
## References
[[LPIC-1 Exam 101.pdf#page=]]