# The Boot Process

### Kernel Ring Buffer
kernel log messages
in-memory data structure
captures:
* boot messages
* event logging
* errors and warnings

> #### dmesg
> print or control kernel ring buffer
> `dmesg [options]`

<span>&nbsp;</span>

### The Boot Process
Steps when powering on a computer
1. system powered on
2. CPU runs firmware (BIOS or EFI)
3. firmware looks for *Boot Loader*
4. Boot Loader loads the kernel or chainloads to another boot loader
5. kernel initializes devices, mounts root partition and runs initial program for your system
