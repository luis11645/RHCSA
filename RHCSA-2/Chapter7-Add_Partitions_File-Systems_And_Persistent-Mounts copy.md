# 7.1 #

* `parted /dev/vda unit s` work with unit type sector, we can specify B,MiB,GiB,TiB, MB,GB or TB unit types.
* `parted /dev/vdb help mkpart` we can use the help command with the argument mkpart to see which options are available
* use `uveadm settle` to detect new added partition
* We can use `rm <partition-number>` inside parted command to delete a partition
* `lsblk --fs` to see partitions UUIDs 

# 7.3 #

* activate swap specified in /etc/fstab with the command `swapon -a`
* Show status of swap with the command  
