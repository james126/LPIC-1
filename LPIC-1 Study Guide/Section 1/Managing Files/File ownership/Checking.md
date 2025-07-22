# Checking

File permission tiers:
<ol>
<li>owner</li>
<li>group</li>
<li>other users</li>
</ol>

> `ls -l`
> ![alt text](../../../Image/filepermissions.png)
> **owner** james -rw
> **group** james

> #### Permission strings
> -rw-rw-rw--
> | index | |
> |-|-|
> | 1 | file type: <br> `-` regular file<br> `d` directory<br> `l` symbolic link |
> | 2,3,4 | *owner permissions*<br> **r**ead **w**rite **e**xecute |
> | 5,6,7 | *group permissions* |
> | 8,9,10 | *other permissions* |