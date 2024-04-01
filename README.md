Lenovo Thinkpad X1 Carbon 5th Gen 6300u Intel Graphics 520 macOS Sonoma 14.3.1 EFI Opencore. 20K4, 20K3.

Copy EFI for OpenCore.

Boot to Sonoma 14.3.1. Offline installer. (make take several reboots but will work) (download on mac using gibMacos) (createinstallmedia)

Install. Profit! 

(It is possible to updated to Sonoma 14.4.1 but you have to disable SecureBootModels in config.plist for opencore. Change it from Defaults to Disabled and then back again after the update.)(Sonoma 14.4.1 also needs an updated kext as I have been reading reports online. [
](https://github.com/OpenIntelWireless/itlwm/releases/download/v2.3.0-alpha/AirportItlwm-Sonoma14.4-v2.3.0-DEBUG-alpha-e886ebb.zip) )
