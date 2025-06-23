> ```grep [options] regex [files]``` <br>
> Global Regular Expression Print <br>
> 
> |                              |                                                                                                                 |
> |------------------------------|-----------------------------------------------------------------------------------------------------------------|
> | Count matching lines         | ```-c``` <br> ```--count``` <br> display the number of lines that match the pattern                             |
> | Specify a pattern input file | ```-f file``` <br> ```--file=file```                                                                            |
> | Ignore case                  | ```-i``` <br> ```--ignore-case``` <br> Non case sensitive                                                       |
> | Search recursively           | ```-r``` <br> ```--recursive``` <br> searches in directory and subdirectories                                   |
> | Used fixed strings pattern   | ```-F``` <br> ```--fixed-strings``` <br> Characters are treated as a string and not regex e.g. \$ treated as \$ |
>
> Example <br>
> ```grep –r eth[01] /etc/*```
> * Finds all files that contain string eth0 or eth1 <br>
> * Searches recursively <br>
> * For each matching file, the line that contains the string is printed
> 
> Example <br>
> ```Grep -E "(something\.example\.com).*200" /etc/*``` <br>
> * -E extended regular expression <br>
> * Match the URL, then any number of characters before 200

<br>

> ```sed``` <br>
> Stream Editor <br>
> ```sed [options] -f _script-file_ [input-file]``` <br>
> ```sed [options] _script-text_ [input-file]``` <br>
> Modify a files contents <br>
> Modifications are temporary unless you save them <br>
>
> |                  |                                           |
> |------------------|-------------------------------------------|
> | ```a\text```     | append text to file                       |
> | ```i\text```     | insert text into file                     |
> | ```R filename``` | append text from filename into file       |
> | ```c\text```     | replace selected lines with provided text |
> | ```Q```          | immediately quit the script               |
>
> Example <br>
> ```sed 's/2012/2013/' calender1.txt > calendar2.txt``` <br>
> * Replace the first occurance of 2012 on each line with 2013 <br>
> * Send the output in calendar2.txt
