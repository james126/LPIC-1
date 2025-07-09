### RPM
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

<br>

### Compatability issues
packages can use linux distro files that are not present on your distro
e.g. a package may require a newer version of a library than you have 
