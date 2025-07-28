# Configuring units

### Configuration file
each unit requires a configuration file
defines what program it starts
how it should be started
files are stored in `/lib/systemd/system`
<span>&nbsp;</span>

#### Service
<img src="../../../Image/ssh.service.png" style="width:50%;border:1px solid lightgrey">

**/usr/sbin/sshd** program to run
**After=...** services to run after
**WantedBy=...** target level the system should be in
**Restart=...** how to reload the program
<span>&nbsp;</span>

#### Target
define which service units to start
<img src="../../../Image/graphical.target.png" style="width:80%;border:1px solid lightgrey">

**Requires, After, Conflicts**