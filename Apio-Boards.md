[![](https://github.com/FPGAwars/Apio-wiki/raw/main/wiki/Logos/apio-banner.svg)](https://github.com/FPGAwars/apio/wiki)

# Contents
  * [Usage](#usage)  
  * [Description](#description)  
  * [Options](#options)
  * [Packages](#packages)
  * [Examples](#examples)  
  * [Folders](#folders)


# Usage

```bash
apio boards [OPTIONS]
```

# Description

Show FPGA boards information

> [!NOTE]
> Check the [Supported-boards] page for a list of all the available boards 

# Options

| Flag | Long Flag | Description |
| ---- | --------- | ----------- |
| `-a` | `--all`   | Install all packages |
| `-l` | `--list`  | List all available packages |
| `-f` | `--force` | Force the packages installation |
| `-p` | `--platform` | Set the platform [linux, linux_x86_64, linux_i686, linux_armv7l, linux_aarch64, windows, windows_amd64, windows_x86, darwin] (Advanced) |

# Packages

| Package | Installation   | Description
|---------|----------------|---------------
| [tools-oss-cad-suite](https://github.com/FPGAwars/tools-oss-cad-suite) | apio install oss-cad-suite| Selected binaries from the [YosysHQ/oss-cad-suite project](https://github.com/YosysHQ/oss-cad-suite-build) 
| [examples](https://github.com/FPGAwars/apio-examples) | apio install examples | Verilog basic examples, pinouts, etc
| [drivers](https://github.com/FPGAwars/tools-drivers) | apio install drivers | Drivers tools (only for Windows)
| [gtkwave](https://github.com/FPGAwars/tool-gtkwave) | apio install gtkwave | Simulation viewer. [GTKWave project](http://gtkwave.sourceforge.net) (only for Windows) 

# Examples

## 1. Install oss-cad-suite and examples packages 

```bash
apio install oss-cad-suite examples
```

The latest stable versions are installed (0.0.9 and 0.0.36 in this example):

![](https://github.com/FPGAwars/Apio-wiki/blob/main/wiki/Apio-commands/apio-install-01.png)  

## 2. Install oss-cad-suite package version 0.0.8

```bash
apio install oss-cad-suite@0.0.8
```
![](https://github.com/FPGAwars/Apio-wiki/blob/main/wiki/Apio-commands/apio-install-02.png)  

## 3. Show all available/installed packages

```bash
$ apio install --list
```
![](https://github.com/FPGAwars/Apio-wiki/blob/main/wiki/Apio-commands/apio-install-03.png)   


## 4. Install and update all packages

```bash
apio install --all
```
The packages are only installed if they are not in the latest version

![](https://github.com/FPGAwars/Apio-wiki/blob/main/wiki/Apio-commands/apio-install-04.png)  

## 5. Install the drivers package for windows in a linux platform

This is usually done by the developers, to test if the correct package is downloaded

```bash
apio install drivers --platform windows_amd64
```

![](https://github.com/FPGAwars/Apio-wiki/blob/main/wiki/Apio-commands/apio-install-05.png)  

# Folders

The **apio home** folder by default is `.apio`, located in the **user home folder**. The full path depends on the operating system and the user who installed apio
* Ex. in Linux: `/home/obijuan/.apio`
* Ex. in Windows: `C:\Users\JANEL\.apio`

The packages are installed in the `packages` folder, inside the **apio home** folder
* Ex. in Linux: `/home/obijuan/.apio/packages`
* Ex. in Windows: `C:\Users\JANEL\.apio\packages`

The **apio home** directory can be changed by means of the **APIO_HOME_DIR** environment variable. For example, icestudio set this env variable to store the packages in a differnt folder (separated from the apio installed on the system)

Once a package is installed, it is added to the `.apio/profile.json` file. Apio reads this file for knowing which packages are present

> [!NOTE]
> You can install manually a package uncompressing it in the package folder, and modifying manually the **profile.json** file


-------
[![](https://github.com/FPGAwars/icestudio-wiki/raw/main/Logos/fgpawars-banner.svg)](https://fpgawars.github.io/)
