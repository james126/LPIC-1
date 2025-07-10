# Examining Processes

> #### ps [options]
> process status
>
>
> *three different types of options:*
> |                 |                                  |
> | --------------- | -------------------------------- |
> | `-` single dash | can be grouped together e.g. -Ax |
> | `()` no dash    | can be grouped together          |
> | `--` two dash   | **can't** be grouped together    |
>
> options
> |                 |                                  |
> | --------------- | -------------------------------- |
> | `-A` `-e`       | all processes on the system      |
> | `x`             | all processes owned by the user  |
> | `--h`           | help                             |
> | `v `            | extra information        |

 **Output Column Names** 
![](../../../Image/ps.png)
 * **PID** &nbsp; Process ID 
 * **PPID** &nbsp; Parent Process ID 
 * **TTY** &nbsp; TeleTYpe code to identify a terminal 
 * **TIME**, **%CPU** &nbsp; CPU time consumed/percentage when executed 
 * **CPU Priority** &nbsp; Default value 0 - positive values *reduce* priority, negative *increase* 
 * **Command** &nbsp; launch process
 * **RSS**, **%MEM** memory - Resident Set Size (program + data)
<br>

example
<mark>view a particular process</mark>
`ps -A | grep bash`
<br>

example
view parent/child processes
`ps -A --forest`
![](../../../Image/psforest.png)