# 10.1 #

* we can find kernel parameters in `/proc/cmdline`
* The file `/etc/default/grub` is the configuration file for grub to end users.
* `grub2-mkconfig` command generates the `/boot/grub2/grub.cfg` and `/boot/efi/EFI/redhat/grub.cfg` files.
* `systemctl list-dependencies graphical.target` show all the targets and services that depends on grafical.target.

# 10.3 Reset root password #

1-Reboot the system
2-interrupt the boot hittin any key
3-edit grub setting with the key `e`
4-Go to kernel option and go to the final part with the key `end`
5-type rd.break at the end an press `ctrl+x`
6-type `mount -o remount,rw /sysroot`
7-type `chroot /sysroot` and then change password with `passwd`
8-type touch `/.autorelabel`
9-and then type exit and exit