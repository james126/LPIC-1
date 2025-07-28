# Managing Runlevel Services

> #### chkconfig
> manage SysV init service configuration
> `chkconfig options`
> options
> |||
> |-|-|
> | `--list` | list all services as on/off and runlevels |
> | `--list [service-name]`<br> *chkconfig --list http* | show services as on/off and runlevel |
> | `[service-name] on`<br> *chkconfig http on*| enable service to start with default runlevel |
> | `--level level [service-name] on`<br> *chkconfig --level 23 nfs-common on* | enable with runlevels | 
> |`--add [service-name]`<br> *chkconfig --add http* | add service |
> 
> 
> 
> 