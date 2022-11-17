# Ubuntu development environment

The best way is to check the official documentation


## Install Anaconda

https://anaconda.cloud/support-center/installers

1.apt-get install libgl1-mesa-glx libegl1-mesa libxrandr2 libxrandr2 libxss1 libxcursor1 libxcomposite1 libasound2 libxi6 libxtst6

2.bash ~/Downloads/Anaconda3-2020.02-Linux-x86_64.sh



## Install VSCode

1.https://code.visualstudio.com/docs

wget -qO- https://packages.microsoft.com/keys/microsoft.asc | gpg --dearmor > packages.microsoft.gpg

sudo install -o root -g root -m 644 packages.microsoft.gpg /etc/apt/trusted.gpg.d/

sudo sh -c 'echo "deb [arch=amd64,arm64,armhf signed-by=/etc/apt/trusted.gpg.d/packages.microsoft.gpg] https://packages.microsoft.com/repos/code stable main" > /etc/apt/sources.list.d/vscode.list'

rm -f packages.microsoft.gpg

sudo apt install apt-transport-https

sudo apt update

sudo apt install code # or code-insiders


## Install Java git gcc

1.$javac

2.$sudo apt install openjdk-17-jdk-headless

## Install IDE

1.sudo snap install pycharm-community --classic

2.sudo snap install intellij-idea-community --classic


## Install Virtual Box

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


## Setting linux in VirtualBox

1.Virtualbox setting, new NatNetwork 10.0.2.0/24 and Supports DHCP

2.VirtalLinux NatNetwork

3.Restart VirtualMachine

4.sudo vi /etc/sysconfig/network-scripts/ifcfg-enp0s3

BOOTPROTO=static
ONBOOT=yes

IPADDR=10.0.2.6
GATEWAY=10.0.2.1
NETMASK=255.255.255.0
DNS1=10.0.2.1

save

5. service network restart


## Mac SSH VirtuanBox

1. VirtualBox  setting-adapter-advanced-Port Forwarding

rule1-tcp-2222(port)-10.0.2.15-22

2. ssh -p 2222 username@127.0.0.1

ssh_exchange_identification: read: Connection reset by peer??

vi /etc/hosts.allow
sshd: ALL

check sshd in terminal

sudo apt install openssh-server

3. systemctl restart sshd

4. restart linux

5. ssh -p 2222 username@127.0.0.1

