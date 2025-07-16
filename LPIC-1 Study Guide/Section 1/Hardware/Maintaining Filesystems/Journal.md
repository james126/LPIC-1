# Journal

#### What is a Journal
<li>a file that records changes it intends to make *before* committing those changes to the main file system</li>
<li>it's like a "to-do" list</li>
<br>

#### Prevents inconsistencies
<ol>
<li>if there's a crash/power failure, the system can check and journal and examine data structures described in it</li>
<li>if there are inconsistencies, it can do a roll-back</li>
</ol>

Journaling filesystems are standard in most partitions
<br>

#### Checking for a journal
![](../../../Image/journal.png)

> `tune2fs`
> to modify the journal:
> | | |
> |-|-|
> | `-J size=journal-size` | set journals size |
> | `-J device=external-journal` | set device on which it's stored |

