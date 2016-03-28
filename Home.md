![](https://github.com/bqlabs/apio/raw/master/doc/apio.jpg)

(_Apio means celery in spanish_ :)

# Apio

Experimental **open source** micro-ecosystem for **open FPGAs**. Based on [platformio](https://github.com/platformio/platformio). It includes [scons](http://scons.org/), pre-built static [toolchain-icestorm](http://www.clifford.at/icestorm/) and icestick rules file auto-installation. Also clean, build, upload commands using scons.

It has been tested on **Ubuntu 14.04**, **15.10**, **Windows 7** and **Mac 10.10**.

## Installation

1. [Install dependencies](https://github.com/bqlabs/apio/wiki/Dependencies)

2. Install latest apio: ```pip install -U apio```

## Quick start

* **Install apio**

* **Install fpga toolchain**:

```bash
apio install
apio install --driver
```

* **Clone the apio github repo**:

```bash
git clone https://github.com/bqlabs/apio.git
```

* **Enter into the examples folder**:

```
cd apio/examples/leds/
```

* **Synthesize the hello world example**

```bash
apio build
```
It generates the **hardware.bin** bitstream

* **Upload the bitstream into the icestick board**

```bash
apio upload
```

All the leds should turn on after 3 seconds:

![](https://github.com/bqlabs/apio/raw/master/doc/apio-icestorm-hello-world.png)

Congrats! Now You have your fully open source FPGA toolchain ready!

## Commands

#### FPGA driver
```bash
apio install --driver
apio uninstall --driver
```

#### FPGA toolchain
```bash
apio install
apio uninstall
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
apio install --system
apio uninstall --system
```

```bash
apio system lsusb
apio system lsftdi
```

#### Debug tools
```bash
apio debug
```

## Authors
* Jesús Arroyo

## License
![](https://github.com/bqlabs/apio/raw/master/doc/bq-logo-cc-sa-small-150px.png)

Licensed under a GPL v2 and [Creative Commons Attribution-ShareAlike 4.0 International License](http://creativecommons.org/licenses/by-sa/4.0/)

## Acknowledgments
### Testers:
* **Javier Martínez**: Tested on Linux mint. ¡Gracias!

    ```
Linux Elvex2 3.16.0-38-generic #52~14.04.1-Ubuntu SMP 
Fri May 8 09:43:57 UTC 2015 x86_64 x86_64 x86_64 GNU/Linux
    ```
* **Julian Caro Linares**: Tested on Ubuntu. ¡Gracias!
* **Rafa Couto**: Debian testing. ¡Gracias!
```(kernel 4.3, pip 1.5.6, python 2.6)```
