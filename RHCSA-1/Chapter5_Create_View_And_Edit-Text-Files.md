# Create,View, And Edit Text Files #

## 5.1 Redirect output to a file or program ##
* We can use `>` operator to send output to a file or discard message sending to `/dev/null`
* Also we can use the operator `> file 2> /dev/null` to send output to a file and discard error messages
* We can use `tee` command to show output to the terminal and save output to a file at the same time. eg `find / -name 'prueba' | tee salida`
* We can use `tee -a` to append output to a file instead of replacing.

## 5.3 Edit Text Files from the shell prompt ##
* You can use shift + v inside vi or vim editor to enter multiline selector.
* you can use `v` command to enter in multiselector
* You can usr `ctrl+v` to enter in block selection
* /etc/vimrc is the global configuration file and each user have ~/.vimrc file to edit vim configuration on user scope only

## 5.5 Change the shell Environment ##
* Interactive login shell source from /etc/profile and ~/.bash_profile while non interactive login shell only source /etc/bashrc and ~/.bashrc
* 