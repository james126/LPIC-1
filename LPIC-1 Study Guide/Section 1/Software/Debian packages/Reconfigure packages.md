# Reconfiguring packages

Install scrips often ask a handful of questions
to re-customise run `dpkg-reconfigure [package]`
<br>

### Debian source packages
Files that are used to build the binary package that you interact with
contains:
<li><mark>tarball</mark></li>
<li>patch file - used to modify source code</li>
<li>.dsc file - contains a digital signature to verify the files</li>
You can compile these to create a Debian binary package

> ### tar
> `.tar`
> stand for **T**ape **AR**chiver
> bundles files and directories together but doesn't compress them
> `tar something.tar file1 file2 dir1`
> <br>
> 
> ### tarball
> A compressed tar file (like a zip file)
> `.tar.gz` (**tar** + **gzip** compression)
