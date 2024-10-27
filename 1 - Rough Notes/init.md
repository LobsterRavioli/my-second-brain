2024-09-12 15:52
Status:
Tags:
___
# init

The first program the kernell will run is the `init` program that is responsable for running all initialization scripts and system daemons.
The kernel after mounted all filesystem configured in `/etc/fstab`, will execute the init module.
There are distinct implementations of such system apart from traditionals init like [[systemd]] and [[Upstart]].
Once the init program is loaded, the [[initramfs]] is removed from RAM.
The init program has always a PID equal to 1 because it's the first program to be runned.
___
## References
[[LPIC-1 Exam 101.pdf#page=]]