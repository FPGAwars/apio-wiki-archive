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

```bash
apio build
```


-------
[![](https://github.com/FPGAwars/icestudio-wiki/raw/main/Logos/fgpawars-banner.svg)](https://fpgawars.github.io/)
