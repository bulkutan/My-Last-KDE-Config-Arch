# How to configure your system just like me!!
![Screenshot](https://github.com/bulkutan/My-Last-KDE-Config-Arch/blob/main/2023-11-15_00-59.png)


 For Iconpack; `yay -S gruvbox-plus-icon-theme-git`  

- I use KDE and Openbox at the same time. For this, install Openbox; `sudo pacman -S openbox`
- Look and Feel [Link](https://www.pling.com/p/1327723/) Install From System Settings --> Look and Feel --> Get New Theme 
- Color Schemes Folder; `~/.local/share/color-schemes/`
- Plasma Theme; `~/.local/share/plasma/desktoptheme/`
- Aurorae Theme; `~/.local/share/aurorae/themes/`
- Konsole Color Scheme Folder; `~/.local/share/konsole/`
- BetterDiscord, Kvantum, fish and neofetch Folders; `~/.config/`

Install Spotify from Flatpak; `sudo pacman -S flatpak` -> `flatpak install flathub com.spotify.Client` -> `flatpak run com.spotify.Client`
Install yay, git etc.; `sudo pacman -S --needed base-devel git` -> `git clone https://aur.archlinux.org/yay.git` -> `cd yay` -> `makepkg -si`

## Install NVIDIA

- Firstly, update the system `sudo pacman -Syu`, then install required packages: `sudo pacman -S base-devel linux-lts-headers git --needed` (I use LTS Kernel, install the linux headers package based on your kernel choice.)
- Secondly, install these packages; `yay -S nvidia nvidia-utils lib32-nvidia-utils nvidia-settings` (I currently have Nvidia GTX 1050Ti, find your drivers from this [link](https://nouveau.freedesktop.org/CodeNames.html) and you can check this [link](https://wiki.gentoo.org/wiki/NVIDIA#Feature_support) too.)
  
 ***For GRUB Users***
- `sudo nano /etc/default/grub` find the line starts with **GRUB_CMDLINE_LINUX_DEFAULT=** and update the line to: **GRUB_CMDLINE_LINUX_DEFAULT="loglevel=3 splash nvidia-drm.modeset=1 quiet"**
- Update the GRUB configuration; `sudo grub-mkconfig -o /boot/grub/grub.cfg`

 - `sudo nano /etc/mkinitcpio.conf` Find the line that says **MODULES=()**
 - Update the line to: **MODULES=(nvidia nvidia_modeset nvidia_uvm nvidia_drm)** --> *CTRL+S* --> *CTRL+X* --> `sudo mkinitcpio -P`

NVIDIA Drivers are done!! (nvidia i hate you)

### The Apps Currently I Use;
- Lunar Client; [install from there](https://www.lunarclient.com/download)
- Steam; `sudo pacman -S steam`
- Neovim; `sudo pacman -S neovim`
- Viusal Studio Code; `sudo pacman -S code`
- Heroic Games Launcher; `yay -S heroic-games-launcher`
- ProtonVPN; `sudo pacman -S openvpn`, then follow this [link](https://wiki.archlinux.org/title/ProtonVPN#OpenVPN_setup)
- BleachBit; `sudo pacman -S bleachbit`
- Minecraft Launcher; `sudo pacman -S minecraft-launcher` 
- Obsidian; `sudo pacman -S obsidian`
- OBS Studio; `sudo pacman -S obs-studio`
- Protonup-Qt​; `flatpak install flathub net.davidotek.pupgui2`

#### Wine, Lutris, League of Legends (yikes)
- `sudo pacman -S lutris`
- `sudo pacman -S --needed wine-staging giflib lib32-giflib libpng lib32-libpng libldap lib32-libldap gnutls lib32-gnutls mpg123 lib32-mpg123 openal lib32-openal v4l-utils lib32-v4l-utils libpulse lib32-libpulse libgpg-error lib32-libgpg-error alsa-plugins lib32-alsa-plugins alsa-lib lib32-alsa-lib libjpeg-turbo lib32-libjpeg-turbo sqlite lib32-sqlite libxcomposite lib32-libxcomposite libxinerama lib32-libgcrypt libgcrypt lib32-libxinerama ncurses lib32-ncurses ocl-icd lib32-ocl-icd libxslt lib32-libxslt libva lib32-libva gtk3 lib32-gtk3 gst-plugins-base-libs lib32-gst-plugins-base-libs vulkan-icd-loader lib32-vulkan-icd-loader`
- [Link](https://lutris.net/games/league-of-legends/) for the League of Legends Lutris website.

  #### Openrazer
  - `sudo pacman -S openrazer-daemon`
  - reboot your system
  - `yay -S polychromatic`

    ##### Install Yay
    - `sudo pacman -S --needed base-devel git`
    - `git clone https://aur.archlinux.org/yay.git`
    - `cd yay`
    - `makepkg -si`
