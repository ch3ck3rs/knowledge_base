# Dual Booting on Windows

Create a live USB with the Ubuntu version of your choice then install.

## Create Live USB 

#### On linux

use `Ubuntu Startup Disk Creator`
- select .iso
- select usb to create boot image on

#### On Windows

use `Uneetbootin` or `Rufus` like program
- select .iso
- select usb to create boot image on


## Shrink and partition HHD/SSD

- in Start menu search for `disk management`
- shirk current partition
- create `new simple` partition in blank space


## Shut Down and Reboot into BIOS/UEFI

- Select your USB to boot from
- Follow install steps



## TIPS / Trouble Shoot

On DELL (other SSD) they are natively in RAID mode.  This will make them invisible during the boot process and linux will not find them.  Read [this blog](https://samnicholls.net/2016/01/14/how-to-switch-sata-raid-to-ahci-windows-10-xps-13/) to get an idea.  Beware, it may crash your system. [Stack Overflow Sauce](https://askubuntu.com/questions/952434/dell-xps-15-trying-to-install-ubuntu-16-04-and-not-able-to-get-past-select-part)

Try:
- Change SATA Controller to AHCI in BIOS
- Boot Win into Safe mode
- reboot into windows
- shutdown
- do dual boot process