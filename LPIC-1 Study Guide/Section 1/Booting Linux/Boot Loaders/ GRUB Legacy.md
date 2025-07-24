# GRUB Legacy

Boot Loader for Linux
Eclipsed by GRUB 2
<span>&nbsp;</span>

### Configuration
* configuration file `/boot/grub/menu.lst` 
* GRUBs root partition is the partition in which the configuration file exists
* normally `/boot/grub/`

#### Options
|||
|-|-|
| `default=` | default OS<br> 0 = first OS listed, 1 = second etc |
| `timeout=` | how long to wait for user input before booting the default OS |
<span>&nbsp;</span>

### Disk Drives
* Legacy GRUB numbers devices
* */dev/hda* becomes (hd0)
* */dev/hdb* becomes (hd1)
* */dev/hda* first partition becomes (hd0,0)
* drive mappings are found in */boot/grub/device.map*
<span>&nbsp;</span>

### Image Options
refers to the GRUB Boot Loaders executable code
|||
|-|-|
| `title` | **Title**<br> label to display when the boot loader runs |
| `root` | **GRUB Root**<br> location of GRUB root partition |
| `kernel` | **Kernel Specification**<br> location of Linux Kernel<br> and any kernel options |
| `initrd` | **Initial RAM Disk**<br> loads drivers into RAM that let the kernel mount the main root filesystem |
<span>&nbsp;</span>

### Adding a Kernel to GRUB
1. load grub.conf in a text editor
2. copy a working configuration for a Linux kernel
3. title → change to a new name
4. kernel → point to new kernel
   
Reboot and you should see your new kernel in the menu
<span>&nbsp;</span>

### Installing GRUB
you must specify the boot sector device
`grub-install /dev/sda`
or `grub-install '(hd0)'`
<span>&nbsp;</span>

### Using GRUB
The first screen of the boot loader shows you a list of operating systems
To edit an entry:
1. select is and press `E` → brings up a new menu
2. highlight the `kernel` line and press `E` to edit kernel options
3. add any options
4. press `enter` to complete edit
