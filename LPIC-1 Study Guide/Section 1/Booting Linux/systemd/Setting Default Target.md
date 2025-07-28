# Setting Default Target

The default target when Linux boots is `/etc/systemd/system/default.target`
it's normally a link to a file in */lib/systemd/system*

> #### systemctl
> system control
> control services and targets
> `systemctl [options] command [unit]`
> |commands||
> |-|-|
> | `list-units` ||
> | `start name`||
> | `stop name` ||
> | `reload name` | reload unit configuration file |
> | `restart name` | shut down and restart |
> | `status name` ||
> | `enable name` ||
> | `disable name`||
>
> example
> <img src="../../../Image/systemctlstatus.png" style="border:1px solid lightgrey">
