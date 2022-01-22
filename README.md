# Ubuntu
development environment

## Install Virtual Box on Ubuntu
Virtual error

Kernel driver not installed (rc=-1908)

Kernel driver not installed (rc=-1908)

The VirtualBox Linux kernel driver (vboxdrv) is either not loaded or there is a permission problem with /dev/vboxdrv. 
Please reinstall virtualbox-dkms package and load the kernel module by executing

'modprobe vboxdrv'
as root.

where: suplibOsInit what: 3 VERR_VM_DRIVER_NOT_INSTALLED (-1908) - The support driver is not installed. On linux, open returned ENOENT.


1.$ sudo apt install virtualbox-dkms
2.$ sudo apt upgrade
