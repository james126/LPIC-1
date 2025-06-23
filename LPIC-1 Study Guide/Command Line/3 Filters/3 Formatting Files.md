Format text if a file

> ```fmt``` <br>
> By default formats paragraphs 75 characters wide <br>
>
> | Options              |   |
> |----------------------|---|
> | ```-w width``` <br> ```--width=width``` | Set line length to width characters |

<br>

> ```nl``` <br>
> Number lines <br>
> Numbers all non-blank lines <br>
>
> |       |                                                                                                                                                                                        |
> |-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
> | style | ```-b style``` <br> ```--body-number=style``` <br><br> Style <br> T &nbsp; default, numbers lines except empty <br> A numbers lines including empty  |
> | Header and footer style | ```-h style``` <br> ```--header-numbering=style``` <br> ```--f style``` <br> ```--foter-number=style``` |
> | Page seperator | ```-d=code``` <br> ```--section-delimeter=code``` <br> Where code is a character that defines a new page |
> | position | ```-n``` <br> --number-format=format <br><br> Format <br> ln &nbsp; left justified, no leading zeroes <br> rn &nbsp; right justified <br> rz &nbsp; right justified with leading zeros |
>
> Example <br>
> Add lines numbers to a file <br>
> ```nl –b a buggy > numbered-buggy.txt```

<br>

> ```pr``` <br>
> Text formatted for printing <br>
> 80 character line length <br>
> pr myfile.txt <br>
>
> | Options           |                                                                                       |
> |-------------------|---------------------------------------------------------------------------------------|
> | Number of columns | ```-numcols``` <br> ```--columns=numcols``` <br> Creates output with columns          |
> | Double spaced | ```-d``` <br> ```--double-spaced``` <br> Double spaced output from single spaced file |
> | Page length | ```-l lines``` <br> ```--length-lines```  <br> Set length of page in lines            |
> | Header text | ```-h``` <br> ```--header=text``` <br> ```-t or--omit-header``` omits the header      |
> | Left margin | ```-o chars``` <br> ```--indent=chars``` <br> Sets left margin to char caracters      |
> | Page width | ```-w chars``` <br> ```--width cars``` |
>
> Example <br>
> ```cat –n /etc/profile \| pr –d \| lpr``` <br>
> cat –n &nbsp; output with line numbers <br>
> pr –d &nbsp; double space the result <br>
> lpr &nbsp; print the file
