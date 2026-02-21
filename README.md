# TWM-xfce
### An attempt to recreate the desktop in OneShot: World Machine Edition in Xfce.  
The icon pack is based from Pixelitos and RetroPixel.   
Some icons are also provided by @Charpurr (on Twitter).  
xfwm4 theme is made by apprehensions (on GitHub).  
TWM-theme is based on Darkaneon Purple.  

## Also check out these projects!
### Below projects aren't made by me, but might go well (or can be used) with TWM-xfce!
- TWM-GTK4 `https://github.com/ViviNoSmol/TWM-GTK4`: gtk.css files that provide themes similar to TWM-xfce for GTK4 applications.
- OneShot-WME-Plasma6Theme `https://github.com/capYT-real/OneShot-WME-Plasma6Theme`: Oneshot WME desktop theme for KDE. Most components from TWM-xfce (except TWM-theme) can be used alongside this project as well!

# Instruction:  
### Make sure to change your desktop environment to Xfce.

## TWM-theme: xfwm4 theme
- Move folder into `/usr/share/themes` (`sudo mv TWM-theme /usr/share/themes`)
- Change the theme by going to `Settings Manager - Appearance - Style`, and select `TWM-theme`
- Change the Window Manager theme by going to `Settings Manager - Window Manager`, and select `TWM-theme`
- Change title font to `Volter (Goldfish) Regular 12`; title alignment to `Left`
- Note: Some browsers (mostly Chromium-based one) may have some rendering problems with this theme (or may show wrong window borders). Fix this by enabling System titlebar in said browsers.

<img width="765" height="639" alt="image" src="https://github.com/user-attachments/assets/0da020cb-244f-43fb-b88c-2b8c30cd1543" />

<img width="765" height="639" alt="image" src="https://github.com/user-attachments/assets/ff46a25d-46eb-4172-bba4-902b8883d1cf" />

## TWM-icons: Icons
- Move folder into `/usr/share/icons` (`sudo mv TWM-icons /usr/share/icons`)
- Change the icon by going to `Settings Manager - Appearance - Icons`, and select `TWM`
- Not all icons are replaced. Feel free to request missing icons by creating a new post in Issues.

<img width="765" height="639" alt="image" src="https://github.com/user-attachments/assets/a352f236-831f-4814-bcbc-60b97574a071" />

## TWM-fonts: Fonts
- Move folder into `/usr/share/fonts` (`sudo mv TWM-fonts /usr/share/fonts`)
- Log out/Restart
- Change the fonts in `Settings Manager - Appearance - Fonts`
- Default font should be `Volter (Goldfish) Regular 10`; Monospace font should be `Terminus Medium 12`

<img width="765" height="639" alt="image" src="https://github.com/user-attachments/assets/adc623ef-56d9-482c-953d-cf835c837da4" />

## gtk.css: Panels and Colors
#### Not to be confused with the one inside TWM-theme. This file is placed outside any folder, alongside startup.ogg.
- Go into `~/.config/gtk-3.0` (or create one if doesn't exist `mkdir ~/.config/gtk-3.0`)
- Make sure to backup the original gtk.css inside the folder, if it exists, before replacing it (`cp ~/.config/gtk-3.0/gtk.css ~/.config/gtk-3.0/gtk.bak`)
- Move the file to the folder (`mv gtk.css ~/.config/gtk-3.0`)
- Log out/Restart

<img width="1295" height="535" alt="image" src="https://github.com/user-attachments/assets/067c07cf-da43-4532-acc2-567b8e4dd1e3" />

#### Reconfigure your panel (Settings Manager - Appearance - Panel)
  + Set panel background style to `Solid color` and set the color to Invisible, if possible, or #000000
  + Panel height should be at 36-40; Icon size should be at 24-28

<img width="461" height="561" alt="image" src="https://github.com/user-attachments/assets/f62e1fc5-3009-4abd-a413-ee3345717d32" />

<img width="461" height="561" alt="image" src="https://github.com/user-attachments/assets/2c2d6737-9b5b-4365-9e0c-7e90fa923057" />

#### Reconfigure your panel plugins
  + Clock (not to be confused with DateTime): Layout: `Time Only`; Format: `HH:MM AM/PM` (`%I:%M %p`); Font: `Volter (Goldfish) Regular 11`
  + Whisker Menu: Display: `Icon`; Icon: `oneshot`
  + Window Buttons: Enable `Show button labels` and `Show flat buttons`

<img width="1920" height="41" alt="image" src="https://github.com/user-attachments/assets/2335dd20-4f03-465d-9328-f9b440af2691" />

# Optional
## TWM-cursor: Cursor packs
- Move folder into `/usr/share/icons` (`sudo mv TWM-cursor /usr/share/icons`)
- Go to Settings Manager - Mouse and Touchpad
- On the Themes tab, select TWM-cursor

<img width="632" height="435" alt="image" src="https://github.com/user-attachments/assets/4f5287a2-917c-44cf-933d-658a773ef27d" />

## TWM-Wallpaper: Desktop wallpaper
### SPOILER: If you haven't played OneShot yet, use the TWM.png outside the folder as your wallpaper
- Go to Settings Manager - Desktop
- Click on Folder - Other and browse for the TWM-Wallpapers folder, then click Open
- Change to whatever wallpaper you like
  
<img width="812" height="546" alt="image" src="https://github.com/user-attachments/assets/5e706240-92e0-425f-8a81-9f5a305a8a0f" />

## startup.ogg: Login sound
- Move file into ~/ (or whatever folder you want) (`mv startup.ogg ~/`)
- Go to Settings Manager - Session and Startup - Application Autostart
- Click add, and set the command to `mpv /path/to/startup.ogg`
  + Replace mpv to whatever sound player that you use, or install mpv
  + Replace `/path/to` with the directory of the sound file (ex: `/home/pdn`)
- Set the trigger to on login, then click OK

<img width="441" height="251" alt="image" src="https://github.com/user-attachments/assets/7ca101e4-e369-4dd1-9358-8d422fb6e88d" />

## TWM-Conky | TWM-Conky-sm: Desktop widgets
### Require conky to be installed.
- You should use conky-manager2 to enable and change the position of the widget.
- If your screen is small (<1366x768), use TWM-Conky-sm instead of TWM-Conky.
- TWM-moc-player require mocp, and can only show song played through mocp.
- TWM-weather should automatically detect your location.  
  + In case where it does not (or you want to change the location), edit the file to include your location.  
  + It should be `"https://wttr.in/location?d0ATQ"`, example `"https://wttr.in/California?d0ATQ"`.  
  + For more info: https://wttr.in/:help

<img width="682" height="554" alt="image" src="https://github.com/user-attachments/assets/dab0ef66-c206-4a05-84b5-557191a79b93" />

## TWM-plymouth: Bootup screen
### Require plymouth to be installed and set up correctly. (https://wiki.archlinux.org/title/Plymouth)
- Move folder into `/usr/share/plymouth/themes/` (`sudo mv TWM-plymouth /usr/share/plymouth/themes`)
- Run `sudo plymouth-set-default-theme TWM-plymouth` in console
  + If the above command doesn't exist (or doesn't work), use a text editor and open `/etc/plymouth/plymouthd.conf` to include this line:  
```
[Daemon]
Theme=TWM-plymouth
```
- Regenerate your initramfs
  + For systems using mkinitcpio: `sudo mkinitcpio -P` (https://wiki.archlinux.org/title/Mkinitcpio)
  + For systems using dracut: `sudo dracut-rebuild` or `sudo dracut --regenerate-all --force` (https://wiki.archlinux.org/title/Dracut)
  + Note: Some distributions may have different ways to regenerate your initramfs. For such systems, you may need to google for the command.

<img width="1920" height="1080" alt="img" src="https://github.com/user-attachments/assets/38cfde27-56fa-49f0-aef1-84830435f197" />

## TWM-GRUB: Bootloader theme
### Require GRUB to be used as your bootloader
- Move folder into `/boot/grub/themes` (`sudo mv TWM-GRUB /boot/grub/themes`)
- Use a text editor and open `/etc/default/grub`
- Add/replace `GRUB_THEME=` with this line: `GRUB_THEME="/boot/grub/themes/TWM-GRUB/theme.txt"`, then save the config
- Rebuild GRUB configuration.
  + For Debian/Ubuntu based distro: `sudo update-grub`
  + For Fedora/Arch and other distro: `grub-mkconfig -o /boot/grub/grub.cfg`
  + Some distro may have different ways to rebuild GRUB configuration. For such system, you may need to consult to your distro's wiki or search for the command.
- Work best with 1920x1080+ display.

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/b6ccf291-f691-4979-ba92-d8e6fcaab4cb" />

# Preview:

<img width="1366" height="768" alt="Screenshot_2025-11-11_22-19-33" src="https://github.com/user-attachments/assets/a0e69b50-dbd5-4de8-8295-1932b69ca7d7" />
