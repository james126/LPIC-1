# Default Permissions
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
> ![](../../../Image/umask.png)
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
> example `newgrp skygroup`