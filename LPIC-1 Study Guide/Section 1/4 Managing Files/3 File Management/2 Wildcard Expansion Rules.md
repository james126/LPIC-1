### Wildcard Expansion Rules
You can use *wildcards* with many commands <br>
It's a symbol that stands for other characters <br>

> Question mark (?) <br>
> stands for single character <br>
> `b??k` matches book, buck etc

> Asterisk (*) <br>
> matches any characters, including no character <br>
> `b*k`matches bk, backtrack, book

> Brackets ([]) <br>
> match any character is the set <br>
> `b[ae]ok` matches baok <br>
> each bracket group is used for single character matches <br>
> `b[ae]o[kds]` matches baok
> 
> Range of values ([-]) <br>
> `b[a-z]ck` matches back etc 

<br>

#### Example
>wildcards can be used in commands
> ![](../Image/wildcard.png)

> **Combining options** <br>
> You can combine options e.g. `ls -lF`
