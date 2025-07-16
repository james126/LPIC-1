# Partitioning a disk

#### Partition table format
<img src="../../../Image/gpt.png" width="50%">

> ### fdisk
> fixed disk
> <mark>for MBR patition table format</mark> (Master Boot Record)
> `fdisk [disk]` **disk** that you want to partition
> e.g. `fdisk /dev/hda`
> <br>
>
> | | |
> |-|-|
> | `n` | create a partition
> | `d` | delete a partition
> | `l` | list partitions
>
> example *sudo fdisk -l*
> <img src="../../../Image/fdisk.png" width="50%">

> #### gdisk
> <mark>for GPT table format</mark>
> **G**UID **P**artition **T**able (Globally Unique Identifier)
> <br>
>
> | | |
> |-|-|
> | `n` | create a partition
> | `d` | delete a partition
> | `l` | list partitions

> #### parted
> not in exam
> <mark>for all table formats</mark>
> <li>CLI or GUI</li>
> <li><mark>resize partitions easily (provided their not being used)</mark></li>