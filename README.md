
# u/dublea's Conky Config

<img src="https://github.com/dubl3a/dublea_conky/blob/master/dublea_conky_screenshot.png" alt="screenshot" width="303" height="1051">

This is a custom config I created for my laptop after I migrated from Windows 10 to Linux Mint 19.1.  I had posted a [screenshot](https://old.reddit.com/r/linuxmint/comments/btuhru/just_finished_up_setting_up_my_desktop_may_add/) of my desktop with my config and a got a few requests to share it.

## NOTICE!

I do not own some of these images.  If there is an issue, I will remove them immediatly, just contact me.  This was intended for my personal use and I am only sharing so others can see how I set it up.  I do have planes to replace them and it will be noted in the To-Do list.

### System Specs this was designed for

* Conky 1.10.8
* OS: Mint 19.1 tessa
* Resolution: 3840x2160
* Screen Size: 15.6"
* DE: Cinnamon 4.0.10
* NVidia GPU
* WLAN Connection

### Fonts Used

* ubuntu
* DejaVu Sans Mono (but any Mono should do)

### Execute Command Dependencies

* sensors for CPU Temps
* nvidia-smi for GPU
* hddtemp
	* This typically has to be ran with sudo.  To run without sudo run the following:
	
	`sudo chmod u+s /usr/sbin/hddtemp`

## Install

Place contents into `~/.config/conky`

Run `conky -c ~/.config/conky/conky.conf` to start it up.

Modify the `conky.conf` file while it is running as it will refresh when you save the file.  This will allow you to modify it and verify it working on your system.

For automatically starting with logging in, create `~/.config/autostart/conky.desktop` filw with the following:

`[Desktop Entry]

Type=Application

Exec=conky -c /home/dublea/.config/conky/conky.conf

Hidden=false

NoDisplay=false

X-GNOME-Autostart-enabled=true

Name=conky

Comment=`

### To-Do

1. Replace OS logo with ASCII logo pulled through `exec` objects -- In Progress
2. Replace Intel icon with CPU object\font
3. Replace NVIDIA icon with GPU object\font
4. Add `if_up - endif ` objects for existing network to hide when not connected
5. Add LAN connection to display when hard wired also leveraging `if_up | endif ` objects
6. Add `if_mounted - endif` objects for Network Storage boxes to hide when not at home
7. Create install.sh
8. Add boxes for USB\Removal Media with `if_mounted - endif` objects
9. Auto add Storage box devices and objects
10. Create Second Config: conky2.conf
	* Calendar
    * Weather
    * To-Do list (linked to Google or other)
    * netstat \ firewall stats
    * Fill with other (quote\joke\image of the day; rss feed; reddit feed)
11. Add AMD Support (would require testers)