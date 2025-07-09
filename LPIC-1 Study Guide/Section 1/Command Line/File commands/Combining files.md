# Combining Files


> ### cat
> concatenate
> **display:**
> ```
> cat first.txt
> Data from first file
> ```
> **to file:**
> `cat first.txt second.txt > combined.txt`
> <br>
> 
> options
>
> |                            | |
> |----------------------------|------------------------------------------------------------|
> | Display line ends          | `-E` `--show-ends` <br>add **$** (dollar sign) at the end of each line |
> | Number lines               | `-n` `–number` <br>add line number to start each line |
> | Minimize blank lines       | `-s` `--squeeze-blank` <br>Compresses groups of blank lines to a single line |


> ### tac
> Same as cat but it reverses the order of lines in the output
> ![](../../../Image/tac.png)


> ### join
> Like a <mark>database join</mark>
> By default, uses the first field as they key to match across files
> ![](../../../Image/join.png)
> Can use another field as the key 
> ```join –1 3 –2 2 cameras.txt lenses.txt```
> join using **3rd** field in cameras and **2nd** field in lenses

> ### paste
> Merge files line by line, separating each line with a tab
> ![](../../../Image/paste.png) |
