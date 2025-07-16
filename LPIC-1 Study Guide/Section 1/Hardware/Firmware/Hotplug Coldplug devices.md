# Hotplug and Coldplug Devices

_Hotplug_: can be attached/detached when **computer on** (hot)
_Coldplug_: only attached/detached when **computer off** (cold)
<br>

### Coldplug
CPU, memory, PCI cards, SSDs
<br>

### Hotplug
Rely on software to detect changes to the system as they're attached/detached
<br>

#### Hotplug utilities
utilities to manage hotplug devices
enable programas to learn about hardware
receive notifications when hardware configuration changes
<br>

<ol>
<li><b>sysfs</b></li>
<ul>
<li>a virtual filesystem</li>
<li>mounted at <i>/sys</i></li>
<li>exports info about devices so user-space utilities can access the information</li>
</ul>

|                      |                                                       |
| -------------------- | ----------------------------------------------------- |
| **user space program** | runs as an ordinary program<br>run by user or as root |
| **kernel space code**  | runs as part of the kernel<br>can communicate with hardware <br>helps hotplug devices access hardware |

<li><b>HAL Daemon</b></li>

**H**ardware **A**bstraction **L**ayer **D**aemon
<ul>
<li>a user-space program that runs all the time</li>
<li>provides other user-space programs with hardware info</li>
</ul>
<br>


<li><b>D-Bus</b></li>

**D**esktop **Bus** daemon (always running in the background)
<ul>
<li>lets process communicate</li>
<li>lets process register to be notified of events by other processes or hardware</li>
e.g. new USB device plugged in
</ul>
<br>

<li><b>udev</b></li>
<ul>
<li>virtual filesystem mounted at `/dev`</li>
<li>creates device files as drivers are loaded/unloaded</li>
</ul>
</ol>




