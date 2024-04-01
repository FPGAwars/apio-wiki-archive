[![](https://github.com/FPGAwars/Apio-wiki/raw/main/wiki/Logos/apio-banner.svg)](https://github.com/FPGAwars/apio/wiki)

# Contents
  * [Usage](#usage)  
  * [Description](#description)  
  * [Options](#options)
  * [Examples](#examples)  


# Usage

```bash
apio build [OPTIONS]
```

# Description

Synthesize the bitstream: generates a `.bin` file from the **verilog sources** and **constaint file**

Required package: `oss-cad-suite`

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

-------
[![](https://github.com/FPGAwars/icestudio-wiki/raw/main/Logos/fgpawars-banner.svg)](https://fpgawars.github.io/)
