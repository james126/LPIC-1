# Configuring RPM/Yum package managers

The main use is to add architecture optimizations for your CPU

> #### RPM
> the main config file */usr/lib/rpm/rpmrc* - you shouldn't edit this file
> instead create and edit */etc/rpmrc*
> <br>
>
> example optimizations: `optflags: athlon -02 -g -march=i686`
> this line tells RPM when building for athlon platform use those options

> #### Yum
> configured via:
> `/etc/yum.conf` 
> `/etc/yum.repos.d/` - a directory, each has files that desribe a repository

