# Process priorities

`nice` launch a program with a specified priority
`renice` change a running process priority


> `nice [argument] [command]` 
> You can assign a priority in 3 ways:
> * `nice -12 number-crunch data.txt` *(assigns 12 not -12)*
> * `nice -n 12 number-crunch data.txt`
> * `nice --adjustment=12 number-crunch data.txt`
> run *number-crunch* at priority 12 and pass in *data.txt*
> <br>
> * 0 default
> * -20 (highest)
> * 19 (lowest)


> `renice priority [-p [pids]] [-g [pgrps]] [-u [users]]`
> specify:
> * **priority**
> * **pids** 1+ PIDs
> * or **pgrps** 1+ group IDs
> * or 1+ **users** usernames

example
`renice 7 16580 -u pdavison tbaker`
**7** set *priority*
**16580** to process with *PID* 
**pdavison** **tbaker** amd all processes owned by *users*
