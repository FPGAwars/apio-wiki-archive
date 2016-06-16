![](https://github.com/FPGAwars/apio/raw/master/doc/apio.jpg)

(_Apio means celery in spanish_ :)

# Apio

Experimental **open source** micro-ecosystem for **open FPGAs**. Based on [platformio](https://github.com/platformio/platformio). It includes [scons](http://scons.org/), pre-built static [toolchain-icestorm](http://www.clifford.at/icestorm/) and icestick rules file auto-installation. Also clean, build, upload commands using scons.

It has been tested on **Ubuntu 14.04**, **15.10**, **Windows 7**, **Mac 10.10** and **Raspberry Pi 2**.

## Installation

1. [Install dependencies](https://github.com/FPGAwars/apio/wiki/Dependencies) (Python 2.7 and pip)

2. Install latest apio: ```pip install -U apio```

### Installation in Ubuntu 15.10

* Install pip

```
$ sudo apt-get install pip
```
* Install apio

```
$ sudo pip install apio
```


## Quick start

* **Install apio**

* **Install fpga toolchain**:

```bash
apio install
apio install driver
```

* **Get the leds hello world example**:

```bash
apio examples -d leds
```

* **Synthesize it**:

```
cd leds
apio build
```
It generates the **hardware.bin** bitstream


* **Upload the bitstream into the FPGA**

Connect a supported board (icestick, icezum alhambra)

```bash
apio upload
```

All the leds should turn on after 3 seconds:

![](https://github.com/FPGAwars/apio/raw/master/doc/apio-icestorm-hello-world.png)

Congrats! Now You have your fully open source FPGA toolchain ready!

## Commands

#### FPGA driver
```bash
apio install driver
apio uninstall driver
```

#### FPGA toolchain
```bash
apio install
apio uninstall
```

or

```bash
apio install scons
apio install icestorm
apio uninstall scons
apio uninstall icestorm
```

```bash
apio init
apio clean
apio build
apio upload
apio sim
apio time
```

#### System tools
```bash
apio install system
apio uninstall system
```

```bash
apio system lsusb
apio system lsftdi
```

#### Debug tools
```bash
apio debug
```

#### Examples
```bash
apio install examples
apio uninstall examples
```

* Get a list of all the available examples:

```bash
apio examples -l
```

| Example name | Description
|--------------|------------
| go-board     | Generic constraint file for the Nandland go-board
| icestick     | Generic constraint file for the Icestick board
| icezum       | Generic constraint file for the Icezum Alhambra board
| makefile     | Generic makefile file for building using make (legacy)
| leds         | Hello world verilog example: turning on leds (icestick, icezum)
| wire         | Example: how to create a wire in verilog


## Apio packages

| Package  | Installation | Description 
|----------|------------- |---------------
| [Toolchain-icestorm](https://github.com/FPGAwars/toolchain-icestorm/wiki)  | apio install icestorm | Lattice ICE40 FPGA synthesis, place & route and configuration tools. Icestorm project
| [Tools-usb-ftdi](https://github.com/FPGAwars/tools-usb-ftdi/wiki)  | apio install system | Tools for listing the usb devices and retrieving information from the ftdi chips
| [Examples](https://github.com/FPGAwars/apio-examples)  | apio install examples | Verilog basic examples, pinouts, etc.

## Tests

```bash
nosetests
```

```bash
nosetests --with-coverage  --cover-package=apio --cover-html
```


## Authors
* Jesús Arroyo
* Juan González (Obijuan)

## License
![](https://github.com/FPGAwars/apio/raw/master/doc/bq-logo-cc-sa-small-150px.png)

Licensed under a GPL v2 and [Creative Commons Attribution-ShareAlike 4.0 International License](http://creativecommons.org/licenses/by-sa/4.0/)

## Acknowledgments
### Testers:
* **Javier Martínez**: Tested on Linux mint. Thanks!

    ```
Linux Elvex2 3.16.0-38-generic #52~14.04.1-Ubuntu SMP 
Fri May 8 09:43:57 UTC 2015 x86_64 x86_64 x86_64 GNU/Linux
    ```
* **Julian Caro Linares**: Tested on Ubuntu. Thanks!
* **Rafa Couto**: Debian testing. Thanks!
```(kernel 4.3, pip 1.5.6, python 2.6)```
