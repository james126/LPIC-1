# Disk Space
`df` check disk use by partition
`du` space by directory

> #### df [options] [files]
> | | |
> |-|-|
> | `a` `--all` | all filesystems |
> | `-h` `--human-readable` | use scaled units<br> e.g. instead of 5859784 blocks shows 5.6G (for 5.6GiB) |
> | `-l` `--local` |  local filesystems only<br> not network filesystems |
> | `-T` `--print-type` | shows filesystem type |
> | `-t [fstype]` `--type=fstype` | only show this filesystem type |
>
> example
> ![](../../../Image/df.png)

> ### du [options] [directories]
> how much disk space a disctory is using
> is recursive
> options:
> | | |
> |-|-|
> | -`a` `--all` | reports of individual file sizes as well |
> | `-c` `--total` | show total |
> | `-h` `--human-readable` | same as df |
> | `-s` `--smumarize` | summarize subdirectories |
> | `-x` `--one-file-system` | limit to current filesystem |
>
> ![alt text](../../../Image/du.png)