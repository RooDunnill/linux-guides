Notes on my installation of debian:
I installed this on a flash drive and used another flash drive to install the iso onto
While i wanted to test out two DEs, for some reason either misclick or as default KDE was also installed so had to clear that all away too
Installation Settings:
British keyboard and language
No network
Partitioned with no swap, EXT4 for the main partition mounted at / and then EFI with 512Mb with bootable flag
LXQT for minimalism and cinnamon (Probably added more unnessecary bloat)
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
installed librewolf
remove bloat with sudo apt purge 'bloat'
i removed:
libreoffice* thunderbird* transmission* cheese bresero gnome-themes-extra rhythmbox gnome-games shotwell gnome-disk-utility gnome-logs gnome-screenshot simple-scan sane* cups* printer-driver* sound-juicer orca gnome-keyring synaptic gnome-software kdeconnect smtube smplayer pidgin audacious mpv hexchat remmina qbittorrent meteo-qt screengrab xsane pavucontrol qpdfview kwalletmanager gucharmap xscreensaver gnome-characters gnome-calculator feathernotes gedit gnome-sound-recorder gnote featherpad qlipper xarchiver papirus-icon-theme discover gnome-system-monitor plasma-desktop kwin* kscreen sddm kio* kde* plasma* khelpcenter* 

then clean up with sudo apt clean and sudo apt autoremove
install openbox

