# Apio dependencies

## Linux

### Ubuntu

Install [Python 2.7](https://www.python.org/downloads/) and [pip](https://pip.pypa.io/en/stable/installing/)

Configure [rules file](https://github.com/bqlabs/apio/blob/develop/apio/packages/80-icestick.rules)

```bash
sudo cp 80-icestick.rules /etc/udev/rules.d/
```

```bash
sudo service udev restart
```

## Windows

Install [Python 2.7](https://www.python.org/downloads/)

NOTE: DON’T FORGET to select Add python.exe to Path feature on the “Customize” stage, otherwise Python Package Manager pip command will not be available.

Install FPGA driver:

https://github.com/bqlabs/libftdi-cross-builder/wiki#driver-installation

## Mac

Install [Python 2.7](https://www.python.org/downloads/) and [Homebrew](http://brew.sh/)

Install libftdi0

```bash
brew install libftdi0
```

Configure drivers
```bash
sudo kextunload -b com.FTDI.driver.FTDIUSBSerialDriver
sudo kextunload -b com.apple.driver.AppleUSBFTDI
```



> [Back to installation instructions](https://github.com/bqlabs/apio#install)