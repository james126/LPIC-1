# Extracting data from RPMs

Extra data from RPM withiout installing the package
e.g. to view the original source code, fonts etc
<br>

### Steps
<li>convert to cpio file</li>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;use rpm2cpio program

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`rpm2cpio package.rpm > package.cpio`
<br>

<li>extract the data</li>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`cpio -i --make-directories < package.cpio`
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**-i** extract
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**-make-directories** creates directories

