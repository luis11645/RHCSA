# Manage Networking #

## 11.3 Validate network configuration  ##

* to display network statistics we can use `ip -s link ` command

## 11.5 Configure networking from command Line ##

* A single device can have multiple connections but only one connections can be active peer device
* NetworkManager store network profiles in `/etc/NetworkManager/system-connections/`
* `nmcli con show --active` show all active connections
* `nmcli con add con-name eno3 type ethernet ifname eno3 ipv4.method manual ipv4.addresses 192.168.0.5/24 ipv4.gateway 192.168.0.254` creates a connection named eno3 with the interface eno3 and assign the i4 address and gateway.
* If a device have the autoconnect parameter if we execute `nmcli con down` command it will be reactivated automatically we have to use `nmcli dev disconnect` command to avoid this behavior
* `nmcli con modify` modify our connections options for example `nmcli con mod <connection-name> ipv4.address 192.168.1.4/24`
* We can have multiple IPs in a connection we can add another IP using the command `nmcli con mod ipv4.address +192.168.1.5/25` for example