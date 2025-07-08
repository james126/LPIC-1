### Killing Processes
> ```kill -s signal pid``` <br>
> Will kill only those processes owned by the user who runs kill
> 
> *signal* <br>
> Kill has lots of signals, each with a specific name which performs a different type of kill <br>
> You can specify a signature with its number (eg 9) or name (SIGKILL) <br>
> To get all signals ```kill -l``` <br>
> ![](../../Image/kill.png) <br>
> * ```1)SIGHUP``` terminates interactive programs and causes many daemons to reread their config files <br>
> &nbsp;&nbsp;&nbsp;&nbsp;Daemon is a process that runs in the background and is not interactive
> * ```9)SIGKILL``` exit process without performing routine shutdown tasks <br>
> * ```15)SIGTERM``` causes process to exit but allows it to close open files <br>
>
> ```15)SIGTERM``` is default
> 
