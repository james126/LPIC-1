# Using SysV Initialization Process
### SysV
* stands for System V
* older system to manage boot-up services
* originally from Unix System V operating system
<span>&nbsp;</span>

### init
* initial process (PID1)
* the `init` program determines which services to start based on <mark>runlevels</mark>
* runlevels are numbered **0** to **6**
<hr>

# Runlevel Functions
Numbered 0 to 6
|runlevel||
|-|-|
| 0 | transitional level<br> used to shut down system |
| 1, s, S | single user mode<br> like safe mode in windows |
| 2 | Debian distros → multi-user mode with GUI |
| 3 | Redhat → multi-user mode with CLI |
| 4 | undefined |
| 5 | Redhat → multi-user with GUI |
| 6 | reboot system |

### Runlevel Services
Found in `/etc/inittab`
syntax: `id:runlevels:action:process`
|||
|-|-|
| id | **identification code** |
| runlevel | **application runlevels** for this entry<br> e.g. 345 means runlevels 3,4,5 |
action | **action to be taken**<br> how to treat the process<br> *wait* means start the process and wait for it to terminate |
| process | **process to run** |

example
<img src="../../../Image/inittab.png" style="width:30%;border: 1px solid lightgrey" />
<span>&nbsp;</span>

### Startup Scripts
1. the **rc** script runs scripts for each runlevel
2. symbolic links to scripts are place in runlevel-specific directories
3. **rc** passes a **start** parameter to all the scrips with names that being with **S**, and a stop parameter to all the scripts with names that begin with **K**
<hr>

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
<hr>

# Checking Runlevel
#### Checking Default Runlevel
Check the `/etc/inittab` file
example
<img src="../../../Image/checkingrunlevel.png" style="width:40%; border:1px solid lightgrey">
the default runlevel has id:2
<span>&nbsp;</span>
<span>&nbsp;</span>

#### Changing Default Runlevel
Edit the **initdefault** line in `/etc/inittab`
if the system doesn't have that file, create one with only an **initdefault** line

> #### Checking Current Runlevel
> `runlevel`
> example
> <img src="../../../Image/runlevel.png" style="width:25%; border:1px solid lightgrey">
> **N** → THE system hasn't switched runlevels since booting
>


#### Chaning Runlevels on a Running System
e.g. changing from GUI → CLI
you can use:
1. `init`
2. `shutdown`
3. `halt`
4. `reboot`
5. `poweroff`


> #### init
> `init runlevel`
> example
> *init 1* → change the runlevel to 1

> #### telinit
> **available in SysV, Upstart, systemd**
> `telinit runlevel [options]`
> same as **init** but has an option to reload */etc/inittab*
> |||
> |-|-|
> | `q` | reload */etc/inittab* and any changes |
>
> example
> `telinit q`

> #### shutdown
> `shutdown [options] [time] [message]`
> sends a  message to all users who are logged in 
> lets you specify when to change change runlevel, so users have to to save and exit
> ||||
> |-|-|-|
> | option | `now` | shutdown now |
> | option | `-r` | reboot |
> | option | `-P` | powers off |
> | option | `-h` | halt, shutdown without powering off off|
> | option | `-c` | cancel a pending shutdown |
> | time | `hh:mm` | 24 hour clock format|
>
> example
> `shutdown -h +15 "system going down for maintenance"`

> #### halt, reboot, poweroff
> **available in SysV, Upstart, systemd**
> `halt` shutdown without powering off
> `reboot`
> `shutdown`