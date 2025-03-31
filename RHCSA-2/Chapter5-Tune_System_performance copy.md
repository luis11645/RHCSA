# Manage SELinux Security #

# 6.1 change SELINUX Enforcement mode#

* `/etc/selinux/config` file is the configutarion file of SELINUX in RHEL

# 6.3 Control SELinux File Contexts #

* `chcon -R -t httpd_sys_content_t /website` change the context of the /website directory to httpd_sys_content_t where the -t represent the new context to add.
* `semanage fcontext -a -t httpd_sys_content_t /website'(/.*)?'` add the httpd_sys_content_t to the selinux database where the "-a" indicates to add in this command.
* `semanage fcontext -l` list the fcontext rules of selinux database.
* `semanage fcontext -l -C` list the local customization of fcontext database

# 6.5 adjust SElinux policiy with Boleans #

* `semanage boolean -l` list all the selinux boleans
* `setsebool -P httpd_use_nfs on` turn on httpd_use_nfs with the "-P" which means persistent
* `semanage boolean -l -C` list local customization of selinux booleans

# 6.7 Investigate and resolve SElinux Issues #

* `sealert -l <alert-id>` to view the alert message and possible solution
* AVC(Access Vector Cache) is the resposible to send selinux violation message
* `ausearch -m AVC` we can use this command to search for selinux messages