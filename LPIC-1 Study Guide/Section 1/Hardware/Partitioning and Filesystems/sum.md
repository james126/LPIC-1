# Partitioning a disk

#### Partition table format
<img src="../../../Image/gpt.png" width="50%" style="opacity:0.7">

> ### fdisk
> fixed disk
> <mark>for MBR partition table format</mark> (Master Boot Record)
> `fdisk [disk]` **disk** that you want to partition
> e.g. `fdisk /dev/hda`
> <br>
>
> | | |
> |-|-|
> | `n` | create a partition
> | `d` | delete a partition
> | `l` | list partitions
>
> example *sudo fdisk -l*
> <img src="../../../Image/fdisk.png" width="75%" style="opacity:0.65">

> #### gdisk
> <mark>for GPT table format</mark>
> **G**UID **P**artition **T**able (Globally Unique Identifier)
> <br>
>
> | | |
> |-|-|
> | `n` | create a partition
> | `d` | delete a partition
> | `l` | list partitions

> #### parted
> not in exam
> <mark>for all table formats</mark>
> <li>CLI or GUI</li>
> <li><mark>resize partitions easily (provided their not being used)</mark></li>
<hr>

# Formatting a partition
Often called "making a filesystem"
<li>Involves writing low-level data structures to disk</li>
<li>Linux can use these data structures to store and read files</li>
<br>

**low-level formatting**
creates a structure on the disk
only low-level formatted when they are made
<br>

**high-level formatting**
creates a filesystem
<br>

### Common Filesystem Types
| | |
|-|-|
| ext2 | **Second Extended File System**<br> traditional Linux-native filesystem<br> |
| ext4 | **Fourth Extended File System**<br> works with  large disks<br> improved performance |
| reiserFS | **journaling filesystem**<br> traditional filesystems can crash while creating/modifying files and creates inconsistencies<br> journaling keeps track of operations and has rollback options |
| FAT | **File Allocation Table**<br> old filesystem<br> supported by Microsoft DOS<br> good for exchanging data between drives<br> |
| NTFS | **New Technology File System**<br> Windows filesystem<br> Linux can read/modify but not write new files<br> |
| ISO-9660 | Filesystem for CD-ROMS |

<br>

### Creating a Filesystem
> #### mkfs
> example  `mkfs -t ext3 /dev/sda6`
> creates an ext3 filesystem on /dev/sda6
> <br>
> to learn about filesystem options
> `man mkfs.[filesystem]`
> e.g. *man mkfs.ext2*# Swap space
<hr>

# Swap space
an extension of memory
Linux can use a *swap file* which is a file that works the same way
<img src="../../../Image/swapfile.png" style="opacity:0.65">