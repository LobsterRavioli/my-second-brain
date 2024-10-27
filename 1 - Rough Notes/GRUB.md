2024-09-12 12:36
Status:
Tags:
___
# GRUB

GRUP  is a bootloader for linux x86 architecture.
From the GRUB menu we could change some kernel parameters that follow the pattern `option=value`.

Some of the most useful:

- `acpi`
	- Enable and disable ACPI support.
- `init`
	- Sets an alternative system initiator, for exaple `init=/bin/bash` will set the Bash shell as the initiator. A Ball session will start after he kernel boots up/
- `systemd.unit`
	- Sets the systmd target
- `mem`
	- Sets the amount of avaible RAM for the system.
- `maxcpus`
	- Limits the number of processors visible to the system in symmetric multi-processor machines.
- `quiet`
	- hides most boot messages
- `vga`
	- Selects a video mode.
- `root`
	- Sets the root partition
- `rootflags`:
	- Mount option for the root filesystem.
- `ro`
	- Makes the initial mount of the root filesystem read-only
- `rw`
	- Allows writing in the root filesystem durin initial mount

![[Screenshot 2024-10-18 alle 10.22.10.png]]
![[Screenshot 2024-10-18 alle 10.22.20.png]]


___
## References
[[LPIC-1 Exam 101.pdf#page=]]