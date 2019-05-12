

Setup Red Hat Enterprise Linux 8.
---------------------------------


	sudo bash
	subscription-manager remove --all
	subscription-manager list --consumed
	subscription-manager register --auto-attach
	yum repolist
	exit
	sudo yum -y update
	reboot


	sudo yum -y module install python27
	sudo alternatives --set python /usr/bin/python2
	sudo yum -y install mc




Install NVIDIA Graphics Card
----------------------------

	sudo bash
	yum -y groupinstall "Development Tools"
	sudo yum -y install gcc make kernel-headers kernel-devel acpid libglvnd-glx libglvnd-opengl libglvnd-devel pkgconfig
	yum -y install elfutils-libelf-devel "kernel-devel-uname-r == $(uname -r)"
	grub2-editenv - set "$(grub2-editenv - list | grep kernelopts) nouveau.modeset=0"
	grub2-editenv - list | grep kernelopts
	reboot
	sudo systemctl isolate multi-user.target

### Install the NVIDIA graphic driver.

	reboot


######## Insatll EPEL Repository ########

	sudo yum repolist
	sudo yum -y install https://dl.fedoraproject.org/pub/epel/epel-release-latest-7.noarch.rpm
	sudo yum repolist


######## Insatll RPM Fusion Repository ########

	sudo yum localinstall --nogpgcheck https://download1.rpmfusion.org/free/el/rpmfusion-free-release-7.noarch.rpm https://download1.rpmfusion.org/nonfree/el/rpmfusion-nonfree-release-7.noarch.rpm
	sudo yum repolist



	sudo yum -y install gnome-tweaks.noarch
	sudo yum -y install ntfs-3g
	sudo yum -y install lm_sensors
	sudo yum -y install libnsl
	# sudo yum -y install qt5-qtx11extras qt5-qtquickcontrols qt5-qtwebchannel qt5-qtwebchannel-devel 



	sudo yum -y install gimp




###### Autodesk Maya 2018.5 Install ######

	sudo yum -y install xorg-x11-fonts-ISO8859-1-100dpi xorg-x11-fonts-ISO8859-1-75dpi xorg-x11-fonts-100dpi xorg-x11-fonts-75dpi
	sudo yum -y install mesa-libGLw libXp libXp-devel gamin e2fsprogs-libs tcsh
	sudo yum -y install compat-openssl10.x86_64 libpng12


Houdini
-------

	sudo yum -y install libnsl








