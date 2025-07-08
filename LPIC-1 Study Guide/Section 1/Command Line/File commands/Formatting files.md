# Formatting files
Commands that reformat the text in a file

> ### fmt
> 
> <li>limit text files width</li>
> <li>75 characters by default</li>
> 
> 
> options:
> |                            |                                     |
> |----------------------------|-------------------------------------|
> | `-w width` `--width=width` | set line length to width characters |

> ### nl
> numbers non-blank lines of a file
> options:
> |       | |
> |-------|-|
> | numbering style <br> `-b style-option` <br> `--body-number=style-option` | **style-option** <br> t - default, numbers lines except empty <br> a - number all lines including empty one  |
> | new page <br> `-p` `--no-renumber` | default is to number each new page starting with 1, the options don't reset the line number with a new page |
> | page seperator <br> `-d=code` `--section-delimiter-code` | **code** is the delimeter that defines a new page |
>
> example
> you get error messages that refer to a script line
> to add line numbers to the script
> `nl –b a somescript > numberedscript.txt`

> ### pr
> prepare a file for printing
> by default creates a header which includes: <li>current date/time</li> <li>filename</li> <li>page number</li>
>
> options:
> |                   | |
> |-------------------|-|
> | multicolumn output <br> `-numcols` <br> `--columns=numcols` | creates output with **numcols** columns          |
> | double spacing <br> `-d` <br> `--double-spaced` | double spaced output |
> | page length <br> `-l lines` <br> `--length-lines` | page length in **lines**            |
> | header text <br> `-h text` <br> `--header=text` | set text to be displayed in header, replacing the filename |
> | omit header <br> `-t`  `--omit-header` | |
> | left margin <br> `-o chars` <br> `--indent=chars` | sets left margin to **chars** characters      |
> | page width <br> `-w chars` <br> `--width cars` | |
>
> example
> `cat –n /etc/profile | pr –d | lpr`
> **cat –n** &nbsp; output with line numbers
> **pr –d** &nbsp; double space
> **lpr** &nbsp; print the file
