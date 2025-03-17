# Locate Files on the system #

* `locate -i` command search case insensitive files or directories
* `find -user developer` perform a search for files with the owner developer
* `find -group developer` perform a search for files with the group developer
* We can user `find -uid` or `find -gid` aswell
* When we are search files for a speficic permissions we have to use `find -perm -755` for example we are searching files with this specific permissions.
* Also if you want to search files for a least a specific permissions we have to use the `/` symbol for instance `find -perm /754`
* 