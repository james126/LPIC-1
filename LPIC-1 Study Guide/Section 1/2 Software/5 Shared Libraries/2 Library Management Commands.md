### Library Management Commands
```ldd``` <br>
Displays a programs shared libraries <br>
*Example*
```ldd /usr/bin/date``` finds what files the date command uses
> ![](../../Image/ldd.png) <br>
Each line begins with a library name e.g. linux-vdso.1, if it doesn't contain a complete path it attempts to find the true library and display its path using the => symbol. <br>
You don't need to worry about the hexidecimal number. <br>


