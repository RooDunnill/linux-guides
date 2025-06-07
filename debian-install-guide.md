Notes on my installation of debian:
I installed this on a flash drive and used another flash drive to install the iso onto
Installation Settings:
British keyboard and language
No network
Partitioned with no swap, EXT4 for the main partition mounted at / and then EFI with 512Mb with bootable flag
LXQT for minimalism
Did not allow automatic updates
Selected adding grub installation to removeable medium
Did not selectre NVRAM or osprober
Did not allow analytic telemetry
After Installation:
su - followed by usermod -aG sudo username for sudo perms
reboot and access another flash drive for eduroam
installed eduroam by running the program
add mirrors by navigating to /etc/apt/sources.list
edit as such:
comment out cdrom line
add deb http://deb.debian.org/debian bookworm main
add deb http://security.debian.org/debian-security bookworm-security main
add deb http://deb.debian.org/debian bookworm-updates main
now sudo apt update
remove bloat with sudo apt purge 'bloat'
i removed:
libreoffice* thunderbird* transmission* cheese bresero gnome-themes-extra rhythmbox gnome-games shotwell gnome-disk-utility gnome-logs gnome-screenshot simple-scan sane* cups* printer-driver* sound-juicer orca gnome-keyring
then clean up with sudo apt clean and sudo apt autoremove
