# GRUB 2

Works with BIOS and EFI (Extensible Firmware Interface)
<span>&nbsp;</span>

### Configuration 
Config file `/boot/grub/grub.conf`
example
<img src=../../../Image/grub2.png style="width:70%;border:1px solid lightGrey;">
|||
|-|-|
| `menuentry` | title |
| `set root =` | sets root directory<br>partitions start from 1, not 0 |


### Editing Configuration
Don't edit `/bot/grub/grub.conf`
* instead edit `/etc/grub.d` and `/etc/default/grub`
* then use `update-grub` to makes changes to grub.conf
* when you run update-grub it outputs to standard output. To save the changes `update-grub > /boot/grub/grub.cfg`