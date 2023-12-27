# TWM-xfce
An attempt to recreate the desktop in OneShot: World Machine Edition in XFCE.  
The icon pack is based from Pixelitos and RetroPixel.  
Some icons are also provided by @Charpurr (on Twitter).  
xfwm4 theme is made by apprehensions (on GitHub).

# Instruction:  
* Make sure to change your desktop environment to Xfce.
* Work best in EndeavourOS as it has some patch to fix the panel border issue

## TWM-fonts: Fonts
- Put into /usr/share/fonts
- Log out/Restart
- Change the fonts in Settings Manager - Appearance - Fonts
- Default font should be Terminus Medium; Monospace font should be Terminus Bold
- I recommend setting the font size to either 11 or 13
![Fonts](https://github.com/pdn6606/TWM-xfce/assets/31226956/38292757-d508-4844-b7db-c4b3895c6782)

## gtk.css: Panels and Colors
- Go into ~/.config/gtk-3.0
- Make sure to backup the original gtk.css inside the folder, if it exists, before replacing it
- Put the file to the folder
- Log out/Restart
- Reconfigure plugins in your panel, for example the clock might have incorrect fonts and size  
If you are not using EndeavourOS, the panel's border may overlap with some plugins.
![gtk](https://github.com/pdn6606/TWM-xfce/assets/31226956/8e88be4f-9323-46ef-bfa9-990fca17559f)

## TWM-icons: Icons
- Put into /usr/share/icons
- Change the icon by going to Settings Manager - Appearance - Icons, and select TWM
- Not all icons are replaced.
![Icons](https://github.com/pdn6606/TWM-xfce/assets/31226956/adc1f8ed-210e-443d-b2ed-896fb84e4124)

## TWM-theme: xfwm4 theme
- Put into /usr/share/themes
- Change the theme by going to Settings Manager - Appearance - Style, and select TWM-theme
- Change the Window Manager theme by going to Settings Manager - Window Manager, and select TWM-theme
- Change title font to Terminus Bold, recommended size 15
- Change title alignment to Left
![Theme](https://github.com/pdn6606/TWM-xfce/assets/31226956/46b1a06a-1d3b-44ac-93cf-951f1c280ea5)
![Window Manager](https://github.com/pdn6606/TWM-xfce/assets/31226956/e0063775-1407-4f62-95aa-fe12b60c145d)


# Optional
## TWM-Wallpaper: Desktop wallpaper
- Spoiler alert, if you didn't play OneShot yet, just use the TWM.png outside the folder
- Go to Settings Manager - Desktop
- Click on Folder - Other and browse for the TWM-Wallpapers folder, then click Open
- Change to whatever wallpaper you like
![Wallpaper](https://github.com/pdn6606/TWM-xfce/assets/31226956/4db729b6-b649-40c3-8e05-daff0352f35c)

## startup.ogg: Login sound
- Put into ~/Music (or whatever folder you want)
- Go to Settings Manager - Session and Startup - Application Autostart
- Click add, and set the command to `mpv ~/Music/startup.ogg`  
Replace mpv to whatever sound player that you use, or install mpv
- Make sure to set the trigger to on login, then click OK
![Login sound](https://github.com/pdn6606/TWM-xfce/assets/31226956/fad6b27b-0e62-4aad-9847-a32769a91016)

## TWM-conky: Desktop widgets
- Require conky to be installed.
- You should use conky-manager2 to enable and change the position of the widget.
- TWM-moc-player require mocp, and can only show song played through mocp.
![Conky Manager2](https://github.com/pdn6606/TWM-xfce/assets/31226956/caf3dacf-1834-4a0c-82e1-8dca80e49ebd)

## TWM-plymouth: Bootup screen
- Require plymouth to be installed.
- Put into /usr/share/plymouth/themes/
- Run `sudo plymouth-set-default-theme -R TWM-plymouth` in console
- If plymouth-set-default-theme is not found, use a text editor and open /etc/plymouth/plymouthd.conf to include this line:  
```
[Daemon]
Theme=TWM-plymouth
```


## TWM-grub: Bootloader theme
* Warning: This can lead to an unbootable system if you don't know what you are doing.
- Require GRUB to be used as your bootloader
- Put into /boot/grub/themes
- Use a text editor and open `/etc/default/grub`
- Add or replace `GRUB_THEME=` to this line: `GRUB_THEME="/boot/grub/themes/TWM/theme.txt"`

# Preview:
![The desktop, with all of the above done, in EndeavourOS XFCE](https://github.com/pdn6606/TWM-xfce/assets/31226956/e9421ee1-ce0a-4158-865d-b4c87642d738)

