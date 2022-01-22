# Ubuntu development environment

The best way is to check the official documentation


##Install Anaconda

https://anaconda.cloud/support-center/installers

1.apt-get install libgl1-mesa-glx libegl1-mesa libxrandr2 libxrandr2 libxss1 libxcursor1 libxcomposite1 libasound2 libxi6 libxtst6

2.bash ~/Downloads/Anaconda3-2020.02-Linux-x86_64.sh



##Install VsCode

1.https://code.visualstudio.com/docs
wget -qO- https://packages.microsoft.com/keys/microsoft.asc | gpg --dearmor > packages.microsoft.gpg
sudo install -o root -g root -m 644 packages.microsoft.gpg /etc/apt/trusted.gpg.d/
sudo sh -c 'echo "deb [arch=amd64,arm64,armhf signed-by=/etc/apt/trusted.gpg.d/packages.microsoft.gpg] https://packages.microsoft.com/repos/code stable main" > /etc/apt/sources.list.d/vscode.list'
rm -f packages.microsoft.gpg

sudo apt install apt-transport-https
sudo apt update
sudo apt install code # or code-insiders


##Install Java git gcc

1.$javac

2.$sudo apt install openjdk-17-jdk-headless

##Install IDE

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
