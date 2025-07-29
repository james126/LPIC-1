# RPM
RedHat Package Manager
<br>

 #### Package Naming Convention
 `packagename-a.b.c-x.arch.rpm`

 
 |               |                                            | 
 |---------------| ------------------------------------------ |
 | `packagename` | name of package                                              |
 | `a.b.c`       | version number                                               |
 | `x`           | build/release <br> minor changes to build    |
 | `arch`        | cpu architecture<br> e.g. i386 for any x86 CPU from 80386 onwards<br> `noarch` cpu-independent package<br> `src` source package|

### Compatibility issues
packages can use linux distro files that are not present on your distro
e.g. a package may require a newer version of a library than you have
<hr>

# Commands
#### package and files
<li>filename may be samba-4.1.9-4.fc20.x86_64.rpm</li>
<li>package name is samba</li>
<li>install multiple packages my separating with spaces</li>

> `rpm [operation][options] [package/file]`
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
<hr>

# Yum 
alternative to `rpm`
automatically locates packages by searching its repositories

> `yum [options] [command] [package]`
> 
> |           |                            |
> |------------------|----------------------------|
> | **command**          |                            |
> | `install`        |                            |
> | `update`         | update or                  |
> | `check-update`   | check if updates available |
> | `remove` `erase` | uninstall                  |
> | `list`           | display package info       |

options available depend on the command# Extracting data from RPMs

Extra data from RPM without installing the package
e.g. to view the original source code, fonts etc
<br>

### Steps
<li>convert to cpio file</li>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;use rpm2cpio program

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`rpm2cpio package.rpm > package.cpio`
<br>

<li>extract the data</li>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`cpio -i --make-directories < package.cpio`
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**-i** extract
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**-make-directories** creates directories
<hr>

# Configuring RPM/Yum package managers
The main use is to add architecture optimizations for your CPU

> #### RPM
> the main config file */usr/lib/rpm/rpmrc* - you shouldn't edit this file
> instead create and edit */etc/rpmrc*
> <br>
>
> example optimizations: `optflags: athlon -02 -g -march=i686`
> this line tells RPM when building for athlon platform use those options

> #### Yum
> configured via:
> `/etc/yum.conf` 
> `/etc/yum.repos.d/` - a directory, each has files that describe a repository

