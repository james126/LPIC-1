### apt -get
Similar to Yum <br>
```/etc/apt/sources.list``` contains repos packages downloaded from <br>
<br>
```apt-get [options][command][package-names]``` <br>
In most cases you won't use options, just a command and package names <br>

| command            |                                                                         |
|--------------------|-------------------------------------------------------------------------|
| ```install```      | install by package name                                                 |
| ```remove```       | remove by package name                                                  |
| ```update```       | update a package                                                        |
| ```upgrade```      | upgrade all packages                                                    |
| ```dist-upgrade``` | upgrade and handles changing dependencies with new versions of packages |
| ```download```      | download package only                                                   |

| option                         | used with                                 |                                                  |
|--------------------------------|-------------------------------------------|--------------------------------------------------|
| ```-d``` ```--download-only``` | upgrade, dselect-upgrade, install, source | downloads packages without installing            |
| ```-f``` ```--fix-broken```        | install, remove                           | fix system on which dependencies are unsatisfied |

