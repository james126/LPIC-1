- Redirects the first programs STDOUT to second programs STDIN
- first | second
- First | second | third | fourth …
 
> ### tee
> Splits STDIN to multiple STDOUT <br>
> ![](../../Image/Exported%20image%2020250304130143-0.png) <br>
> $PATH goes to STDOUT and also saved in path.txt

<br>

> ### xargs [options] [command [initial-arguments]]
> 
> When you run xargs, it runs command once for every word passed to it on STDIN <br>
> If you want to pass multiple options to command, enclose the group in quotation marks.
>
> |   |   |
> |---|---|
> | **options**  | xargs options, they aren't passed to command  |
> |**command**   | what you want to execute   |
> |**initial-arguments**   | arguments to pass to the command  |
>
> **Example** <br>
> Delete files that belong to a user  
> ```find / -user Christine | xargs –d "\n" rm```  
> **find / -user Christine**: finds all files in directory tree (/) and subdirectories belonging to Christine  
> The list is piped to ```xargs```, which adds each input value to its own rm command  
> * Problems can happen if filenames contain spaces  
> * By default xargs uses spaces and newlines as delimeters  
> * ```-d "\n"```: use only newlines as delimeters
   
<br>

> ### backtick \`
> Not the same as single quote <br>
> Text with backticks are treated as a separate command <br>
> The output of the backtick command is passed to the command that preceds it <br>
> e.g. ```rm `find ./ -user Christine` ```
