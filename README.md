# i3wmFedora28Config
Configuration file for i3wm using Xfce panel and configs for brightness, sound, etc. 
This is an i3wm configuration (work in progress) I'm using for Fedora 28. Written on a 2016 Dell XPS, this is relevant because it includes the screen brightness, volume controls, etc. configurations. Will be testing on desktop in the future.
Instructions:
- Install Fedora 28 Gnome (base I used)
- Install i3wm (use my Fedora Install Script) or here are the installation apps and code you can run.
       #Install i3wm DE & dasgeek config
				  echo "Installing i3wm & config"
				  dnf -y install i3 i3status dmenu i3lock xbacklight feh conky 
				  #Use XFCE panel instead of default i3 and xfce plugins
				  dnf -y xfwm4.x86_64 xfce4-statusnotifier-plugin.x86_64 xfce4-statusnotifier-plugin.x86_64 xfce4-pulseaudio-plugin.x86_64 xfce4-sensors-plugin.x86_64 xfce4-battery-plugin.x86_64 xfce4-panel.x86 xfce4-whiskermenu-plugin.x86_64 xfce4-clipman-plugin.x86_64 xfce4-session.x86_64
				# Installs compton to prevent screen tearing
				dnf -y install compton.x86_64
				# Backlight controls for laptop work on Dell XPS and other laptops
				dnf -y install light
        
   - Logout of Gnome DE or whatever DE you're using and into the i3 desktop environment (cog wheel at login screen)
   - Do initial setup choosing [Super Key] etc. when prompted by i3 at login
   - Next you will replace your i3 config file with this one. Here is how: 
   - Go to home directory (Ctrl + H) to unhide files
   - Navigate to .config > i3
   - In the i3 folder you will see a config file
   - Rename that file in case you don't like my config you can go back to default
   - Paste my config file in here
   - Press [Super Key] + Shift + R
   - This key combo refreshes your i3 and you should see my config kick off
   - Don't forget to change the wallpaper path in the feh portion of the config to use your own wallpaper
   - Enjoy!
