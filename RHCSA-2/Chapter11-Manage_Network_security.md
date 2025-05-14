# Chapter 11.1 #
* `firewall-cmd --get-default-zone`
* `firewall-cmd --list-all`
* `firewalld-cmd --add-service http --permanent`
* `firewall-cmd --remove-service`
* `firewall-cmd --reload` reload the firewall to load the configuration files
* `firewalld-cmd --add-port 1234/tcp`
* `firewalld-cmd --get-active-zones`

# 11.3 Control SElinux Port Labeling #
`semanage port -l` show context for ports
`semanage port -m -t ssh_port_t -p 23` this command modifies the context ssh_port_t to have a new port 23, the `-m` option means modifiy.
`semanage port -l -C` to show local or custom modifications