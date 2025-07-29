# Terminology
#### Boot Loader
A small program that loads the operating system
<span>&nbsp;</span>

#### Boot Manager
Lets you choose what OS to boot
especially in systems with multiple operating systems
<span>&nbsp;</span>

**boot manager** decides what to boot
**boot loader** loads the operating system
<span>&nbsp;</span>

#### GRUB
* GRUB acts as a boot manager and a boot loader.
* when you see the menu, it's the boot manager
* when you make a selection, it's a boot loader and loads the selected OS
<hr>

# Boot Loader Principles
### BIOS Booting
<img src="../../../Image/bootloader.png" style="width:80%">

1. **Firmware** loads **BIOS**
2. in BIOS configure boot order for bootable devices (e.g. hard drive, then USB)
3. from bootable device BIOS loads **Master Boot Record (MBR)**
MBR contains the **Primary Boot Loader** 
<span>&nbsp;</span>

**Primary Boot Loader:**
1. loads **Boot Sector** from device
2. the Boot Sector contains a secondary boot loader which when executed loads the OS kernel
<span>&nbsp;</span>

* Windows uses (path A) - boot sector loads Windows Boot Manager
* Linux uses either (path A) or (path B)
<span>&nbsp;</span>

### EFI Booting
**EFI System Partition (ESP)**
Boot Loaders are stored as files in a disk partition known as the EFI System Partition (ESP)
ESP is mounted at `/boot/efi`
<span>&nbsp;</span>

**Boot Loaders**
stored in .efi files
e.g. `/boot/efi/EFI/ubuntu/grub.efi`
lets you store a separate boot loader for each 0S installed on the computer
<span>&nbsp;</span>

**Boot Manager**
the EFI firmware includes a Boot Manager program
it lets you select which boot loader to launch
<span>&nbsp;</span>

<img src="../../../Image/efi.png" style="width:80%"> 
<hr>

# GRUB Legacy
Boot Loader for Linux
Eclipsed by GRUB 2
<span>&nbsp;</span>

### Configuration
* configuration file `/boot/grub/menu.lst` 
* GRUBs root partition is the partition in which the configuration file exists
* normally `/boot/grub/`
<span>&nbsp;</span>

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
<hr>

# GRUB 2
Works with BIOS and EFI (Extensible Firmware Interface)
<span>&nbsp;</span>

### Configuration 
Config file `/boot/grub/grub.conf`
example
<img src=../../../Image/grub2.png style="width:70%;border:1px solid lightGrey;">
|||
|-|-|
| `menuentry` | title |
| `set root =` | sets root directory<br>partitions start from 1, not 0 |


### Editing Configuration
Don't edit `/bot/grub/grub.conf`
* instead edit `/etc/grub.d` and `/etc/default/grub`
* then use `update-grub` to makes changes to grub.conf
* when you run update-grub it outputs to standard output. To save the changes `update-grub > /boot/grub/grub.cfg`# Alternative Boot Loaders
<span>&nbsp;</span>

### The Linux Kernel
* Since version 3.3.0 it has incorporated an EFI boot loader for *x86* and *x86-64* systems
* on EFI computers, this lets the kernel serve as its own boot loader
* eliminates the need for a separate tool like GRUB
<span>&nbsp;</span>

### Damaged Boot Loader
Linux sometimes becomes un-bootable if the boot loader becomes damaged
1. Try booting from the USB you used to install the OS, and look for an option to boot a kernel from the hard dist
2. once the system is booted, you can use `grub-install` to reinstall GRUB
3. The USB may also provide a recovery option