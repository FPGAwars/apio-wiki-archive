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
| `-t` | `--top-module` | Set the top_module in the init file |
| `-p` | `--project-dir` | Set the target directory for the project |
| `-y` | `--sayyes`  | Automatically answer YES to all the questions |


# Examples

## 1. Create an apio.ini file for the Alhambra II board

```bash
apio init --board alhambra-ii
```

![](https://github.com/FPGAwars/Apio-wiki/blob/main/wiki/Apio-commands/apio-init-01.png) 

The default name for the **top module** is `main`
This is the content of the `apio.ini` file created:

```ini
[env]
board = alhambra-ii
top-module = main
```

## 2. Create an apio.ini file for the icebreaker board and the top module leds

```bash
apio init -b iCEBreaker --top-module leds
```

![](https://github.com/FPGAwars/Apio-wiki/blob/main/wiki/Apio-commands/apio-init-02.png)  

This is the content of the `apio.ini` file created:

```ini
[env]
board = iCEBreaker
top-module = leds
```

## 3. Create an SConstruct file

```bash
apio init --scons
```

![](https://github.com/FPGAwars/Apio-wiki/blob/main/wiki/Apio-commands/apio-drivers-03.png)  

This commands is used by developers for testing new SConstruct files, or by the users who wants to edit/modify the default SConstruct file



-------
[![](https://github.com/FPGAwars/icestudio-wiki/raw/main/Logos/fgpawars-banner.svg)](https://fpgawars.github.io/)
