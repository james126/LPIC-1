# Libraries
<li>many packages can use the same shared library</li>
<li>you can have multiple versions of the same library installed</li>
<li>major package upgrades are installed side by side with their older counterparts</li>
<li>the files have a <mark>.so</mark> or .so.version extension, similar to Windows .dll files</li>
<br>

**static libraries** - contained in the package
**dynamic libraries** - shared
<hr>

### System Library path
contained in `/etc/ld.so.conf`
example - *include /etc/ld.so.conf.d/*.conf*
can have multiple paths
Linux also refers to trusted libraries in `/lib` and `/usr/lib`
<br>

### Environment variable
`LD_LIBRARY_PATH`
specifies additional directories to search for libraries
example `export LD_LIBRARY_PATH=/usr/local/testlib:/opt/new/lib`
specifies 2 paths separated by <mark>:</mark>
<br>

### Errors
**example**
<img src="../../../Image/libraryerror.png" style="border:1px solid darkgrey;width:90%">
it could find the library *libXinerama.so.1*
<br>

**troubleshooting**
<li>check if library installed</li>
<li>if library is installed, you may need to add it to the Library Path</li>
<li>Sometimes the librarys <mark>path is hardcoded</mark> in the programs binary file, you can create a symbolic <mark>link</mark> from where the program expects it and the location of the library on your system</li>
<br>

**example**
A program may link to `biglib.so.5` but you have `biglog.so.5.2` installed, so creating a <mark>link</mark> would solve the problem
<hr>

# Library Management
*<mark>libraries can depend on other libraries
so a library may be there, but its dependencies are not installed</mark>*

> ### ldd
> displays a programs shared libraries
> example
> <img src="../../../Image/ldd.png" style="opacity:0.7" >

> ### ldconfig
> updates caches and links used by the system for locating libraries
> it reads */etc/ld.so.conf* and implements any changes in that file
<hr>

# Rebuilding Library Cache
Linux doesn't read `etc/ld.so.conf` every time a program runs
instead it relies on a cached stored in `/etc/ld.so.cache`
it runs automatically when you install/uninstall packages

> To update the library cache manually, use `ldconfig`
> #### ldconfig
> |    |                                                       |
> | -- | ----------------------------------------------------------- |
> |    | **option**                                                      |
> | -v | display verbose information                                 |
> | -N | don't rebuild cache, but update symbolic links to libraries |
> | -p | display current cache                                       |
