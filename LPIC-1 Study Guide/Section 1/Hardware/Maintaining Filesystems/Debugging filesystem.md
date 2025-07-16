# Debugging filesystem

> `debugfs`
> view and modify a filesystem
> similar to *dumpe2fs*, *tune2fs*
> prompts for commands:
> | | |
> |-|-|
> | `show_super_stats` `stats` | show superblock information |
> | `stat [filename]` | show inode data on a file |
> | `undelete insode name` | undelete a file |

**superblock**
<li>like a table of contents for a filesystem</li>
<li>contains information the OS needs to sue it</li>
<br>

**inode**
<li>index node</li>
<li>stores metadata about a file or directory</li>
<li>doesn't include it's name and content</li>
<li>e.g. file type, permissions, size etc </li>