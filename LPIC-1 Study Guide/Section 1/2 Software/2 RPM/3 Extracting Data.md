### Extract files without installing package
RPM files are modified ```cpio``` archives <br>
To do this you use the ```rpm2cpio``` program <br>
It takes a single argument - name of RPM file - and outputs cpio archive <br>
<br>
> Example <br>
> ```rpm2cpio samba-4.1.9-4.fc20.src.rpm > samba-4.1.9-4.fc20.src.cpio``` <br>
> <br>
> extract data <br>
> ```cpio -i --make-directories < samba-4.1.9-4.fc20.src.cpio``` <br>
> ```-i``` &nbsp; option extract archive <br>
> ```--make-directories``` &nbsp; creates directories
