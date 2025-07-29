# Packages

#### Libraries
Software that be used by many different programs
<br>

#### Package Management
Relates to programs (*processes*) on your computer
Two main package management systems:
<ol>
<li><mark>RPM (RedHat Package manager)</mark></li>
<li><mark>DEB (Debian)</mark></li>
</ol>

*You can't install a RPM package on a Debian system and vice versa*
<br>

#### Package
once installed, consist of files on you computer
<br>

#### Database
contains info about installed files
<br>

#### Dependencies
libraries that a package requires
<br>

#### Binary Package Creating
download course code and using tools create a binary package
can install the package
<hr/>

# Dependency conflicts
**Dependency problems**
* Missing libraries/support packages
* Incompatible libraries - wrong version
* Duplicate libraries
* Mismatched name - same libraries but different name
<br>

**Workarounds**
* forcing the installation
with dpkg ```--ignore-depends=package``` ```--force-depends``` ```--force-conflicts``` <br>
* upgrading, downgrading or replacing the dependency
* rebuilding the package - 
<br/>

### RPM to Debian

*alien* lets you convert between RPM and Debian packages
<li>requires you have both RPM and Debian package managers</li> 
<li>having another package manager isn't a problem as long as you don't use it</li>

> ### alien 
> ```alien [options] file[...]``` <br>
> 
> |    |                           |   
> |----------|---------------------------|
> | **option**   |                           |   
> | --to-deb |                           |   
> | --to-rpm |                           |    
> | --to-tgz | convert to tarball format | 
