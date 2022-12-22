# **Customizations of SuaveOS**

## **Document Purpose:**
This document is intended to serve as a method of cataloging all of the changes I have made to the Debian system that serves as the base for SuaveOS. The changes mentioned are what makes SuaveOS unique and different from the Debian system it spawned from.

### **Simple Changes:**
These changes only include installing personally selected software and such, no complex custom configurations or anything.

1. Ranger - file manager.
2. Evolution - Email client.
3. Arc Theme - GTK Theme.
4. Neofetch - looks good.
5. Snapd - installs stuff.

### **Changes With Configuration:**
These changes involved installing hand-picked software and customizing their corresponding configuration files to make the software look and feel the way I like.

1. Spectrwm - Window Manager for custom graphics environment
2. North Icon Theme - custom icon theme
3. Kitty - default terminal for SuaveOS
4. Rofi - window switcher and application launcher.
5. Picom - window compositor.
6. Conky - system monitor.
7. Trayer - system tray.
8. Nitrogen - wallpaper application.
9. Firefox - default browser.
10. Neofetch - shows system info.
11. LightDM - simple login screen and display manager.

### **Corresponding Configuration Data:**
These are the configuration files and data of the software mentioned in 'Changes With Configuration'.

1. Spectrwm - `~/.config/spectrwm/`
2. North Icon Theme - `~/.icons/north-icon-theme/`
3. Kitty - `~/.config/kitty/`
4. Rofi - `~/.config/rofi/`
5. Picom - `~/.config/picom/`
6. Conky - `~/.config/conky/`
7. Trayer - launched by Spectrwm on boot and can be restarted using custom script `trayer-py`.
8. Nitrogen - `~/.config/nitrogen/`
9. Firefox - `/etc/firefox-esr/firefox-esr.js`
10. Neofetch - `~/.config/neofetch/config.conf`
11. LightDM - `/etc/lightdm/*`

### **Custom Configuration Files:**
These are just custom configuration files for software already installed on the base Debian system.

1. `~/.config/gtk-3.0/settings.ini` - GTK theme configuration.
2. `/lib/systemd/system/apparmor.service` - added custom bit to fix "snap-confine has elevated permissions..." issue. Information from [here](https://forums.whonix.org/t/live-mode-breaks-apparmor/7559/12).
3. `~/.xinitrc` - configuration for "startx" command for Xorg.
4. `.bashrc` - configured an alias for Neofetch. Now the command **"neofetch"** shows a custom logo and computer information.
5. `.bashrc` - configured an alias for "alsamixer". Now, just type in the command **"volume"** and the alsamixer volume control TUI will show.

### **Custom Scripts:**
A handful of custom scripts I programmed to assist with controlling various aspects of SuaveOS. All of these are stored in `/usr/bin` and can be launched simply by typing `sudo <custom script>` or just typing `<custom script>` in the command line.

1. `auto-persistence` - automates the process of setting up persistence for a live instance of SuaveOS.
2. `ss-py` - Python 3 script to control the Shadowsocks-Libenv proxy. 
3. `pyrandr` - xrandr Python 3 frontend that helps with adjusting monitor brightness.
4. `trayer-py` - starts and kills trayer (systray) process with Python frontend.

### **Complex Changes:**
These changes cannot be modified easily.

1. `grub-pc` - bootloader is configured and set during the build process with *live-build*, only customization is the grub boot menu background image (now a custom logo designed by me).

Document Started On 2022/2/18
