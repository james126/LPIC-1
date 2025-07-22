# Links

Like shortcuts in Windows
<span>&nbsp;<span/>

### Hard links
* two entries that point to the same file
* links must be on the same filesystem as the file
* to delete the file, you must delete both
<span>&nbsp;<span/>

### Symbolic links (soft links)
* a file that points to the linked-to file
* can point across filesystems


### Creating links
> #### ln
> link
> `ln [options] source link`
> **source** - original file
> **link** name of link you want to create
> by default creates hard links
> | | |
> |-|-|
> | `-s` `--symbolic` | create symbolic link |


> #### Existing links
> example
> <span>&nbsp;<span/>
> 
> `ls -l` shows link count
> ![](../../../Image/createlinks.png)
> ![](../../../Image/showlinks.png)
> <li>3 hard links pointing to inode</li>
> <li>symlink.txt has link count 1</li>
> <li>symbolic links have their own inode</li>
> <span>&nbsp;<span/>
> 
> `ls -i` shows inode number of each file
> ![](../../../Image/linkinode.png)





