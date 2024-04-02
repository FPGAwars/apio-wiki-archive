[![](https://github.com/FPGAwars/Apio-wiki/raw/main/wiki/Logos/apio-banner.svg)](https://github.com/FPGAwars/apio/wiki)

# Contents
  * [Usage](#usage)  
  * [Description](#description)  
  * [Options](#options)
  * [Examples](#examples)  


# Usage

```bash
apio lint [OPTIONS]
```

# Description

Lint the verilog code. It is agnostic of the FPGA. It does not use the constraints files (`.pcf`,`.lpf`)

> [!WARNING]
> `apio lint` is broken for oss-cas-suite@0.0.9 apio package

# Options

| Flag | Long Flag    | Description |
| ---- | ------------ | ----------- |
| `-a` | `--all`      | Enable all warnings, including code style warnings |  
| `-t` | `--top`      | Set top module |
|      | ` --nowarn`  | Disable all style warnings |
|      | `--warn`     | Enable specific warning(s) |
| `-p` | `--project-dir` | Set the target directory for the project |  

# Examples

## 1. Lint the ledon example

```bash
apio lint
```

![](https://github.com/FPGAwars/Apio-wiki/blob/main/wiki/Apio-commands/apio-lint-01.png)  

-------
[![](https://github.com/FPGAwars/icestudio-wiki/raw/main/Logos/fgpawars-banner.svg)](https://fpgawars.github.io/)
