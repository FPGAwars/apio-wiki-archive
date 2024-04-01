[![](https://github.com/FPGAwars/Apio-wiki/raw/main/wiki/Logos/apio-banner.svg)](https://github.com/FPGAwars/apio/wiki)

# Contents
  * [Usage](#usage)  
  * [Description](#description)  
  * [Argument](#argument)
  * [Examples](#examples)  


# Usage

```bash
apio raw '[CMD]'
apio raw "[CMD]"
```

# Description

Execute commands using Apio packages

# Argument

| Argument | Description |
| ---- | ---------- |
| `cmd`| Command to be executed using installed Apio packages |



# Examples

## 1. Run yosys to check its version

```bash
apio raw "yosys --version"
```

```
$ apio raw "yosys --version"
Yosys 0.33+103 (git sha1 11ffd7df4, clang 10.0.0-4ubuntu1 -fPIC -Os)
```

## 2. Generate a verilog diagram with yosys

```bash
apio raw 'yosys -p "read_verilog leds.v; show" -q'
```

![]()  


-------
[![](https://github.com/FPGAwars/icestudio-wiki/raw/main/Logos/fgpawars-banner.svg)](https://fpgawars.github.io/)
