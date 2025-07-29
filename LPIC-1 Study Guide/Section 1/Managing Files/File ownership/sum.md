# Checking
File permission tiers:
<ol>
<li>owner</li>
<li>group</li>
<li>other users</li>
</ol>

> `ls -l`
> <img src="../../../Image/filepermissions.png" style="opacity:0.65;width:80%">
> **owner** james -rw
> **group** james
<hr>

# Changing
only root user can change a files owner and groups
ordinary users can change files they own

> #### chown
> change owner
> `chown [options] [new-owner][:new-group] filenames`
> example
> `chown sally:skyhook document.txt`
> changes user to *sally*
> changes group to *skyhook*
> | | |
> |-|-|
> | `R` `--recursive` | change ownership on entire directory tree |

> #### chgrp
> change group
> `chgrp [options] newgroup filenames`
