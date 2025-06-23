### Rebuilding Library Cache
Linux doesn't read ```etc/ld.so.conf``` every time a program runs. Instead it relies on a cached list stored in binary format in ```/etc/ld.so.cache```. <br>

The drawback is that you must rebuild the cache every time you add or remove libraries. <br>
To do this use ```ldconfig``` <br>

Both RPM and Debian packages typically run ```ldconfig``` automatically after installing/removing a package.

> ``ldconfig``
>
>|    | options                                                                                                                  |
>|----|--------------------------------------------------------------------------------------------------------------------------|
>| -v | *Display verbose information* <br> normally it won't display any information                                             |
>| -N | *Don't rebuild cache* <br> don't update library cache, but update symbolic links to libraries                            |
>| -n | *Process only specified directories* <br> update links in directories specified only                                     |
>| -X | *Don't update links* <br> update cache but not links                                                                     |
>| -p | *Display current information* <br> display current cache - all of the library directories and the libraries they contain |

