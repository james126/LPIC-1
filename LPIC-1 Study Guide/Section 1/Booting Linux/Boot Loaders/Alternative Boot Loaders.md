# Alternative Boot Loaders

### The Linux Kernel
* Since version 3.3.0 it has incorporated an EFI boot loader for *x86* and *x86-64* systems
* on EFI computers, this lets the kernel serve as its own boot loader
* eliminates the need for a separate tool like GRUB
<span>&nbsp;</span>

### Damaged Boot Loader
Linux sometimes becomes unbootable if the boot loader becomes damaged
1. Try booting from the USB you used to install the OS, and look for an option to boot a kernel from the hard dist
2. once the system is booted, you can use `grub-install` to reinstall GRUB
3. The USB may also provide a recovery option