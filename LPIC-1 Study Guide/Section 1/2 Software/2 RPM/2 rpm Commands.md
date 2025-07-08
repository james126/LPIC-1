> ```rpm``` <br>
> Install or upgrade a package <br>
> ```rpm [operation][options] [package-files|package-names]```
>  
> | operations                  | o                                               |
> |-----------------------------|-----------------------------------------------------------|
> | ```-i```                    | install package                                           |
> | ```-U```                    | install package or upgrade existing                       |
> | ```-F``` or ```--freshen``` | upgrade package                                           |
> | ```-q```                    | query - find out if installed, what files it contains etc |
> | ```-V``` or ```--verify```  | verify - check files unchanged since install              |
> | ```-e```                    | uninstall package                                         |
> | ```-b```                    | build package from source code and config files           |
> | ```--rebuild```             | build package from source RPM file                        |
> | ```--rebuilddb```           | rebuild RPM database to fix errors                        |
> 
> 
> | options                           |                |                                                                                                                                                         |
> |-----------------------------------|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
> | ```-h``` or ```--hash```          | -i, -U, -F     | display # to show progress                                                                                                                              |
> | ```-v```                          | -i, -U, -F     | used with -h to produce a uniform number of hash marks                                                                                                  |
> | ```--nodeps```                    | -i, -u, -F, -e | no dependency checks be performed <br> installs even if it relies of a package that's not present <br> uninstalls even if another package depends on it |
> | ```--test```                      | -i, -U, -F     | checks for dependency conflicts without installing package                                                                                              |
> | ```--prefix path```               | -i, -U, -F     | install directory to path                                                                                                                               |
> | ```-a``` or ```--all```           | -q, -V         | queries or verifies all packages                                                                                                                        |
> | ```-f file``` or ```--file file``` | -q, -V         | queries of verifies package that owns file                                                                                                              |
> | ```-p package-file```             | -q             | queries uninstalled package-file                                                                                                                        |
> | ```-i```                          | -q             | display package info                                                                                                                                    |
> | ```-R``` or ```--requires```      | -q             | display package that this package requires                                                                                                              |
> | ```-l```                          | -q             | display files contained in package                                                                                                                      |>

### Using RPM
combine 1 operation with 1+ options <br>
<br>
A package filename may be samba-4.1.9-4.fc20.x86_64.rpm, but the package name is samba <br>
Some operations require a package filename others a package name <br>
<br>
You can install multiple packages my separating their names by spaces <br>
Automatically installs the depended on packages first or removes it last <br>

<br>

**Examples** <br>
install or upgrade a package <br>
```rpm -Uvh samba-4.1.8-4.fc20.x86_64.rpm``` <br>
-U &nbsp; install or upgrade existing <br>
-vh @nbsp; display # to show progress <br>


display package info <br>
```rpm -q sambs```
