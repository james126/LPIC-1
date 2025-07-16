# Kernel Modules
<li><mark>provide access to hardware</mark></li>
<li><b>a driver is a type of module but not all modules are drivers</b></li>
<li>the stand-alone files are stored in <i>lib/modules</i></li>
<br>
Linux loads the modules when it boots, but you can load additional modules.

> #### lsmod
> shows all the modules that are loaded
> ![](../../../Image/lsmod.png)
> **Used by** - number of dependencies (other modules) 
> if it's being used by another module, the module name is shown next to the number 
