Dependency problems
* Missing support package
* Incompatible support package
* Duplicate support package
* Mismatched name (RPM and Debian package names don't always match)

Work arounds:
* forcing the installation <br>
with dpkg ```--ignore-depends=package``` ```--force-depends``` ```--force-conflicts``` <br>
* upgrading, downgrading or replacing the dependency
* rebuilding the dependency 
