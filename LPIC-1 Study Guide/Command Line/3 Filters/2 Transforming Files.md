> ```expand``` <br>
> Converting Tabs to Spaces <br>
> When programs processing files don't deal well with tabs <br>
> By default it takes tab as 8 characters, you can change this with <br>
> &nbsp;&nbsp;&nbsp;&nbsp; ```-t num or –tabs=num``` <br>
> &nbsp;&nbsp;&nbsp;&nbsp; (num = tab spacing value)<br><br>  
> ```unexpand``` <br>
> Convert spaces to tabs
   
<br>

> ```sort``` <br>
> ![](../../Image/Exported%20image%2020250304130158-0.png) <br>
>
> | Options    |                                                                         |
> |------------|-------------------------------------------------------------------------|
> | Ignore case | ```-f or --ignore-case``` <br> Don't differentiate uppercase/lowercase |
> | Month sort | ```-M or --month-sort``` <br> Sort by three letter month abbreviation e.g. JAN |
> | Number sort | ```-n or--numeric-sort``` |
> | Reverse order | ```-r or --reverse-order``` |
> | Field sort | ```-k field or --k=field``` |
  
<br>

> ```split``` <br>
> Split a file into multiple files <br>
>
> | Options |                                    |
> |---------|------------------------------------|
> | Split by bytes | ```-b size``` or ```--bytes=size``` |
> | Split by bytes in line-size chunks | ```-C=size``` or ```--line-bytes=size``` |
> | Split by number of lines | ```-l lines``` or ```--lines=lines``` |
> 
> Split listing1 into two files – *numbersaa* and *numbersab* <br>
> ![](../../Image/Exported%20image%2020250304130200-1.png)\||
   
<br>

> ```tr [options] SET1 [SET2]``` <br>
> Translate characters from SET1 to SET2 <br>
> 
> | Options                    |                                                      |
> |----------------------------|------------------------------------------------------|
> | ```-t or –truncate-set1``` | Truncate SET1 to size of SET2 |
> | ```-d``` | Delete characters from SET1 <br> No need for a SET2  |
> 
> Example: B→b, C→c, G→c <br>
> ![](../../Image/Exported%20image%2020250304130201-2.png)
   
<br>

> ```uniq``` <br>
> Delete duplicate lines 
> ![](../../Image/Exported%20image%2020250304130203-3.png)

<br>
    
> ```od``` <br>
> * For displaying files that are not easily displaced in ASCII <br>
> * e.g. audio files etc will look like gibberish <br>
> * od (stands for octal dump) displays a file in octal (base 8) numbers by default <br>
> ![](../../Image/Exported%20image%2020250304130205-4.png)
