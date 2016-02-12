![](https://github.com/bqlabs/apio/raw/master/doc/apio.jpg)

(_Apio means celery in spanish_ :)

# Apio

Experimental **open source** micro-ecosystem for **open FPGAs**. Based on [platformio](https://github.com/platformio/platformio). It includes [scons](http://scons.org/), pre-built static [toolchain-icestorm](http://www.clifford.at/icestorm/) and icestick rules file auto-installation. Also clean, build, upload commands using scons.

## Installation

It has been tested on **Ubuntu 14.04** and **15.10**

```bash
sudo apt-get install libftdi1
sudo pip install apio
```

**Install the icestorm toolchain:**

```
apio install
```

## Quick start

* **Clone the apio github repo**:

```bash
git clone https://github.com/bqlabs/apio.git
```

* **Enter into the examples folder**:

```
cd examples/leds/
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

## Authors
* Jesús Arroyo

## License
![](https://github.com/bqlabs/apio/raw/master/doc/bq-logo-cc-sa-small-150px.png)

Licensed under a GPL v2 and [Creative Commons Attribution-ShareAlike 4.0 International License](http://creativecommons.org/licenses/by-sa/4.0/)

## Acknowledgments
### Testers:
* **Javier Martínez**: Tested on Linux mint

```bash
$ uname -a
Linux Elvex2 3.16.0-38-generic #52~14.04.1-Ubuntu SMP Fri May 8 09:43:57 UTC 2015 x86_64 x86_64 x86_64 GNU/Linux
```

* **Julian Caro Linares**: Tested on Ubuntu