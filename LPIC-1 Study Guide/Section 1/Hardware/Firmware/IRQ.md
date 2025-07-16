# IRQ
* **I**nterrupt **R**e**Q**uest
* <mark>signal sent to the CPU to handle an event</mark>
e.g. keyboard input
<br>

IRQs are numbered 0 to 15, some modern computers have more
<ul>
<li>some are reserved for specific purposes e.g. keyboard</li>
<li>some are shared with common uses</li>
<li>some are left for extra devices that may be added to the system</li>
</ul>
<br>

#### Common IRQ
|    |          |
| -- | -------- |
| **1**  | Keyboard |
| **12** | Mouse    |

#### Examining IRQ
 `cat /proc/interrupts`
![](../../../Image/irqs.png)
shows: 
<ol>
<li>IRQ</li>
<li>number IRQs for a CPU</li>
<li>driver name</li>
</ol>

