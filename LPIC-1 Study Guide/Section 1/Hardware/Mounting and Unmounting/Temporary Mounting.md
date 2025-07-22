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
