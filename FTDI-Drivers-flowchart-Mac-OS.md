### FTDI Drivers scenario
* _iceprog_ requires all the drivers unloaded to detect the board
* FTDIUSBSerialDriver is automatically loaded when the FTDI board is connected for the first time
* AppleUSBFTDI is automatically loaded after unload FTDIUSBSerialDriver and reconnect the board
* After unload AppleUSBFTDI no more drivers are loaded although the board is reconnected
* In order to enable other FTDI devices, the drivers configuration must be restored
* No kext configuration remains after reboot

Therefore, to create a good user experience, the next process must be run on each bitstream upload:

![](https://raw.githubusercontent.com/FPGAwars/apio/develop/docs/resources/images/macos-drivers-flowchart.png)