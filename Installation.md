# Apio drivers

## Linux
```bash
apio install driver
```

or

```bash
sudo cp 80-icestick.rules /etc/udev/rules.d/
sudo service udev restart
```

## Windows

https://github.com/FPGAwars/libftdi-cross-builder/wiki#driver-installation

## Mac
```bash
apio install driver
```

or

Install libftdi0

```bash
brew install libftdi0
```

Configure drivers
```bash
sudo kextunload -b com.FTDI.driver.FTDIUSBSerialDriver
sudo kextunload -b com.apple.driver.AppleUSBFTDI
```