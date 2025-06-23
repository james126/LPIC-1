- Linux handles all objects as files
- This includes a programs input and output stream
- To identify a file object, Linux uses file descriptors
 
> ### Standard Input
> Keyboard input  
> Abbreviation: STDIN  
> File descriptor: 0
 
> ### Standard Output
> Normally displayed on the screen  
> STDOUT  
> 1
 
> ### Standard Error
> Normally sent to same output device as standard output  
> STDERR  
>2
 
Internally, programs treat STDIN, STDOUT and STDERROR like data files  
They open, read, write and close them when they're done.
