# File Attributes
you can change attributes for most file systems using `chattr`

> #### chattr
> `chatter +/-[option] file`
> options
> | | |
> |-|-|
> | `A` | no access time updates<br/> don't updated access timestamp when accessing a file |
> | `i` | immutable<br/> don't updated access timestamp when accessing a file |
>
> example
> `chattr +i important.txt`