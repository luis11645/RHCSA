# Chapter 3 #
## 3.7 make link between files and directories ##

* To make links between files we have two ways, hard links and soft links. Links that ares made using hard links points to the same inode and we only can make hard links with regular files and not across file systems. You can create hard links using the command `ln <original_file> <destination_file>`
* Soft links are like shorcuts in Windows and you can use softlinks with directories, you can create soft links using the command `ln -s <newlink> <origin>`
