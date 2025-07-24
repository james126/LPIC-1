# Special Permissions

#### Set User ID (SUID)
run the program with the permissions of whoever owns the file
e.g. if a file is owned by root, the program runs with root privileges
<span>&nbsp;<span>

SUID is shown by a <mark>s</mark> in the owners execute bit
if set on a file without user execute permissions, shown by <mark>S</mark>
e.g. `rwSr-xr-x`
<span>&nbsp;<span>

#### Set Group ID (SGID)
sets the group permissions
same rules as SUID
e.g. `rwxr-s-x`
<span>&nbsp;<span>

#### Sticky Bit
set on a directory
shown as <mark>t</mark>
directories files can only be deleted by:
<li>their owners</li>
<li>directories owner</li>
<li>root</li>

e.g. `rwxr-xr-t`


