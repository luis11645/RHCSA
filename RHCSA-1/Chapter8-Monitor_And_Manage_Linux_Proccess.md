# Chapter 8 #

## Processes States and Lifecycle ##
* We can use ps --forest to display processes in a tree format, and use -O or --sort option to sort it
* Forking is when a parent process create subprocess or childs
* The command ps has few ways for the arguments for instance `ps aux` is the BSD way and is not the same that `ps -aux` the Unix way

## Control jobs ##
* A job that is not belong to a controlling terminal is marked with a (?) in the ps in the TTY colum
* the `+` sign the listing jobs indicates that job is the default, the others can have the `-` sign
  
## Kill processes ##

* HUP signal or the number `1` signal repot termination of the controlling process of a terminal
* KILL signal or number `9` causes abrut of force the program to stop
* TERM or signal number 15 is the cleanest way to stop a program, it send a signal to the program to stop
* You can use `pgrep -l -u <username>` to list all the processes belongs to a specific user
* You can use pkill -<killsign> -u <username> to kill or terminate all the processes belongs to a user
* You can use pkill -t <terminal-id> to match a specific TTY
* Also you can use pstree -p <username> to see the parent processes of a user and then kill it with the command `pkill -P <parent-process>` to kill all the child process.

## Monitor Process ACtivity ##
* wen can calculate the real load of a Linux system by dividing the numbers of core by the load average if the result is below 1 the system is good and if is above 1 the system is overload.