# dpkg (low level package manager)

Debian Package Manager
syntax:
`dpkg [options][action] [package]`
<br>

<li>Because dpkg can take a package filename as input, it's the preferred way of <mark>installing a package you have already downloaded</mark></li>
<li>Doesn't upgrade packages, you have to remove the old one and install the one</li>


> | action                          |                                                                             |
> |---------------------------------|-----------------------------------------------------------------------------|
> | `-i` `--install`                | install                                                   |
> | `--configure`                   | reconfigure an installed package - runs install script to set options |
> | `r` `--remove`                  | remove package but leave config files                                       |
> | `-P` `--purge`                  | remove package and config files                                             |
> | `--get-selections`              | display installed packages                                                  |
> | `-p` `--print-avail`            | display info about installed package                                        |
> | `-I` `--info`                   | display info about uninstalled package                                      |
> | `-l pattern` `--list patter`    | list installed packages whose names match *pattern*                         |
> | `-L` `listfiles`                | list files associated with a package                                        |
> | `-S pattern` `--search pattern` | find packages that own the file *pattern*                                   |
> | `-C` `--audit`                  | find partially installed packages and suggest what to do with them          |


 > | option                     | used with action |                              |
 > | -------------------------- | ---------------- | ---------------------------- |
 > | `--no-act`                 | -i, -r           | checks for dependency conflicts without installing or removing |
 > | `-G`                       | -i               | don't install package if new version of same package is installed |
 > | `-E` `--skip-same-version` | -i               | don't install package if same version of package already installed |
 > |                            |                  |                              |

