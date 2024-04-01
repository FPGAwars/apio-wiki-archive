[![](https://github.com/FPGAwars/Apio-wiki/raw/main/wiki/Logos/apio-banner.svg)](https://github.com/FPGAwars/apio/wiki)

# Contents
  * [Usage](#usage)  
  * [Description](#description)  
  * [Options](#options)
  * [Project commands](#project-commands)  
  * [Setup commands](#setup-commands)  
  * [Utility commands](#utility-commands)  
  * [Examples](#examples)  


# Usage

```bash
apio [OPTIONS] COMMAND [ARGS]
```

# Description

Apio main command. Execute `apio` to see the help:

```
$ apio
Usage: apio [OPTIONS] COMMAND [ARGS]...

  Work with FPGAs with ease

Options:
  --version   Show the version and exit.
  -h, --help  Show this message and exit.

Project commands:
  build      Synthesize the bitstream.
  clean      Clean the previous generated files.
  graph      Generate a a visual graph of the verilog code.
  lint       Lint the verilog code.
  sim        Launch the verilog simulation.
  test       Launch the verilog testbench testing.
  time       Bitstream timing analysis.
  upload     Upload the bitstream to the FPGA.
  verify     Verify the verilog code.

Setup commands:
  drivers    Manage FPGA boards drivers.
  init       Manage apio projects.
  install    Install apio packages.
  uninstall  Uninstall packages.

Utility commands:
  boards     Manage FPGA boards.
  config     Apio configuration.
  examples   Manage verilog examples.
  raw        Execute commands directly from the Apio packages
  system     System tools.
  upgrade    Check the latest Apio version.
```

# Options

| Option      | Description               | 
| ----------- | ------------------------- |
| `--version` | Show the version of Apio  |


# Project Commands

* [apio build](https://github.com/FPGAwars/apio/wiki/Apio-Build)  
* [apio clean](https://github.com/FPGAwars/apio/wiki/Apio-Clean)  
* [apio sim](https://github.com/FPGAwars/apio/wiki/Apio-Sim)  
* [apio time](https://github.com/FPGAwars/apio/wiki/Apio-Time)  
* [apio upload](https://github.com/FPGAwars/apio/wiki/Apio-Upload)  
* [apio verify](https://github.com/FPGAwars/apio/wiki/Apio-Verify)  
* apio test
* apio graph
* apio lint

# Setup commands

* [apio install](https://github.com/FPGAwars/apio/wiki/Apio-Install)  
* [apio uninstall](https://github.com/FPGAwars/apio/wiki/Apio-Uninstall)  
* [apio drivers](https://github.com/FPGAwars/apio/wiki/Apio-drivers)  
* [apio init](https://github.com/FPGAwars/apio/wiki/Apio-init)  

# Utility Commands

* [apio boards](https://github.com/FPGAwars/apio/wiki/Apio-Boards)  
* [apio config](https://github.com/FPGAwars/apio/wiki/Apio-Config)  
* [apio examples](https://github.com/FPGAwars/apio/wiki/Apio-Examples)  
* [apio raw](https://github.com/FPGAwars/apio/wiki/Apio-Raw)  
* [apio system](https://github.com/FPGAwars/apio/wiki/Apio-System)  
* [apio upgrade](https://github.com/FPGAwars/apio/wiki/Apio-Upgrade)  

# Examples

## 1. Show the apio version

```bash
apio --version
```

```
$ apio --version
apio, version 0.9.2
```

-------
[![](https://github.com/FPGAwars/icestudio-wiki/raw/main/Logos/fgpawars-banner.svg)](https://fpgawars.github.io/)
