# Mounting
Filesystems are usually us by being <mark>mounted</mark> - associated with a directory
This can be done **temporarily** or **persistently** across reboots
<hr>

# Temporary Mounting
**mount** - mount filesystem
**umount** - unmount

> ### mount 
> `mount [-o options] [-t type] [device] [mountpoint]`
> **type**: filesystem type e.g. *ext4*
> **device**: device you want to mount e.g. */dev/sdb1*
> **mountpoint**: directory to attach the device e.g. */mnt/something* is common
> options
> | | |
> |-|-|
> | `-r` | mount as read-only |
> | `-w` | mount as read and write (default)
> | `-L` | mount with a custom label
>
> example
> `mount /dev/sdb1 /mnt/shared`
> autodetects the filesystem type

> ### umount
> `umount [options] [-t type] [device | mountpoint]`

Ensures any cached info is written to the device before it's removed
Using a GUIs unmount or eject options is equivalent to using *umount*
<hr>

# Permanent Mounting
<mark>/etc/fstab</mark> contains static file system information
<br>

1. Identify the devide UUID (Universally Unique Identifier)
   `sudo blkid`
2. Create mount point
   `mkdir /mnt/mydata`
3. Add device to `/etc/fstab`
    ![](../../../Image/mounting.png)
    **options**: defaults is a shorthand that includes rw, exec, auto etc
    **dump**: used by dump backup utility (0 means disabled)
    **pass**: Determines the order of filesystems to check at boot time
    &nbsp;&nbsp;&nbsp;&nbsp;0 - no check
    &nbsp;&nbsp;&nbsp;&nbsp;1 - root filesystem
    &nbsp;&nbsp;&nbsp;&nbsp;2 - other filesystem
4. `sudo reboot`
<span>
*backup /etc/fstab before editing in case of error*
*after editing /etc/fstab check for errors sudo mount -a*