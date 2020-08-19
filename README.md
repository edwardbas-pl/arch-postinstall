# arch-postinstall
This is Arch Linux Post-Install script to use after mninimal install.
For both ``install`` and ``laptop_install`` it behave similarly
This repository include 3 scirpts:
- games - this script install Steam, Wine, etc... (needs multilib repository to be anebled in paacman.conf).
- install - this script is for desktop computers with amd CPU's without wifi.
- laptop install - this scrip was writen in thinkpad t460 in mind.

## execution steps:
- install reflector (for download speed optimization).
- make mirrorlist backup in ``/etc/pacman.d/``
- execute ``sudo reflector --verbose --latest 20 --sort rate --save /etc/pacman.d/mirrorlist`` to rank mirror by speed.
- Install packages from Official Arch repos.
- Clone necessary  repositories (my dmenu build, yay, gimpshop reloaded, dotfiles ackup)
- install vim-plug
- Install AUR Packages
- Make symbolic link betwen ``/run/media/username/`` and ``/home/username/Media/`` for more convinient access to mounted usb drives form Terminal
- Exec mkinitcpio -P
- Enable lightdm and dunst services
- Restore Dotfiles Backup
## Desktop postinstall script contains:
### Official Arch Repository Package list:
- git
- qbittorrent
- xclip
- python-pywal
- i3-gaps
- xorg
- vlc
- gtop
- htop
- vim
- firefox
- spectacle
- libreoffice-fresh
- numlockx
- pulseaudio
- amd-ucode
- galculator
- ntfs-3g
- lightdm
- lightdm-gtk-greeter
- feh
- w3m
- yad
- xdotool
- code
- kitty
- pulseaudio-alsa
- alsa-oss
- nemo
- ranger
- dunst
- xf86-video-amdgpu
- lxappearance
- gimp
- alsa-firmware
### AUR Package List:
- wd719x-firmware
- aic94xx-firmware
- pfetch
- ttf-symbola
- polybar
- compton-tryone-git
- udisks2
- lightdm-slick-greeter
- lightdm-settings
- apulse
- ttf-dejavu
- ttf-liberation
## Laptop postinstall script contains:
### Official Arch Repository Package list:
- git
- xorg
- vlc
- xclip
- python-pywal
- i3lock
- xss-lock
- libreoffice-fresh
- spectacle
- deadbeef
- firefox
- pulseaudio
- galculator
- intel-ucode
- lightdm
- lightdm-gtk-greeter
- feh
- w3m
- yad
- xdotool
- code
- kitty
- nemo
- ranger
- dunst
- xf86-video-intel
- lxappearance
- gimp
### AUR Package List:
- pfetch
- ttf-symbola
- polybar
- compton-tryone-git
- network-manager-applet
- udisks2
- i3-gaps
- wd719x-firmware
- aic94xx-firmware
- lightdm-slick-greeter
- lightdm-settings
- apulse
- ttf-dejavu
- ttf-liberation
