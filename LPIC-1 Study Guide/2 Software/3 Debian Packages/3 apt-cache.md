### apt-cache
provides info about the Debian package database <br>

| Features                    |                                                                                                                               |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| **Package Info**            | ```apt-cache showpkg```                                                                                                       |
| **Package Statistics**      | ```apt-cache stats``` <br> how many packages installed <br> how many dependencies recorded                                    |
| **Find Unmet Dependencies** | ```apt-cache unmet``` <br> if a program is reporting missing libraries of files                                               |
| **Display Dependencies**    | ```apt-cache depends``` <br> shows all of a packages dependencies                                                             |
| **Locate All Packages**     | ```apt-cache pkgnames str``` <br> shows names of all packages installed on system <br> ```str``` those that begin with string |
