# 3.1 Analyze and Store Logs #

a `none` value in the priority part indicate that no message have to log in the file for example:

* `*.info;mail.none;authpriv.none;cron.none /var/log/messages`

This indicates that no mail,authpriv and cron messages have to be logged in /var/log/messages file

To send manually a message we can use the command `logger -p local7.notice` where the facility is local7 and priority is notice

# 3.7 Preserve the System Journal #

We can make jouirnal log persisten across reboot editing the file `/etc/systemd/journald.conf` and edit the parameter `Storage`. We can have 4 way to achieve this, setting these settings:

* persistent, if the directory /var/log/journal does not exist the systemd-journald service then creates it
* volatile
* auto
* none

* `systemctl restart systemd-journald`

We can use the command `journalctl | grep -E 'Runtime Journal|System Journal'` to verify how much space the logs are occupying. By default journal only use 10% of the file system for logs storage.

# 3.9 Maintain Accurate Time #

Use ` timedatectl set-ntp false ` to disable ntp synchronization 