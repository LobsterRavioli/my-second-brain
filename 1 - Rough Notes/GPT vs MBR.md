---
tags:
  - chapter
type: 
weight:
---

2024-10-20 12:10
Status:
Tags:
___
# GPT vs MBR

[[Master Boot Record]] ha diverse limitazioni.
- 2 tb per dischi
- al massimo 4 partizione primarie

[[GUID partition table]] non presenta queste limitazioni.
- 128 partizioni primarie
- Piu di 4 partizioni
- Le informazioni relative allo schema delle partizioni e' salvato in piu settori quindi e' piu resiliente
- Redundancy check
- [[parted]], [[gdisk]], 



___
## References
[[LPIC-1 Exam 101.pdf#page=]]