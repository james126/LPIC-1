### PATH
When you type a command that's not recognised as an internal command, it checks the path to find a program by that name to execute it.
The *path* is a list of directories in which commands can be found
Defined by `$PATH` environment variable
<br>

### Running programs
You can run programs that aren't on the path by using the path name
`./someprog` runs someprog in the current directory
`home/user/someprog` runs it in the *home/user* directory
<br>

To run a program it must be marked as executable
Standard programs are marked as executable