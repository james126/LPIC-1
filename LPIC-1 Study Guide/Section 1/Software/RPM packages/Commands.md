# Commands
<br>

 #### package and files
<li>filename may be samba-4.1.9-4.fc20.x86_64.rpm</li>
<li>package name is samba</li>
<li>install multiple packages my separating with spaces</li>
<br>

> `rpm [operation][options] [package/file]`
> <br>
> 
> operations
> |                            |                                                     |
> | -------------------------- | --------------------------------------------------- |
> | `-i`                       | install                                             |
> | `-U`                       | install or upgrade                                  |
> | `-F` `--freshen`           | upgrade                                             |
> | `-e`                       | uninstall                                           |
> | `-q`                       | query - checked if installed, files it contains etc |
> | `-V` `--verify`            | verify - check files unchanged since install        |
> | `-b`                       | build package - from source code and config files   |
> 
> options
> |                 |                |                                |
> | ----------------| ---------------| ------------------------------ |
> | `-h` `--hash`   | -i, -U, -F     | display # to show progress     |
> | `--nodeps`      | -i, -u, -F, -e | no dependency checks be performed |
> | `--test`        | -i, -U, -F     | check for dependency conflicts without installing package |
> | `--prefix path` | -i, -U, -F     | set installation directory     |
> | `-i`            | -q             | display package info           |

*examples*
install or upgrade a package
`rpm -Uh samba-4.1.8-4.fc20.x86_64.rpm`
**-U** install or upgrade
**-h** display # progress bar
<br>

display package info
`rpm -qi sambs`
**-q** check if installed
**-i** display info
