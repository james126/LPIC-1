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
| FAT | **File Allocation Table**<br> old filesystem<br> suppored by Microsoft DOS<br> good for exchanging data between drives<br> |
| NTFS | **New Technology File System**<br> Windows filesystem<br> Linux can read/modify but not write new files<br> |
| ISO-9660 | Filesystem for CD-ROMS |

### Creating a Filesystem
> #### mkfs
> example  `mkfs -t ext3 /dev/sda6`
> creates an ext3 filesystem on /dev/sda6
> <br>
> to learn about filesystem options
> `man mkfs.[filesystem]`
> e.g. *man mkfs.ext2*