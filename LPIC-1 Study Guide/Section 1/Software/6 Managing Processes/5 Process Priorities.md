### Process Priorities
```nice``` launch a program with a specified priority <br>
```renice``` alter the priority of a running program <br>

<br>

> ```nice [argument] [command]``` <br>
> You can assign a priority in 3 ways:
> * ```nice -12 number-crunch data.txt```
> * ```nice -n 12 number-crunch data.txt```
> * ```nice --adjustment=12 number-crunch data.txt``` <br><br>
> 
> * All of these commands run *number-crunch* program at priority 12 and pass it to the *data.txt* file <br>
> * The range of possible values is -20 to 19 <br>
> * Negative values have the highest priority
> * The default value is 0

> ```renice priority [[-p] pids] [[-g] pgrps] [[-u] users]``` <br>
> You must specify:
> * ```priority``` 
> * ```pids``` 1+ PIDs <br>
> * ```pgrps``` 1+ group IDs <br>
> * or 1+ ```users``` usernames

Example <br>
```renice 7 16580 -u pdavison tbaker``` <br>
Set priority to 7 for PID 16580 for all processes owned by pdavison tbaker <br>
