# FPGA FTDI drivers

## Linux
```bash
apio drivers --enable
```

or

```bash
sudo cp 80-icestick.rules /etc/udev/rules.d/
sudo service udev restart
```

## Mac
```bash
apio drivers --enable
```

or

Install libftdi

```bash
brew install libftdi
```

Configure drivers
```bash
sudo kextunload -b com.FTDI.driver.FTDIUSBSerialDriver
sudo kextunload -b com.apple.driver.AppleUSBFTDI
```

To revert the configuration
```bash
sudo kextload -b com.FTDI.driver.FTDIUSBSerialDriver
sudo kextload -b com.apple.driver.AppleUSBFTDI
```

## Windows

https://github.com/FPGAwars/libftdi-cross-builder/wiki#driver-installation
