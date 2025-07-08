### Configuring PCI Cards

The PCI bus, which is the standard expansion bus for most internal devices was designed with
Plug-and-Play style configuration. Most PCI devices configure themselves automatically. You can 
however tweak how PCI devices are detected: <br>
* The kernel has options that affect how it detects PCI devices. These are in the kernel config 
  screens under Bus Options.
* Most firmware has PCI options that change the way PCI resources are allocated.
* Some drivers support options that can configure hardware to use particular resources. You must 
  pass these options to the kernel using a boot loader.
* The `setpci` utility and query and adjust PCI devices configurations.

> `lspci` <br>
> Displays info about the PCI busses on your system and all items connected to those busses. <br>
>  
> | options       |       |
> |---------------|-------|
> | -v, -vv, -vvv | verbose |
> 
