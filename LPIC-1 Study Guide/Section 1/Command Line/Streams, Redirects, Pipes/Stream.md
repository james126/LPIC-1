# Stream
Linux handles all objects as files
this includes a programs input/output stream
to identify a file, linux uses <mark>file descriptors:</mark>


 
> ### Standard Input
> Programs accept keyboard input via *standard input*  
> in most cases, this data comes from the keyboard
> **abbreviation:** STDIN  
> **file descriptor:** 0
 
> ### Standard Output
> Data sent to users via *standard output*
> usually displayed on a screen
> **abbreviation:** STDOUT  
> **file descriptor:** 1
 
> ### Standard Error
> An output stream
> carries error messages
> **abbreviation:** STDERR  
> **file descriptor:** 2
 
**programs treat STDIN, STDOUT and STDERR like files  
They open/read/write/close them when**
