2024-09-11 14:40
Status:
Tags:
___
# Devices and drivers

[[lspci]] lista le periferiche connesse al bus pci.

```bash
lspci 
```

```bash
lspci -t
```

I devices sono visibile anche al seguente file:

/dev/sda

## Gestione dei drivers

For listing all the drivers of the system there is this command:

```bash
lsmod
```

That lists all the extensive kernel module.

And there is some other commands for manage these driver, we could load up a driver or mount down the driver.

- Mount down driver

```bash
rmmod driver_name
```

- Loud up driver

```bash
insmod path_driver_file
```

There is modprobe too that is easy to use:
- Mountdown driver
```bash
modprobe -r driver_name
```
- Loud up the driver
```bash
modprobe driver_name
```

insmod is more usefull when the driver or the kernel extensive file object is not in the "classic" path so the "lib/modules" path.

___
## References
