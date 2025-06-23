### IRQ
* **Interrupt Request** rr **interrupt**<br>
* is a signal sent to the CPU to suspend its current activity and handle an external event <br>
* e.g. keyboard input <br>
* IRQs are numbered 0 - 15
<br>

Common IRQs <br>
![](../../Image/irqs.jpg) <br>


Modern computers often use a higher IRQ for sound cards <br>
You can see what IRQs are being used by examining `/proc/interrupts` <br>
![](../../Image/irqs.png) <br>

#### proc
* The `/proc` filesystem is a virtual  filesystem <br>
* It doesn't refer to files on a hard disk, but to kernel data <br>
* The files in /prof contain info about hardware, running processes etc

