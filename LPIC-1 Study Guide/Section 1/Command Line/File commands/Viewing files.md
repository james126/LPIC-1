# Viewing files


> ### head
> <li>view the start of a file</li>
> <li>first 10 lines by default</li>
> 
> options:
> |                             | |
> |-----------------------------|-|
> | `-c num` <br> `--bytes=num` | view first **num** bytes |
> | `-n num` <br> `--lines=num` | view first **num** lines |

> ### tail
> <li>view the end of a file</li>
> <li>has options same as head and some extra ones:</li>
> 
> |                             | |
> |-----------------------------|-|
> | `-f` <br> `--follow` | keep the file open and display new lines as they're added <br> good for tracking log files |
>
> example
> combining head with tail  
> extract the first 15 lines, then display its last 5 lines
> `head --n 15 sample.txt | tail --n 5`
