# Permissions
permissions don't apply to root
however root still needs execute bit to run a program
but can change permissions on any file
<span>&nbsp;</span>

#### Permission strings
10 characters long
<img src="../../../Image/permissions.png" width=75% style="border:1px solid lightgrey">
**File type**
`-` regular file
`d` directory
`l` symbolic link 
<span>&nbsp;</span>

**execute** - file may be run as a program
<span>&nbsp;</span>

#### Permission bits
<ol>
<li>individual permissions e.g. execute access for file owner, are often referred to as permission bits</li>
<li>linux encodes this information in binary</li>
<li>permission information can be expressed as a 9-bit number</li>
<li>the number is expressed in octal (base 8)</li>
<li>the base-8 representation of a permission string is three characters long; one for owner, group and world</li>
</ol>

<span>&nbsp;</span>
<b>octal permissions:</b>
1 execute
2 write
4 read
<span>&nbsp;</span>

example
`-rwxrw-r--`
`111110100`
1. group bits
`111 110 100`
2. convert to octal
`111` 2^0 2^1 + 2^2 = 7
`110` 2^1 + 2^2 = 6
`100` 2^2 = 4
3. combine octal digits
764

> #### Common permissions
> | string | octal |
> |-|-|
> | rwxrwxrwx | 777 |
> | rwx------ | 700 |
> | rwxr-xr-x | 755 |
<hr>

# Special Permissions
#### Set User ID (SUID)
run the program with the permissions of whoever owns the file
e.g. if a file is owned by root, the program runs with root privileges
<span>&nbsp;<span>

SUID is shown by a <mark>s</mark> in the owners execute bit
if set on a file without user execute permissions, shown by <mark>S</mark>
e.g. `rwSr-xr-x`
<span>&nbsp;<span>

#### Set Group ID (SGID)
sets the group permissions
same rules as SUID
e.g. `rwxr-s-x`
<span>&nbsp;<span>

#### Sticky Bit
set on a directory
shown as <mark>t</mark>
directories files can only be deleted by:
<li>their owners</li>
<li>directories owner</li>
<li>root</li>

e.g. `rwxr-xr-t`
<hr>

# Access Control List (ACL)
#### Discretionary Access Control (DAC)
uses permissions string
<span>&nbsp;</span>

#### Access Control List (ACL)
set per file
list of users/groups and the permissions they are given
set - `setfacl`
view - `getfacl`
<hr>

# Changing Mode
modify file permissions
> #### chmod
> change mode
> `chmod [options] [mode] filename`
> | | |
> |-|-|
> | `-R` `--recursive` | changes all files in directory tree |
>
> example
> `chmod 644 file.dat`

#### Setting Special Permissions
add a number before the three octal digits
setting the first digit as 0 removes all special permissions
<span>&nbsp;</span>

**bit permissions:**
1 sticky bit permission
2 SGID permission
4 SUID permission
<span>&nbsp;</span>

example
`chmod 6750 program.sh`
SGID = 2
SUID = 4
2+4=6
<span>&nbsp;</span>

#### Symbolic Mode
codes for permissions
<img src="../../../Image/symbolicmode.png" style="border:1px solid lightgrey">
example
`chmod a+x bigprogram`
`chmod g=u bigprogram`# Default Permissions
When creating a file, it has default permissions
&nbsp;&nbsp;&nbsp;&nbsp;**owner** is whoever created the file
&nbsp;&nbsp;&nbsp;&nbsp;**group** is the users primary group
<span>&nbsp;</span>

default permissions are configurable

> #### umask
> user mask
> takes an octal value that represents bits to be removed from either:
> &nbsp;&nbsp;&nbsp;&nbsp;777 directories (default)
> &nbsp;&nbsp;&nbsp;&nbsp;666 files (default)
> <span>&nbsp;</span>
> 
> **examples**
> | unmask | created files | created directories |
> |-|-|-|
> | 000 | 666 (rw-rw-rw-) | 777 (rwxrwxrwx) |
> | 022 | 644 (rw-r--r--) | 755 (rwxr-xr-x) |
> | 077 | 600 (rw-------) | 700 (rwx------) |
> 
> **default unmask**
> <img src="../../../Image/umask.png" style="opacity:0.65">
> the first digit is the octal code for SUID, SGID and the sticky bit
> <span>&nbsp;</span>
>
> **To change unmask**
> 1. `unmask 0022`
> changes to 0022
> 2. `umask u=rwx,g-rx,o=rx`
> equivalent to method 1


### Default Group
users can change their default group

> #### newgrp
> new group
> the user using this command must be a member of that group
> example `newgrp skygroup`# File Attributes
you can change attributes for most file systems using `chattr`

> #### chattr
> `chatter +/-[option] file`
> options
> | | |
> |-|-|
> | `A` | no access time updates<br/> don't updated access timestamp when accessing a file |
> | `i` | immutable<br/> don't updated access timestamp when accessing a file |
>
> example
> `chattr +i important.txt`