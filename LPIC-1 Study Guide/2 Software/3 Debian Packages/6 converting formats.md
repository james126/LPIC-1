### RPM to Debian
You can convert between package formats with a utility like *alien* <br>
It may not be installed by default <br>
<br>
```apg-get install alien``` <br>
<br>
* Requires you have both RPM and Debian package systems installed to convert between these formats <br>
* Doesn't always convert dependency information correctly <br>
<br>
> Syntax <br>
> ```alien [options] file[...]``` <br>
> 
> | option   |                           |   
> |----------|---------------------------|
> | --to-deb |                           |   
> | --to-rpm |                           |   
> | --to-slp | convert to Stampede       |   
> | --to-tgz | convert to tarball format | 
