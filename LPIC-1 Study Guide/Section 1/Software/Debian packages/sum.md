# Intro

### dpkg
Debian Package Manager
<li>low level package manager</li>
<li>used to install, configure, remove and query packages</li>
<li>does not handle dependencies and has no knowledge of repositories</li>
<br>

### apt
Advanced Package Tool
<li>high level package manager</li>
<li>automatically resolves dependencies</li>
<li>gets packages from repositories</li>
<br>

#### dpkg (low level package manager)

Debian Package Manager
syntax:
`dpkg [options][action] [package]`
<br>

<li>Because dpkg can take a package filename as input, it's the preferred way of <mark>installing a package you have already downloaded</mark></li>
<li>Doesn't upgrade packages, you have to remove the old one and install the one</li>


> |                           |                                                                             |
> |---------------------------------|-----------------------------------------------------------------------------|
> | **action**                          |                                                                             |
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


 > |                      |  |                              |
 > | -------------------------- | ---------------- | ---------------------------- |
 > | **option**                     | **used with action** |                              |
 > | `--no-act`                 | -i, -r           | checks for dependency conflicts without installing or removing |
 > | `-G`                       | -i               | don't install package if new version of same package is installed |
 > | `-E` `--skip-same-version` | -i               | don't install package if same version of package already installed |
 > |                            |                  |                              |
<hr>

# apt
<mark>**apt** is a newer tool
it combines **apt-get**, **apt-cache** and **apt-config**</mark>
<li>apt-get lets you install, remove... packages</li>
<li>apt-cache shows you info from the package database</li>
<hr>

# apt-get
Repositories list
**/etc/apt/sources.list**
<br>

syntax
`apt-get [options][command][package]`
usually you won't use options

|                 |                                                  |
| ---------------------- | ------------------------------------------------ |
| **command**                |                                                  |
| `install`              |                                                  |
| `remove`               |                                                  |
| `purge`                | <mark>removes package and configuration files</mark> |
| `update`               | says how many packages can be upgrades           |
| `upgrade`              | upgrade all packages                             |
| `dist-upgrade`         | upgrade package if it doesn't break a dependency |
| `download`             | download package only                            |
| `clean`                | clear local cache (not database) of downloaded packages         |

|                  |                                         |         |
| ---------------------- | ------------------------------------------------ | ------- |
| **option**                 | **used with**                                        |         |
| `-d` `--download-only` | upgrade, dselect-upgrade, install, source        | downloads packages without installing |
| `-f` `--fix-broken`    | install, remove                                  | fix system on which dependencies are unsatisfied |
<hr>

# apt-cache
|                     |                                                |
| --------------------------- | ---------------------------------------------- |
| **command**                    |                                                |
| `showpkg`            | show package info                        |
| `stats`      | package stats - how many you've installed etc |
| `unmet` | if a program has missing libraries/files |
| `depends [package]`    | show package dependencies |
| `pckgames`     | shows all installed packages <br> if followed by a string, only those that begin with the string |
<hr>

# Reconfiguring packages

Install scrips often ask a handful of questions
to re-customise run `dpkg-reconfigure [package]`
<br>

### Debian source packages
Files that are used to build the binary package that you interact with
contains:
<li><mark>tarball</mark></li>
<li>patch file - used to modify source code</li>
<li>.dsc file - contains a digital signature to verify the files</li>
You can compile these to create a Debian binary package

> ### tar
> `.tar`
> stand for **T**ape **AR**chiver
> bundles files and directories together but doesn't compress them
> `tar something.tar file1 file2 dir1`
> <br>
> 
> ### tarball
> A compressed tar file (like a zip file)
> `.tar.gz` (**tar** + **gzip** compression)
