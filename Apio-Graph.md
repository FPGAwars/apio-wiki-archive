[![](https://github.com/FPGAwars/Apio-wiki/raw/main/wiki/Logos/apio-banner.svg)](https://github.com/FPGAwars/apio/wiki)

# Contents
  * [Usage](#usage)  
  * [Description](#description)  
  * [Options](#options)
  * [Examples](#examples)  


# Usage

```bash
apio graph [OPTIONS]
```

# Description

Generate a **visual graph** of the verilog code

# Options

| Flag | Long Flag    | Description |
| ---- | ------------ | ----------- |
| `-v` | `--verbose`  | Show the entire output of the command |  
| `-p` | `--project-dir` | Set the target directory for the project |  
|      | `--top-module` | Set the top level module (w/o .v ending) to graph |  

# Examples

## 1. Graph the ledon example

Before executing the command, these are the files in the current directory:

```
$ ls
apio.ini  info  ledon_tb.gtkw  ledon_tb.v  ledon.v  pinout.pcf
```

Graph the project:

```bash
apio graph
```

![](https://github.com/FPGAwars/Apio-wiki/blob/main/wiki/Apio-commands/apio-graph-01.png)  

These are the new files created. The `hardware.svg` file contains the graph in SVG format

```
$ ls
apio.ini      hardware.svg  ledon_tb.gtkw  ledon.v
hardware.dot  info          ledon_tb.v     pinout.pcf
```

-------
[![](https://github.com/FPGAwars/icestudio-wiki/raw/main/Logos/fgpawars-banner.svg)](https://fpgawars.github.io/)
