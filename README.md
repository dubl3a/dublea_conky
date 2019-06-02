
# u/dublea's Conky Config

![Screenshot](https://github.com/dubl3a/dublea_conky/blob/master/Screenshot%20.png)

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

Place contents into `~/config/.conky`

### To-Do

1. Replace OS logo with ASCII logo pulled through `exec` objects -- In Progress
2. Replace NVIDIA logo with GPU object\icon\font
3. Add `if_up - endif ` objects for existing network to hide when not connected
4. Add LAN connection to display when hard wired also leveraging `if_up | endif ` objects
5. Add `if_mounted - endif` objects for Network Storage boxes to hide when not at home
6. Auto add Storage box devices and objects