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
now sudo apt update
