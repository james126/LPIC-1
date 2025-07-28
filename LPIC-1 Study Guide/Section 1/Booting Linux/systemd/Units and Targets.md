# Units and Targets

### unit and targets
**units**
* what you operate on and manage
  * defines a service
  * consists of name, type, configuration file
    *e.g.*
    * automount
    * device
    * mount
    * path
    * service
    * snapshot
    * socket
    * target
<span>&nbsp;</span>

**targets**
group units together

> #### systemctl
> system control
> `systemctl [options] command [unit]`
> example
> <img src="../../../Image/systemctl.png" style="border:1px solid lightgrey"/>
> e.g. network.target groups all the units needed to start the network interfaces for the system
> <span/>&nbsp;</span>
> * instead of changing runlevels to alter what's running, you change **targets**
> * called **runlevel0.target** - **runlevel6.target**