### Environment variables

They hold data referred to by the variable name
Programs can set environment variables for itselfk not for unrelated processes

Shell config files are kept in `~/.bashrc` and `/etc/profile`
<br>

### login shell
- executed for all useres
- owned by root and needs priveledges to modify
- e.g. SSH, console login
<br>

### interactive non-login shell
- a shell that you launch after you've already logged in 
- executed only for invidual user whose home directory it resides
- e.g. logging into desktop environment

> ### .bashrc
> for interactive shell

> ### etc/profile
> for login shells

> ### Setting variables
> `VAR=value` or `export VAR=value` sets current shell session only
> &nbsp; - when setting an enviroment variable, you don't use the **\$** sign
> &nbsp; - referencing a variable, use **\$**