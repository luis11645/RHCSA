# Chapter 7 #

## 7.5 Manage Default Permissions and File Access ##

Special permissions
* `chmod u+s` applies on file and it execute the file as the user that owns the file, very useful for scripts.
* `chmod g+s` can be applied on files and executes the file as the group that owns the file. When is applied to a directory the files that are created on this directory inherit the group of the parent folder
* `chmod o+s` this is called sticky bit and it is applied to a directory only, only the user that is owner of a file in this directory and have write permissions is capable of the deletion of this file
* Using the octal method the 4 represent the suid the 2 represent the gsuid and the 1 represent the sticky bit
* You can delete special permissions with the octal method by using 00777 for eg.
* in redhat 9 the default umask for all users is 0022
* the default permissions for a regular user of a file is 0666 and of a directory is 0777
* You can chage the default umask in /etc/login.defs configuration file