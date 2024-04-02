[![](https://github.com/FPGAwars/Apio-wiki/raw/main/wiki/Logos/apio-banner.svg)](https://github.com/FPGAwars/apio/wiki)

# Contents

* [Introduction](#introduction)
* [Install packages](#install-packages)   
* [Create a project](#create-a-project)  
* [Configure your board](#configure-your-board)  
* [Process the project](#process-the-project)  
  * [Verify](#verify)  

# Introduction

Once apio has been installed and the drivers have been correctly configured is time to start playing with your FPGA!

# Install packages


```bash
$ apio install --all
```

# Create a project

Go to your project's directory or try the examples that comes with apio

```bash
$ apio examples -d Alhambra-II/ledon
$ cd Alhambra-II/ledon
```

# Configure your board

Find your board in the list

```bash
  $ apio boards --list

  Supported boards:
  [...]
```

> [!NOTE] See the [apio boards](https://github.com/FPGAwars/apio/wiki/Apio-Boards) command


Create an `apio.ini` file with your board

```bash
$ apio init --board alhambra-ii
```

# Process the project

## Verify

Check your verilog code using [Icarus Verilog](http://iverilog.icarus.com/)

```bash
$ apio verify
```

## Simulate

Simulate your test bench using [Icarus Verilog](http://iverilog.icarus.com/) and [GTKWave](http://gtkwave.sourceforge.net/>)

```bash
$ apio sim
```
![](https://github.com/FPGAwars/Apio-wiki/raw/main/wiki/Apio-commands/apio-sim-01.png)  

> [!NOTE] GTKWave must be installed. Have a look to the [apio sim](https://github.com/FPGAwars/apio/wiki/Apio-Sim) command

## Build

Syntesize your project using [OSS-CAD-SUITE](https://github.com/YosysHQ/oss-cad-suite-build) Tools

```
$ apio build
```


## Upload

Connect your FPGA board and upload the bitstream using [OSS-CAD-SUITE](https://github.com/YosysHQ/oss-cad-suite-build) Tools

```bash
$ apio upload
```

All the leds should turn on after some seconds

**Congrats! Now You have your fully open source FPGA toolchain ready!**


-------
[![](https://github.com/FPGAwars/icestudio-wiki/raw/main/Logos/fgpawars-banner.svg)](https://fpgawars.github.io/)
