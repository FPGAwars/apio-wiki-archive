[![](https://github.com/FPGAwars/Apio-wiki/raw/main/wiki/Logos/apio-banner.svg)](https://github.com/FPGAwars/apio/wiki)

# Contents
  * [Usage](#usage)  
  * [Description](#description)  
  * [Options](#options)
  * [Examples](#examples)  


# Usage

```bash
apio test [OPTIONS]
```

# Description

Launch the verilog testbench testing. All the testbenches are executed by default (it can be changed by means of the `--testbench` option)


# Options

| Flag | Long Flag    | Description |
| ---- | ------------ | ----------- |
| `-p` | `--project-dir` | Set the target directory for the project. |  
| `-t` | `--testbench`  | Test only this test bench file |  

# Examples

## 1. Test the ledon example

```bash
apio sim
```

![](https://github.com/FPGAwars/Apio-wiki/blob/main/wiki/Apio-commands/apio-sim-02.png)  


![](https://github.com/FPGAwars/Apio-wiki/blob/main/wiki/Apio-commands/apio-sim-01.png)  

-------
[![](https://github.com/FPGAwars/icestudio-wiki/raw/main/Logos/fgpawars-banner.svg)](https://fpgawars.github.io/)
