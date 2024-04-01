[![](https://github.com/FPGAwars/Apio-wiki/raw/main/wiki/Logos/apio-banner.svg)](https://github.com/FPGAwars/apio/wiki)

# Contents
  * [Usage](#usage)  
  * [Description](#description)  
  * [Options](#options)
  * [Examples](#examples)  


# Usage

```bash
apio time [OPTIONS]
```

# Description

Bitstream timing analysis: generates a rpt file with a topological timing analysis report, from a verilog and constraints files

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

> [!NOTE]
> All available boards, FPGAs, sizes, types and packs are showed in [apio boards](Apio-Boards)

# Examples

## 1. Timing analysis for the leds example

```bash
apio time
```

![](https://github.com/FPGAwars/Apio-wiki/blob/main/wiki/Apio-commands/apio-time-01.png)  


-------
[![](https://github.com/FPGAwars/icestudio-wiki/raw/main/Logos/fgpawars-banner.svg)](https://fpgawars.github.io/)
