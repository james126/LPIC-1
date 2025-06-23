### Coldplug and Hotplug Devices
_Hotplug_: can be physically attached/detached when computer is turned **on** <br>
_Coldplug_: can only attached/detached when computer is turned **off** <br>
<br>
#### Hotplug
Rely on software to detect changes to the system as they're attached/detached <br>
There are several utilities to manage hotplug devices: <br>
* *Sysfs* <br>
A virtual filesystem, mounted at `/sys` that exports info about devices so user-space utilities can access <br> the information.

|                      |                                                                                                                                                                   |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *user space* program | runs as an ordinary program, whether runs by a ordinary user or as root                                                                                           |
| *kernel space* code  | runs as part of the kernel <br> typically, only the kernel (kernel-space code) can communicate with hardware <br> these tools help hotplug devices access hardware |

* *HAL Daemon* <br>
Hardware Abstraction Layer (HAL) Daemon <br>
Provides other user-space programs with info on available harware <br>
<br>

* *D-Bus* <br>
Lets processes to be notified of events from hardware <br>
<br>

* *udev* <br>
A virtual filesystem, mounted at `/dev`, that creates device files as drivers are loaded/unloaded 


