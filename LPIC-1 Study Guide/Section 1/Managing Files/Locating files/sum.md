# Filesystem Hierarchy Standard (FHS)
Standardizes linux directories and programs
www.pathname.com/fhs/
<span>&nbsp;</span>

### Terms
**shareable files** 
can be shared between computers
e.g. user data files, program binary files
<span>&nbsp;</span>

**un-shareable files** 
contain system-specific information
e.g. config files
<span>&nbsp;</span>

**static files** 
only changed by the system administrator
e.g. program executables
<span>&nbsp;</span>

**variable files**
home directory files
email files
<span>&nbsp;</span>

FHS tries to fit all the important directories into a 2x2 matrix
<img src="../../../Image/fhs.png" style="width:50%">
<hr>

# Important Directories and Contents
www.pathname.com/fhs/
| | |
|-|-|
| `/` | root directory<br>all directories branch off it |
| `/boot` | boot files |
| `/home` | user data |
| `/opt` | add-on application packages<br> for large third-party software that doesn't follow FHS conventions |
| `/tmp` | temporary files |
| `/usr` | contains programs<br> divided into subdirectories | 
| | `/usr/local` software installed locally |
| `/var` | variable data<br> logs, mail files etc |
| `/bin` | user command binaries<br> *cat, cp, kill, ls, mkdir, ps, rm* |
| `/dev` | device files <br>hardware devices are treated as files | 
| `/etc` | configuration files |
| `/lib` | libraries<br> files shared across many programs<br> |
| | `/lib/modules` contains kernel modules (drivers) |
| `/sbin` | system admin binaries<br> *fdisk, mkswap* |
<hr>

# Locating Files
> #### find
> `find [path] [expression]`
> **expression**
> | | ||
> |-|-|-|
> | by name| `-n pattern` | `find . -name "*.txt"` |
> | by file size | `-size [+\|-]n` | by default n is 512-byte blocks<br> can modify by trailing the value with a letter code e.g. M for megabytes<br> `find . -size +10M`  | 
> | by User Id | `-uid UID` | 
> | by username | `-user name` |
> | restrict search depth | `-maxdepth levels` | limit recursive directories to search |

> #### locate
> search from a database updated daily
> search may not return recently created files
> update it manually using `updatedb` which is configured at */etc/updatedb.conf*
> `locate search-string`