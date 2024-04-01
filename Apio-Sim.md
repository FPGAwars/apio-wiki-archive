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
| `-p` | `--project-dir` | Set the target directory for the project. |  
| `-t` | `--testbench`  | Specify the testbench file to simulate |  

# Examples

## 1. Simulate the leds example

```bash
apio sim
```

![](https://github.com/FPGAwars/Apio-wiki/blob/main/wiki/Apio-commands/apio-sim-02.png)  


![](https://github.com/FPGAwars/Apio-wiki/blob/main/wiki/Apio-commands/apio-sim-01.png)  

-------
[![](https://github.com/FPGAwars/icestudio-wiki/raw/main/Logos/fgpawars-banner.svg)](https://fpgawars.github.io/)
