### Installation

NB: the following steps will require SSH access and administrator rights. 
For the latter, either use `sudo` for each command or use `su` to log in as root.

* The kernel modules for each supported platform can be found in `modules/`. 
Copy the required files to your Synology and move them to `/lib/modules`

* To get DSM 7 to load the modules at boot time, copy the included file `start-usb-drivers.sh` to `/usr/local/etc/rc.d`
* Make sure that the file has executable permissions:
  `chmod +x /usr/local/etc/rc.d/start-usb-drivers.sh`

You don't need to reboot your NAS for the modules to load, just execute the script after you completed the previous steps:
```
# /usr/local/etc/rc.d/start-usb-drivers.sh start
```
