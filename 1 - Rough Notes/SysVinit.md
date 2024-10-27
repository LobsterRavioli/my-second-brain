2024-09-12 15:57
Status:
Tags:
___
# SysVinit

SysVinit is a [[Service Manager]] that provide a set of system states, called run levels, and their corresponding service script files to be executed.
RunLevels are numbered to 0 to 6:

- **Run level 0**: System shutdown.
- **Run level 1**: Single user mode.
- **Run level 2, 3 o 4**: Multi-user mode.
- **Run level 5**: Multi-user mode.
- **Run level 6**: System restart.

The program responsible for managing run levels and associated daemon/resources is /sbin/init.

During boot up the system, the init program identifies the requested run level, defined by a kernel `parameter` or int he `/etc/inittab` .

Run-levels have x services attached.

The syntax of inittab is this:

```
id:runlevels:action:process
```

Here an example:

```
# Default runlevel
id:3:initdefault:

# Configuration script executed during boot
si::sysinit:/etc/init.d/rcS

# Action taken on runlevel S (single user)
~:S:wait:/sbin/sulogin

# Configuration for each execution level
l0:0:wait:/etc/init.d/rc 0
l1:1:wait:/etc/init.d/rc 1
l2:2:wait:/etc/init.d/rc 2
l3:3:wait:/etc/init.d/rc 3
l4:4:wait:/etc/init.d/rc 4
l5:5:wait:/etc/init.d/rc 5
l6:6:wait:/etc/init.d/rc 6

# Action taken upon ctrl+alt+del keystroke
ca::ctrlaltdel:/sbin/shutdown -r now

# Enable consoles for runlevels 2 and 3
1:23:respawn:/sbin/getty tty1 VC linux
2:23:respawn:/sbin/getty tty2 VC linux
3:23:respawn:/sbin/getty tty3 VC linux
4:23:respawn:/sbin/getty tty4 VC linux

# For runlevel 3, also enable serial
# terminals ttyS0 and ttyS1 (modem) consoles
S0:3:respawn:/sbin/getty -L 9600 ttyS0 vt320
S1:3:respawn:/sbin/mgetty -x0 -D ttyS1

```

the command `telinit q` should be runned every time this file is edited.



___
## References
[[LPIC-1 Exam 101.pdf#page=]]