[![](https://github.com/FPGAwars/Apio-wiki/raw/main/wiki/Logos/apio-banner.svg)](https://github.com/FPGAwars/apio/wiki)

# Contents
  * [Usage](#usage)  
  * [Description](#description)  
  * [Options](#options)
  * [Examples](#examples)  


# Usage

```bash
apio upload [OPTIONS]
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

## 1. Process the ledon example

Before executing the command, these are the files in the current directory:

```
$ ls
apio.ini  info  ledon_tb.gtkw  ledon_tb.v  ledon.v  pinout.pcf
```

Build the project:

```bash
apio build
```

It is built for the board specified in the `apio.ini` file:

![](https://github.com/FPGAwars/Apio-wiki/blob/main/wiki/Apio-commands/apio-build-01.png)  

These are the new files created. The `hardware.bin` file contains the **bitstream**

```
$ ls
apio.ini      hardware.bin   info           ledon_tb.v  pinout.pcf
hardware.asc  hardware.json  ledon_tb.gtkw  ledon.v
```

## 2. Build ledon for the icestick board

```bash
apio build -b icestick
```

Even though the project is for the Alhambra-ii boad, the parameters have highest priority than the `apio.ini` file. Therefore, this file is ignored and the bitstream for icestick board is generated instead

![](https://github.com/FPGAwars/Apio-wiki/blob/main/wiki/Apio-commands/apio-build-02.png)  


-------
[![](https://github.com/FPGAwars/icestudio-wiki/raw/main/Logos/fgpawars-banner.svg)](https://fpgawars.github.io/)
