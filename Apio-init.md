[![](https://github.com/FPGAwars/Apio-wiki/raw/main/wiki/Logos/apio-banner.svg)](https://github.com/FPGAwars/apio/wiki)

# Contents
  * [Usage](#usage)  
  * [Description](#description)  
  * [Options](#options)
  * [Examples](#examples)  

# Usage

```bash
apio init [OPTIONS]
```

# Description

Manage apio projects. In addition to the code, an apio project may include a configuration file **apio.ini** and a Scons script **SConstruct**.

# Options

| Flag | Long Flag | Description |
| ---- | --------- | ----------- |
| `-s` | `--scons` | Create a default SConstruct file. This file can be modified and it will be used instead of the default script |
| `-b` | `--board`  | Create a configuration file with the selected board. This will be the default board used by the commands `build`, `upload` and others |
| `-p` | `--project-dir` | Set the target directory for the project |
| `-y` | `--sayyes`  | Automatically answer YES to all the questions |


# Examples

## 1. Enable the FTDI drivers on Linux

```bash
apio drivers --ftdi-enable
```

![](https://github.com/FPGAwars/Apio-wiki/blob/main/wiki/Apio-commands/apio-drivers-01.png)  

## 2. Disable the FTDI drivers on Linux

```bash
apio drivers --ftdi-disable
```

![](https://github.com/FPGAwars/Apio-wiki/blob/main/wiki/Apio-commands/apio-drivers-02.png)  

## 3. Enable the Serial drivers on Linux

```bash
apio drivers --serial-enable
```

![](https://github.com/FPGAwars/Apio-wiki/blob/main/wiki/Apio-commands/apio-drivers-03.png)  

## 4. Disable the Serial drivers on Linux

```bash
apio drivers --serial-disable
```

![](https://github.com/FPGAwars/Apio-wiki/blob/main/wiki/Apio-commands/apio-drivers-04.png) 


-------
[![](https://github.com/FPGAwars/icestudio-wiki/raw/main/Logos/fgpawars-banner.svg)](https://fpgawars.github.io/)
