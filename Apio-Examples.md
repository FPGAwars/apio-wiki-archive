[![](https://github.com/FPGAwars/Apio-wiki/raw/main/wiki/Logos/apio-banner.svg)](https://github.com/FPGAwars/apio/wiki)

# Contents
  * [Usage](#usage)  
  * [Description](#description)  
  * [Options](#options)
  * [Examples](#examples)  


# Usage

```bash
apio examples [OPTIONS]
```

# Description

Manage [verilog examples](https://github.com/FPGAwars/apio-examples): 

This command requires the **examples package**.

# Options

| Flag | Long Flag | Description |
| ---- | --------- | ----------- |
| `-l` | `--list`  | List all available examples |
| `-d` | `--dir`   | Copy the selected example directory |
| `-f` | `--files` | Copy the selected example files |
| `-p` | `--project-dir` | Set the target directory for the examples |  
| -`-n`| `--sayno` | Automatically answer NO to all the questions |


# Examples

## 1. Show all available examples

```bash
apio examples --list
```

![]()  

## 2. Copy the leds example files

```bash
apio examples --files leds
```

![]()  

## 3. Copy the leds example directory

```bash
apio examples --dir leds
```

![]()  



-------
[![](https://github.com/FPGAwars/icestudio-wiki/raw/main/Logos/fgpawars-banner.svg)](https://fpgawars.github.io/)
