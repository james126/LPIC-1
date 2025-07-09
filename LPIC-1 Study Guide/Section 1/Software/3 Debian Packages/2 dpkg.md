### dpkg
* Debian Package Manager <br>
* **Debian packages are incompatible with RPM packages** <br>
* Use *dpkg* command to install a Debian package

```dpkg [options][action] [package-files|package-name]``` <br>


> | action                                        |                                                                             |
> |-----------------------------------------|-----------------------------------------------------------------------------|
> | ```-i``` ```--install```                | requires package filename                                                   |
> | ```--configure```                       | reconfigure installed package: runs post-installation script to set options |
> | ```r``` ```--remove```                  | remove package but leave config files                                       |
> | ```-P``` ```--purge```                  | remove package and config files                                             |
> | ```--get-selections```                  | display installed packages                                                  |
> | ```-p``` ```--print-avail```            | display info about installed package                                        |
> | ```-I``` ```--info```                   | display info about uninstalled package                                      |
> | ```-l pattern``` ```--list patter```    | list installed packages whose names match *pattern*                         |
> | ```-L``` ```listfiles```                | list files associated with a package                                        |
> | ```-S pattern``` ```--search pattern``` | find packages that own the file *pattern*                                   |
> | ```-C`1` ```--audit```                  | find partially installed packages and suggest what to do with them          |


> | option                          | used with action |                                                                            |
> |---------------------------------|------------------|----------------------------------------------------------------------------|
> | ```--no-act```                  | -i, -r           | checks for dependencies, conflicts without install or removing the package |
> | ```-G```                        | -i               | don't install package if new version of same package is installed          |
> | ```-E``` ```--skip-same-version``` | -i               | don't install package if same version of package already installed         |
> |                                 |                  |                                                                            |

