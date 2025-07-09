# Transforming files
These commands don't change files contents, but instead send the changed file contents to STDOUT

> ### expand
> converting tabs to spaces

> ### unexpand
> convert spaces to tabs
   

> ### sort
> sort a file
> ![](../../../Image/sort.png)
>
> options
> |               | |
> |---------------|-| 
> | Ignore case   | `-f` `--ignore-case` don't differentiate uppercase/lowercase |
> | Month         | `-M` `--month-sort` sort by three letter month abbreviation e.g. JAN |
> | Numeric       | `-n` `--numeric-sort` sort by number |
> | Reverse       | `-r` `--reverse-order` sorts in reverse order |
> | Field         | `-k` `--k=field` by default uses the first field as its sort field, you can specify another field/s |
> 
> ![](../../../Image/sort2.png)


> ### split
> split a file into multiple files
> options
> |         |                                    |
> |---------|------------------------------------|
> | Split by bytes | `-b size` `--bytes=size` breaks input file into pieces by maximum *size* bytes |
> | by bytes in line-size chunks | `-C=size` `--line-bytes=size` same as split by bytes, but without breaking lines  |
> | by number of lines | `-l lines` `--lines=lines` |
> 
> example - split listing1 into two files – *numbersaa* and *numbersab*
> ![](../../../Image/split.png)
   
> ### tr
> translate (replace)
> <li>replace characters in a SET1 with characters in SET2</li>
> <li>each character in SET1 is replaced by the one at the equivalent position in SET2</li>
> <br>
> 
> `tr [options] set1 [set2]` translate characters from SET1 to SET2 
> <br>
>
> options
> |                        | |
> |------------------------|-|
> | `-t` `--truncate-set1` | truncate SET1 to size of SET2 |
> | `-d`                   | delete characters from SET1, no need for a SET2  |
> 
> example: B→b, C→c, G→c
> *note that set2 was smaller than set 1, it substitutes the last letter from set2 for the missing letter*
> ![](../../../Image/translate.png)
> <br>
> 
> **shortcuts**
> |                   | |
> |-------------------|-|
> | `:alnum`          | truncate SET1 to size of SET2 |
> | `:upper` `:lower` | delete characters from SET1, no need for a SET2 |
> | `:digits`         | delete characters from SET1, no need for a SET2 |
>
> examples
> `echo "hello world 123" | tr '[:lower:]' '[:upper:]'` converts all lowercase to upper
> `echo "password" | tr '[:alnum:]' '*'` replace all characters with *
> `echo "hello, world! 123" | tr -d [:punc:][:space:]` delete punctuation and whitespace

> ### uniq
> delete duplicate lines 
> e.g. if you've sorted a file and don't want duplicates e.g. Shakespears vacabularly
> ![](../../../Image/uniq.png)
    
> ### od
> octal dump
> <li>For displaying files that are not easily displaYed in ASCII</li>
> <li>e.g. audio files etc will look like gibberish</li>
> <li>displays a file in octal (base 8) numbers by default</li>
> 
>![](../../../Image/od.png)
