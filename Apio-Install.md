# Contents
  * [Usage](#usage)  
  * [Description](#description)  
  * [Options](#options)
  * [Packages](#packages)
  * [Examples](#examples)


# Usage

```bash
apio install [OPTIONS] [PACKAGES]
```

# Description

**Install** apio packages. By default it installs the **latest stable version**. Other versions can be installed using the following notation: `package@version`  (Ex. `oss-cad-suite@0.0.8`)  

# Options

| Flag | Long Flag | Description |
| ---- | --------- | ----------- |
| `-a` | `--all`   | Install all packages |
| `-l` | `--list`  | List all available packages |
| `-f` | `--force` | Force the packages installation |
| `-p` | `--platform` | Set the platform [linux, linux_x86_64, linux_i686, linux_armv7l, linux_aarch64, windows, windows_amd64, windows_x86, darwin] (Advanced) |

# Packages

| Package | Installation   | Description
|---------|----------------|---------------
| [tools-oss-cad-suite](https://github.com/FPGAwars/tools-oss-cad-suite) | apio install oss-cad-suite| Selected binaries from the [YosysHQ/oss-cad-suite project](https://github.com/YosysHQ/oss-cad-suite-build) 
| [examples](https://github.com/FPGAwars/apio-examples) | apio install examples | Verilog basic examples, pinouts, etc
| [drivers](https://github.com/FPGAwars/tools-drivers) | apio install drivers | Drivers tools (only for Windows)
| [gtkwave](https://github.com/FPGAwars/tool-gtkwave) | apio install gtkwave | Simulation viewer. [GTKWave project](http://gtkwave.sourceforge.net) (only for Windows) 

# Examples

1. Install `oss-cad-suite` and `examples` packages (latest stable versions):

```bash
apio install oss-cad-suite examples
```
(Screenshot)


