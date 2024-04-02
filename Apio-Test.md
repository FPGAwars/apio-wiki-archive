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

Before executing the command, these are the files in the current directory:

```
$ ls
apio.ini  info  ledon_tb.gtkw  ledon_tb.v  ledon.v  pinout.pcf
```

Simulate the project:

```bash
apio test
```

![](https://github.com/FPGAwars/Apio-wiki/blob/main/wiki/Apio-commands/apio-test-01.png)  

These are the new files created:

```
$ ls
apio.ini  ledon_tb.gtkw  ledon_tb.v    ledon.v
info      ledon_tb.out   ledon_tb.vcd  pinout.pcf
```


-------
[![](https://github.com/FPGAwars/icestudio-wiki/raw/main/Logos/fgpawars-banner.svg)](https://fpgawars.github.io/)
