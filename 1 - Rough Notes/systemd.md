2024-09-12 16:00
Status:
Tags:
___
# systemd

Systemd is a service manager that controls [[Daemon |daemons]] and system resources, which are referred to as units by systemd.
Is the _first process_ to start by the kernel.
A unit consist of a name, a type and a corresponding configuration file.
For example a unit for httpd server will be httpd.service.

There are many typed of unit:

- **service**: The most common unit type.
- **socket**: network socket.
- **device**: a device unit is associated with a hardware device identified by the kernel.
- **[[Systemd Mount units|mount]]**: a mount point definition.
- **[[Systemd auto-mount unit|auto-mount]]**: a mount point mounted automatically.
- **target**: a group of others unit managed as a single unit.
- **snapshot**: a snapshot of a state of systemd

Systemd could be managed trought [[systemctl]] command.
___
## References
[[LPIC-1 Exam 101.pdf#page=]]