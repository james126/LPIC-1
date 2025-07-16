### Configuring PCI Cards
Peripheral Component Interconnect
used for connecting internal components

![](../../../Image/pcislots.png)
* the PCI bus is the standard expansion bus for internal devices 
* plug-and-Play style configuration. 
<br>

#### Configuration
most PCI devices configure themselves automatically. 
however you can tweak how PCI devices are detected: <br>
* The kernel has options that affect how it detects PCI devices. These are in the kernel config screens under Bus Options.
* Most firmware has PCI options that change the way PCI resources are allocated.
<br>

> #### setpci
>  query and adjust PCI devices configurations

> #### lspci
> * info about the PCI busses on your system
> * items connected to those busses
>  
> | options       |       |
> |---------------|-------|
> | -v, -vv, -vvv | verbose, (-vv and -vvv increase verbosity) |
> 
> ![](../../.../Image/../../../Image/lspci.png)
