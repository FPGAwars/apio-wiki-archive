[![](https://github.com/FPGAwars/Apio-wiki/raw/main/wiki/Logos/apio-banner.svg)](https://github.com/FPGAwars/apio/wiki)

# Contents
  * [Usage](#usage)  
  * [Description](#description)  
  * [Options](#options)
  * [Examples](#examples)  

# Usage

```bash
apio drivers [OPTIONS]
```

# Description

Enable/Disable the FTDI drivers.

* **Linux**: add the rules file. It may require a reboot or to uplug and reconnect the board.
* **Mac OSX**: configure FTDIUSBSerialDriver and AppleUSBFTDI keys and install libftdi.
* **Windows**: open zadig to replace the current driver by libusbK. It requires to uplug and reconnect the board.

This command requires the `drivers` package (only for Windows).

> [!NOTE]
> More information in (`install_drivers`) (TODO)

# Options

| Option            | Description            |
| ----------------- | ---------------------- |
| `--ftdi-enable`   | Enable FPGA drivers    |
| `--ftdi-disable`  | Disable FPGA drivers   |
| `--serial-enable` | Enable Serial drivers  |
| `--serial-disable`| Disable Serial drivers |

# Examples

## 1. Enable the FTDI drivers on Linux

```bash
apio drivers --ftdi-enable
```

![]()  

## 2. Disable the FTDI drivers on Linux

```bash
apio drivers --ftdi-disable
```

![]()  

## 3. Enable the Serial drivers on Linux

```bash
apio drivers --serial-enable
```

![]()  

## 4. Disable the Serial drivers on Linux

```bash
apio drivers --serial-disable
```

![]() 


-------
[![](https://github.com/FPGAwars/icestudio-wiki/raw/main/Logos/fgpawars-banner.svg)](https://fpgawars.github.io/)
