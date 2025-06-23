### Redirect Operators
The arrow points to the target

|       |   |
|-------|---|
| **>** |**Creates a new file containing STDOUT**  <br>**If file exists, it's overwritten**|
| **>>** |**Appends STDOUT to file**  <br>**If file doesn't exist, it's created**|
| 2>    |Creates a new file containing STDERR|
| 2>>   |Appends STDERR to existing file|
| &>    |Creates a new file containing STDOUT and STDERR|
| **<** |**Contents of file to be used as STDIN**|
| <<    |Accepts text as STDIN|
| <>    |File to be used for both STDIN and STDOUT|

<br>
 

> ### Redirecting to Null
> Redirect STDOUT or STDERR to ```/dev/null``` <br>
> This file is a device that's connecting to nothing, it's used when you want to get rid of data

<br>
 
> ```<<``` <br>
> You might use this command in a script to pass data to a program <br>
> The text after << isn't a filename, instead it's a word used to mark the end of input <br>
> ```someprogram << EOF``` <br>
> causes someprogram to accept input until it sees a line that contains only thee string EOF|
 

