### Package
Bundles collection of files that can be installed using a package manager <br>

### Library
Collection of reusable code that programs can use to perform common tasks <br>
**Example**
* libc.so (C standard library)



Most programs use their libraries as shared libraries <br>
They include references to a shared library which can be loaded with the program <br>
They are similar to *.dll* files in windows, in linux that have a *.so* or *.so.version* extension<br>

### Locating Library Files
```/etc/ld.so.conf``` contains lines, each list a directory in which shared library files can be found <br>
This lets package maintainers add their library directories to the list <br>
<br>
Linux also contains libraries in ```/lib``` and ```/usr/lib```. These are always on the library path even if they are not listed in ```/etc/ld.so.conf``` <br>

### Correcting Problems
You may get errors like this <br>
```error while loading shared libraries: libXinerama.so.1: cannot~CA open shared object file: No such file or directory``` <br>
This means it could find the library. If the file isn't installed you can track down the package (google search) where it belongs and install it. If the file is available, you can add its directory globally or to LD_LIBRARY_PATH. <br>

Sometimes the librarys path is hardcoded in the programs binary file, when this happens you need to create a symbolic link from where the program expects it and the location of the library on your system. <br>

*Example* <br>
A program may link to ```biglib.so.5``` but you have ```biglog.so.5.2``` installed, so creating a link would solve the problem. <br>
```ln -s biglib.so.5.2 biglib.so.5``` <br>
you must type this command as the root in the directory tha the library resides. You must them run ```ldconfig```. <br>

