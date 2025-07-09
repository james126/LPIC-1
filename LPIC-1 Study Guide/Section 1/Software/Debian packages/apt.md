# apt

<mark>**apt** is a newer tool
it combines **apt-get**, **apt-cache** and **apt-config**</mark>
<li>apt-get lets you install, remove... packages</li>
<li>apt-cache shows you info from the package database</li>
<br>

# apt-get
Repositories list
**/etc/apt/sources.list**
<br>

syntax
`apt-get [options][command][package]`
usually you won't use options

| command                |                                                  |
| ---------------------- | ------------------------------------------------ |
| `install`              |                                                  |
| `remove`               |                                                  |
| `purge`                | <mark>removes package and configuration files</mark> |
| `update`               | says how many packages can be upgrades           |
| `upgrade`              | upgrade all packages                             |
| `dist-upgrade`         | upgrade package if it doesn't break a dependency |
| `download`             | download package only                            |
| `clean`                | clear local cache (not database) of downloaded packages         |

| option                 | used with                                        |         |
| ---------------------- | ------------------------------------------------ | ------- |
| `-d` `--downloa-only` | upgrade, dselect-upgrade, install, source        | downloads packages without installing |
| `-f` `--fix-broken`    | install, remove                                  | fix system on which dependencies are unsatisfied |

<br>

# apt-cache
| Fcommand                    |                                                |
| --------------------------- | ---------------------------------------------- |
| `showpkg`            | show package info                        |
| `stats`      | package stats - how many you've insalled etc |
| `unmet` | if a program has missing libraries/files |
| `depends [package]`    | show package dependencies |
| `pckgames`     | shows all installed packages <br> if followed by a string, only those that begin with the string |
