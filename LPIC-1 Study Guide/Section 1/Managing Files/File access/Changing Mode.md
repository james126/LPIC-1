# Changing Mode
modify file permissions

> #### chmod
> change mode
> `chmod [options] [mode] filename`
> | | |
> |-|-|
> | `-R` `--recursive` | changes all files in directory tree |
>
> example
> `chmod 644 file.dat`

#### Setting Special Permissions
add a number before the three octal digits
setting the first digit as 0 removes all special permissions
<span>&nbsp;</span>

**bit permissions:**
1 sticky bit permission
2 SGID permission
4 SUID permission
<span>&nbsp;</span>

example
`chmod 6750 program.sh`
SGID = 2
SUID = 4
2+4=6
<span>&nbsp;</span>

#### Symbolic Mode
codes for permissions
![](../../../Image/symbolicmode.png)
example
`chmod a+x bigprogram`
`chmod g=u bigprogram`