> ### cat
> ```cat first.txt second.txt > combined.txt```
>
> **Options**
>
> |                          |                                                                                                                                                                           |
> |----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
> | Display line ends          | ```-E or --show-ends```  <br>Adds $ at end of each line                                                                                                                     |
> | Number lines               | ```-n or –number```  <br>Adds line number to start of each line                                                                                                             |
> | Minimize blank lines       | ```-s or --squeeze-blank```  <br>Compresses groups of blank lines to a single line                                                                                          |
> | Display special characters | ```-T or --show-tabs``` displays characters such as ^A <br/> ```-v or --shownonprinting``` displays most control and other special caracters using carat (^) and M- notations |

<br>

> ### tac
> Similar to cat but it reverses the order of lines in the output<br>
> ![](../../Image/Exported%20image%2020250304130149-0.png)

<br>

> ### join
> Like a database join <br>
> By default, uses the first field as they key to match across files <br>
> ![](../../Image/Exported%20image%2020250304130150-1.png) <br>
> Can specify another field to use as key by using –1 or –2 option <br>
> ```join –1 3 –2 2 cameras.txt lenses.txt``` <br>
> &nbsp;&nbsp;&nbsp;&nbsp; join using 3rd field in cameras and 2nd field in lenses

<br>

> ### paste
> Merge files line by line, separating each line with a tab
> ![](../../Image/Exported%20image%2020250304130155-2.png) |
