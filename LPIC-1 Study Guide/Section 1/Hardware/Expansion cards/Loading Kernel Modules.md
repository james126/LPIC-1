### Loading Kernel Modules

two programs to load them: `insmod` `modprobe`
Linux loads modules automatically


> #### insmod [path]
> **must <mark>manually</mark> load module dependencies**
> you can pass in module options, that are specified in a module
> example
> ![](../../../Image/insmod.png)

> #### modprobe [name]
> **<mark>automatically</mark> loads dependencies**
> ![alt text](../../../Image/modprobe.png)
>
> | options         |                                                |
> |-----------------|----------------------------------------------- |
> | `-C filepath`   | modproble configuration file is /etc/modprobe.conf or in /etc/modprobe.d/<br> you can change it by passing in  your own filepath and file |
> | `-r` `--remove` | remove module and any on which it depends that are not used elsewere |
> | `--show-depends`| show modules that the specified module depends on |

