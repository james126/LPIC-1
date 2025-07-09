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
