### Learning about Kernel Modules
Kernel drivers, many of which come in the form of _kernel modules_ handle hardware.
They are usually stored in `lib/modules` and be be loaded to provide access to hardware and 
unloaded to disable. <br>

Linux loads the modules when it boots, but you can load additional modules.

> `lsmod` <br>
> shows the kernel modules loaded
> > ![](../../Image/lsmod.png) <br>
> **Used by column** shows the number of modules or processes using that module <br>
> If it's being used by another module, the module name is shown next to the number <br>
> <br>
> 
