# TWM-xfce
### An attempt to recreate the desktop in OneShot: World Machine Edition in XFCE.  
The icon pack is based from Pixelitos and RetroPixel.   
Some icons are also provided by @Charpurr (on Twitter).  
xfwm4 theme is made by apprehensions (on GitHub).  
TWM-theme is based on Darkaneon Purple.  

# Instruction:  
### Make sure to change your desktop environment to Xfce.

## TWM-fonts: Fonts
- Move folder into `/usr/share/fonts`
- Log out/Restart
- Change the fonts in `Settings Manager - Appearance - Fonts`
- Default font should be `Terminus Medium`; Monospace font should be `Terminus Bold`
- Font size should be either 11 or 13    
![Fonts](https://github.com/pdn6606/TWM-xfce/assets/31226956/38292757-d508-4844-b7db-c4b3895c6782)

## gtk.css: Panels and Colors
#### Not to be confused with the one inside TWM-theme. This file is placed outside any folder, alongside startup.ogg.
- Go into `~/.config/gtk-3.0`
- Make sure to backup the original gtk.css inside the folder, if it exists, before replacing it
- Move the file to the folder
- Log out/Restart
#### Reconfigure your panel (Settings Manager - Appearance - Panel)
  + Set panel background style to `Solid color` and set the color to invisible
  + General icon size and Status icon size should be around 16 to 22
#### Reconfigure your panel plugins
  + Clock: Layout: `Time Only`; Format: `HH:MM AM/PM` (`%I:%M %p`); Font: Terminus Medium size 13-16
  + Whisker Menu: Display: `Icon`; Icon: `oneshot`
  + Window Buttons: Enable `Show button labels` and `Show flat buttons`
![gtk](https://github.com/pdn6606/TWM-xfce/assets/31226956/8e88be4f-9323-46ef-bfa9-990fca17559f)

## TWM-icons: Icons
- Move folder into `/usr/share/icons`
- Change the icon by going to `Settings Manager - Appearance - Icons`, and select `TWM`
- Not all icons are replaced.    
![Icons](https://github.com/pdn6606/TWM-xfce/assets/31226956/adc1f8ed-210e-443d-b2ed-896fb84e4124)

## TWM-theme: xfwm4 theme
- Move folder into `/usr/share/themes`
- Change the theme by going to `Settings Manager - Appearance - Style`, and select `TWM-theme`
- Change the Window Manager theme by going to `Settings Manager - Window Manager`, and select `TWM-theme`
- Change title font to `Terminus Bold`, recommended size 15
- Change title alignment to Left
- Known issue: Icons do not show in the title bar of a window    

![Theme](https://github.com/pdn6606/TWM-xfce/assets/31226956/46b1a06a-1d3b-44ac-93cf-951f1c280ea5)
![Window Manager](https://github.com/pdn6606/TWM-xfce/assets/31226956/e0063775-1407-4f62-95aa-fe12b60c145d)


# Optional
## TWM-Wallpaper: Desktop wallpaper
### SPOILER: If you haven't played OneShot yet, use the TWM.png outside the folder as your wallpaper
- Go to Settings Manager - Desktop
- Click on Folder - Other and browse for the TWM-Wallpapers folder, then click Open
- Change to whatever wallpaper you like
  
![Wallpaper](https://github.com/pdn6606/TWM-xfce/assets/31226956/4db729b6-b649-40c3-8e05-daff0352f35c)

## startup.ogg: Login sound
- Move file into ~/Music (or whatever folder you want)
- Go to Settings Manager - Session and Startup - Application Autostart
- Click add, and set the command to `mpv ~/Music/startup.ogg`  
  + Replace mpv to whatever sound player that you use, or install mpv
- Set the trigger to on login, then click OK

![Login sound](https://github.com/pdn6606/TWM-xfce/assets/31226956/fad6b27b-0e62-4aad-9847-a32769a91016)

## TWM-Conky: Desktop widgets
### Require conky to be installed.
- You should use conky-manager2 to enable and change the position of the widget.
- TWM-moc-player require mocp, and can only show song played through mocp.
- TWM-weather should automatically detect your location.  
  + In case where it does not (or you want to change the location), edit the file to include your location.  
  + It should be `"https://wttr.in/location?0ATQ"`, example `"https://wttr.in/California?0ATQ"`.  
  + For more info: https://wttr.in/:help

![Conky Manager2](https://github.com/pdn6606/TWM-xfce/assets/31226956/caf3dacf-1834-4a0c-82e1-8dca80e49ebd)

## TWM-plymouth: Bootup screen
### Require plymouth to be installed and set up correctly. (https://wiki.archlinux.org/title/Plymouth)
- Move folder into `/usr/share/plymouth/themes/`
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

## TWM-GRUB: Bootloader theme
### Require GRUB to be used as your bootloader
- Move folder into `/boot/grub/themes`
- Use a text editor and open `/etc/default/grub`
- Add/replace `GRUB_THEME=` with this line: `GRUB_THEME="/boot/grub/themes/TWM-GRUB/theme.txt"`
- Work best with 1920x1080 display.  

# Preview:
![The desktop, with all of the above done, in EndeavourOS XFCE](https://github.com/pdn6606/TWM-xfce/assets/31226956/e9421ee1-ce0a-4158-865d-b4c87642d738)

