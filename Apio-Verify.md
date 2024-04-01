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

**Verify** the verilog code. It is agnostic of the FPGA. It does not use the constraint file

Required package: `oss-cad-suite`

# Options

| Flag | Long Flag        | Description |
| ---- | ---------------- | ----------- |
| `-p` | `--project-dir` | Set the target directory for the project. |  


# Examples

## 1. Verify the leds example

```bash
apio verify
```

![](https://github.com/FPGAwars/Apio-wiki/blob/main/wiki/Apio-commands/apio-verify-01.png)    


-------
[![](https://github.com/FPGAwars/icestudio-wiki/raw/main/Logos/fgpawars-banner.svg)](https://fpgawars.github.io/)
