# 12.1 REgister Systems for Red Hat Support #

* We can use `rhc connect` command to register a system using the new Red Hat Hybrid Cloud command
* Also we can use `rhc disconnect` to unregister a system

# 12.3 Explain and Investigate RPM software packages #

* We can use `rpm2cpio <package-name> |cpio -idv` to extract the files from rpm package
* Also we can use `rpm2cpio <package-name> |cpio -tv` to see the files from a rpm package

# 12.5 Install And Update Sfpotware Packages with DNF #

* `dnf module info` command show information about module
* `dnf module list` list all the available modules
* `dnf repolist all` command show all available repos
* `dnf config-manager --enable <repo-name>` enable a repo
* `dnf config-manager --disable <repo-name>` disable a repo
* `rpm --import <URL-path>` to import a gpg verification key