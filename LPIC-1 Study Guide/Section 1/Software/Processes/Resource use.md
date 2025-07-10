## Resource usage

> ### top
> examining process <mark>CPU usage</mark>
> updates every few seconds
> | option    |                               |
> |-----------|-------------------------------| 
> |`-d delay` | specify delay between updates |
> | `-p pid`  | to monitor a specific process |
> 
> ![](../../../Image/top.png)
> **load average (top line):** shows *current load average : two previous measures*
> &nbsp;&nbsp;&nbsp;&nbsp;0 = no programs demanding cpu
> &nbsp;&nbsp;&nbsp;&nbsp;1 = one program running CPU-intensive tasks
> &nbsp;&nbsp;&nbsp;&nbsp;higher averages = multiple programs competing for CPU time
> <br>
> when it's running you can use these commands:
> `k` kill a process - will ask for PID
> `q` quit

> ### free
> for examining Memory usage