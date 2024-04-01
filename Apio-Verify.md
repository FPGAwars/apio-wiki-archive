[![](https://github.com/FPGAwars/Apio-wiki/raw/main/wiki/Logos/apio-banner.svg)](https://github.com/FPGAwars/apio/wiki)

# Contents
  * [Usage](#usage)  
  * [Description](#description)  
  * [Options](#options)
  * [Examples](#examples)  


# Usage

```bash
apio verify [OPTIONS]
```

# Description

**Upload** the bitstream to the FPGA. It **builds** the project if required

It also performs an **automatic discovery** and validation of the FTDI chip depending on the selected board.

Required package: `oss-cad-suite`

# Options

| Flag | Long Flag        | Description |
| ---- | ---------------- | ----------- |
| `-b` | `--board`        | Select a specific board |
|      | `--serial-port`  | Select a specific serial port. You can check the available serial devices with the command `apio system --lsserial` |
|      | ` --ftdi-id` | Select a specific FTDI index. You can check the available FTDI indexes with the command `apio system --lsftdi` |
| `-s` | `--sram`     | Perform SRAM programming. Only available for iceprog compatible boards |  
| `-f` | `--flash`    | Perform FLASH programming |
| `-p` | `--project-dir` | Set the target directory for the project. |  
| `-v` | `--verbose`  | Show the entire output of the command |  
|      | `--verbose-yosys` | Show the yosys output of the command |
|      | `--verbose-pnr` | Show the pnr output of the command |  
|      | `--top-module str` | Set the top level module (w/o .v ending) for build |  

> [!NOTE]
> All available boards, FPGAs, sizes, types and packs are showed in [apio boards](Apio-Boards)


# Examples

## 1. Upload the ledon example

```bash
apio upload
```

![](https://github.com/FPGAwars/Apio-wiki/blob/main/wiki/Apio-commands/apio-upload-01.png)  


-------
[![](https://github.com/FPGAwars/icestudio-wiki/raw/main/Logos/fgpawars-banner.svg)](https://fpgawars.github.io/)
