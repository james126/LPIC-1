# Changing

only root user can change a files owner and groups
ordinary users can change files they own

> #### chown
> change owner
> `chown [options] [newowner][:newgroup] filenames`
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
