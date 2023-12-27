An attempt to recreate the desktop in OneShot: World Machine Edition in XFCE.
The icon pack is based from Pixelitos and RetroPixel.
Some icons are also provided by @Charpurr (on Twitter/X).
TWM-theme is based from Darkaneon Purple, with some assets from apprehension (on GitHub).

Instructions:
* Make sure to change your desktop environment to Xfce.
* Work best in EndeavourOS as it has some patch to fix the border issue

TWM-fonts:
- Put into /usr/share/fonts
- Log out/Restart
- Change the fonts in Settings Manager - Appearance - Fonts
- Default font should be Terminus Medium; Monospace font should be Terminus Bold
- I recommend setting the font size to either 11 or 13

gtk.css:
- Go into ~/.config/gtk-3.0
- Make sure to backup the original gtk.css inside the folder, if it exists, before replacing it
- Put the file to the folder
- Log out/Restart

TWM-icons:
- Put into /usr/share/icons
- Change the icon by going to Settings Manager - Appearance - Icons, and select TWM
- Not all icons are replaced.

TWM-theme:
- Put into /usr/share/themes
- Change the theme by going to Settings - Window Manager, and select TWM
- Change title font to Terminus Bold, I recommended size 15
- Change title alignment to Left

Optional:
TWM-Wallpaper: (spoiler alert, if you didn't play OneShot yet, just use the TWM.png outside the folder)
- Go to Settings Manager - Desktop
- Click on Folder - Other and browse for the TWM-Wallpapers folder, then click Open
- Change to whatever wallpaper you like

startup.ogg:
- Go to Settings Manager - Session and Startup - Application Autostart
- Click add, and set the command to `mpv /home/pdn/Music/startup.ogg`
+ Replace mpv to whatever sound player that you use, or install mpv
- Make sure to set the trigger to on login, then click OK

TWM-conky:
- Require conky to be installed.
- You should use conky-manager2 to enable and change the position of the widget.
- TWM-moc-player require mocp, and can only show song played through mocp.

TWM-plymouth:
- Require plymouth to be installed.
- Put into /usr/share/plymouth/themes/
- Run `sudo plymouth-set-default-theme -R TWM-plymouth` in console
- If plymouth-set-default-theme is not found, use a text editor and open /etc/plymouth/plymouthd.conf to include this line:
[Daemon]
Theme=TWM-plymouth

TWM-grub:
- Warning: This can lead to an unbootable system if you don't know what you are doing.
- Require GRUB to be used as your bootloader
- Put into /boot/grub/themes
- Use a text editor and open `/etc/default/grub`
- Add or replace `GRUB_THEME=` to this line: `GRUB_THEME="/boot/grub/themes/TWM/theme.txt"`



