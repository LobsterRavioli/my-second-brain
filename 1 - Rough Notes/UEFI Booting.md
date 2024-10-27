2024-09-12 11:51
Status:
Tags:
___
# UEFI Booting

The [[UEFI]] booting is really similiar to [[BIOS booting]] with the only difference that the uefi has an internal storage for loading up the bootsrap and does not depend from a storage device.

So the step when the pc start up are these.

1. UEFI check for hardware failures
2. UEFI activate hardware peripherals like monitor and keyboards
3. UEFI load up the bootstrap (a predefined application placed in the NVRAM) from his NVRAM.
4. The pre-defined EFI application is a bootloader and it will load the kernel.


___
## References
[[LPIC-1 Exam 101.pdf#page=]]