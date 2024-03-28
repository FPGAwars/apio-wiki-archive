[![](https://github.com/FPGAwars/Apio-wiki/raw/main/wiki/Logos/apio-banner.svg)](https://github.com/FPGAwars/apio/wiki)

# Contents
  * [Usage](#usage)  
  * [Description](#description)  
  * [Options](#options)
  * [Packages](#packages)
  * [Examples](#examples)  

# Usage

```bash
apio drivers [OPTIONS]
```

# Description

Enable/Disable the FTDI drivers.

* Linux: add the rules file. It may require a reboot or to uplug and reconnect the board.
* Mac OSX: configure FTDIUSBSerialDriver and AppleUSBFTDI keys and install libftdi.
* Windows: open zadig to replace the current driver by libusbK. It requires to uplug and reconnect the board.

This command requires the ``drivers`` package (only for Windows).

> [!NOTE]
> More information in (`install_drivers`) (TODO)


# Options

| Flag | Long Flag | Description |
| ---- | --------- | ----------- |
| `-a` | `--all`   | Uninstall all packages |
| `-l` | `--list`  | List all installed packages |
| `-p` | `--platform` | Set the platform [linux, linux_x86_64, linux_i686, linux_armv7l, linux_aarch64, windows, windows_amd64, windows_x86, darwin] (Advanced) |

# Packages

| Package | Installation   | Description
|---------|----------------|---------------
| [tools-oss-cad-suite](https://github.com/FPGAwars/tools-oss-cad-suite) | apio install oss-cad-suite| Selected binaries from the [YosysHQ/oss-cad-suite project](https://github.com/YosysHQ/oss-cad-suite-build) 
| [examples](https://github.com/FPGAwars/apio-examples) | apio install examples | Verilog basic examples, pinouts, etc
| [drivers](https://github.com/FPGAwars/tools-drivers) | apio install drivers | Drivers tools (only for Windows)
| [gtkwave](https://github.com/FPGAwars/tool-gtkwave) | apio install gtkwave | Simulation viewer. [GTKWave project](http://gtkwave.sourceforge.net) (only for Windows) 

# Examples

## 1. Uninstall examples package

```bash
apio uninstall examples
```

![](https://github.com/FPGAwars/Apio-wiki/blob/main/wiki/Apio-commands/apio-uninstall-01.png)  

## 2. Uninstall the drivers package for windows in a linux platform

```bash
apio uninstall drivers --platform windows_amd64
```

![](https://github.com/FPGAwars/Apio-wiki/blob/main/wiki/Apio-commands/apio-uninstall-02.png)  

-------
[![](https://github.com/FPGAwars/icestudio-wiki/raw/main/Logos/fgpawars-banner.svg)](https://fpgawars.github.io/)
