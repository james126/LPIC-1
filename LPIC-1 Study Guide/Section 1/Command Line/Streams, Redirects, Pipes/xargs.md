# xargs

> ### xargs
> Builds a command from standars input
> `xargs [options] [command] [initial-arguments]`
> **command:** the command you want to execute
> **initial-arguments:** command arguments
> **options:** xargs options, not passed to command

- The command is run for every word passed to it from input
- Uses spaces and newlines as delimiters by default, which can cause issues

> *Example*
> delete files that belong to a user  
> `find / -user Christine | xargs –d "\n" rm`
> 
> <li> <mark>find / -user Christine</mark> finds all files in directory tree (/) and subdirectories belonging to Christine</li>
> <li> <mark>-d "\n"</mark> use newlines as delimeters</li>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-d is delimeter option
   
> ### backtick \`

>  <li>Text with backticks are treated as a separate command</li>
>  <li>The output of the backtick command is passed to the command that before it</li>
> <li>All the output is passed at once, not word at a time like <mark>xargs</mark></li>
![](../../../Image/backtick.png)

You can replace backticks with $() - so you don't confuse single quotes and backticks
![](../../../Image/backtick2.png)
