# Locating Files

> #### find
> `find [path] [expression]`
> **expression**
> | | ||
> |-|-|-|
> | by name| `-n pattern` | `find . -name "*.txt"` |
> | by file size | `-size [+\|-]n` | by default n is 512-byte blocks<br> can modify by trailing the value with a letter code e.g. M for megabyes<br> `find . -size +10M`  | 
> | by User Id | `-uid UID` | 
> | by username | `-user name` |
> | restrict search depth | `-maxdepth levels` | limit recursive directories to search |

> #### locate
> search from a database updated daily
> search may not return recently created files
> update it manually using `updatedb` which is configured at */etc/updatedb.conf*
> `locate search-string`