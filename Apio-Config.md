[![](https://github.com/FPGAwars/Apio-wiki/raw/main/wiki/Logos/apio-banner.svg)](https://github.com/FPGAwars/apio/wiki)

# Contents
  * [Usage](#usage)  
  * [Description](#description)  
  * [Options](#options)
  * [Examples](#examples)  


# Usage

```bash
apio config [OPTIONS]
```

# Description

Apio configuration commands

# Options

| Flag | Long Flag | Description |
| ---- | --------- | ----------- |
| `-l` | `--list`  | List all configuration parameters |
| `-e` | `--exe [default\|native\]` | Configure executables: default selects apio packages, native selects native binaries`
| `-v` | `--verbose [0\|1\]` | Verbose mode: 0 General, 1 Information |


# Examples

## 1. Show all configuration parameters

```bash
apio config --list
```

## 2. Enable native mode for executable binaries

```bash
apio config --exe native
```

## 3. Enable verbose mode 1

```bash
apio config --verbose 1
```

# Profile file

TODO

-------
[![](https://github.com/FPGAwars/icestudio-wiki/raw/main/Logos/fgpawars-banner.svg)](https://fpgawars.github.io/)
