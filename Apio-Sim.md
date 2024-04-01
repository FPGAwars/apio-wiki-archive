[![](https://github.com/FPGAwars/Apio-wiki/raw/main/wiki/Logos/apio-banner.svg)](https://github.com/FPGAwars/apio/wiki)

# Contents
  * [Usage](#usage)  
  * [Description](#description)  
  * [Options](#options)
  * [Examples](#examples)  


# Usage

```bash
apio sim [OPTIONS]
```

# Description

Launch the verilog simulation using [GTKWave](http://gtkwave.sourceforge.net/) from a verilog test bench

> [!NOTE]
> GTKWave must be installed
> | Platform | Command |
> | -------- | ------- |
> | Debian/Ubuntu | apt install gtkwave  |
> | Mac OSX  | brew install gtkwave |
> | Windows  | apio install gtkwave |

# Options

| Flag | Long Flag    | Description |
| ---- | ------------ | ----------- |
| `-b` | `--board`    | Select a specific board |
|      | `--fpga`     | Select a specific FPGA |
|      | `--size --type --pack`    | Select a specific FPGA size, type and pack |
| `-p` | `--project-dir` | Set the target directory for the project. |  
| `-v` | `--verbose`  | Show the entire output of the command |  
|      | `--verbose-yosys` | Show the yosys output of the command |
|      | `--verbose-pnr` | Show the pnr output of the command |  
|      | `--top-module str` | Set the top level module (w/o .v ending) for build |  


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

![](https://github.com/FPGAwars/Apio-wiki/blob/main/wiki/Apio-commands/apio-sim-01.png)  

-------
[![](https://github.com/FPGAwars/icestudio-wiki/raw/main/Logos/fgpawars-banner.svg)](https://fpgawars.github.io/)
