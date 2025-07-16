# Checking for errors

Bugs, power failures and mechanical problems can corrupt data structures on a filesystem

> #### fsck
> uses tools like `e2fsck`
> only use on unmounted filesystems
> <br>
> `fsck [options] filesystem`
> options:
> | | |
> |-|-|
> | `-A` | check all files |
> | `-C` |show progress |
> | `-N` | no action<br> just describe what it would normally do |
>
> 