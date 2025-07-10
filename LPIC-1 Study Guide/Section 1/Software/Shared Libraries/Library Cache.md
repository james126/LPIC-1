# Rebuilding Library Cache

Linux doesn't read `etc/ld.so.conf` every time a program runs
instead it relies on a cached stored in `/etc/ld.so.cache`
it runs automatically when you install/uninstall packages

> To update the library cache manually, use `ldconfig`
> #### ldconfig
> |    | option                                                      |
> | -- | ----------------------------------------------------------- |
> | -v | display verbose information                                 |
> | -N | don't rebuild cache, but update symbolic links to libraries |
> | -p | display current cache                                       |

