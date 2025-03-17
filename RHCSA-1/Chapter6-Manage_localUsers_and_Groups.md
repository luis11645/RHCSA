# Chapter 6 Manage Local Users and Groups #

## 6.3 Gain Superuser Access ##

* `/etc/login.defs` file define default configuration parameters like password expiration, default home, and so on. 
* To enable a user to use sudo you can add the user to the wheel group
* Also we can edit the `/etc/sudoers` file to enable user to gain super user access
* In the sudoers file the sintaxis is `ALL=(ALL) ALL` the first ALL represent the host that can run the command, the second ALL represent the user that you can become and the third ALL represent the commands that you can run
* `groupmod -n <oldname> <newname>` command change a group name
* if we use `usermod -G` to add a user secondary groups it will replace the olders groups to avoid this we nee to use `-a` option eg. `usermod -aG <groupname> <username>`
* You can use `newgrp` command to switch a user to another primary group only for that shell session
* We can calculate the days in the future with the YYY-MM-DD format using the command `date -d "+<number> days" -u`
* You can use usermod -L -e <YYY-MM-DD> <user> to expire a user at certain date