# 12.5 Install and configures virtual machines #

* `virsh` commandline tool allow us to manage KVM virtual machines
* `dnf group install "Virtualization Host"` install the require packages to virtualize
* `virtual-host-validate` command is used to validate if our system is compatible with virtualization
* `virt-install --name demo --memory 4096 --vcpus 2 --disk size=40 --os-type linux --cdrom /root/rhel.iso` deploy a virtual machine
* `dnf install cokpit-machines` enable the virtual machine section on the web console cokpit