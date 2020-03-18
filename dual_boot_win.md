# Dual Booting on Windows

Create a live USB with the Ubuntu version of your choice then install.

[Step by step guide](https://www.tecmint.com/install-ubuntu-alongside-with-windows-dual-boot/
)

## Create Live USB 

#### On linux

use `Ubuntu Startup Disk Creator`
- select .iso
- select usb to create boot image on

#### On Windows

use `Uneetbootin` or `Rufus` like program
- select .iso
- select usb to create boot image on

## Make back up of Windows 
Because you never know

- copy current Windows Key
	
	- cmd `wmic path SoftwareLicensingService get OA3xOriginalProductKey`


- Microsoft Product Key
	- this is now most likely a subscription. Search for Office 2013 key if you have an older version.


- copy all important documents

## Shrink and partition HDD/SSD

- in Start menu search for `disk management`
- shirk current partition


## Shut Down and Reboot into BIOS/UEFI

- Select your USB to boot from
- Follow install steps



## TIPS / Trouble Shoot

On DELL (other SSD) they are natively in RAID mode.  This will make them invisible during the boot process and linux will not find them.  Read [this blog](https://samnicholls.net/2016/01/14/how-to-switch-sata-raid-to-ahci-windows-10-xps-13/) to get an idea.  Beware, it may crash your system. [Stack Exchange Sauce](https://askubuntu.com/questions/952434/dell-xps-15-trying-to-install-ubuntu-16-04-and-not-able-to-get-past-select-part)

[Modify Safe Mode `Win + R` > msconfig](https://techrapidly.com/boot-windows-10-safe-mode-dell/)
Modify Safe Mode cmd > `BCDEDIT /SET {DEFAULT} BOOTMENUPOLICY LEGACY`  disable with `STANDARD`



Try:
- Change SATA Controller to AHCI in BIOS
- Boot Win into Safe mode - F4 (F5 for network option)
- reboot into windows
- shutdown
- do dual boot process