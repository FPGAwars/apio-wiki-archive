![](https://github.com/FPGAwars/apio/raw/develop/docs/resources/images/apio.jpg) ![](https://github.com/FPGAwars/apio/raw/develop/docs/resources/images/apio-logo-mini.png) 

(_Apio means celery in spanish_ :)

The full documentation is located in Read the Docs:

> https://apiodoc.readthedocs.io

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

## Testing

It has been tested on

* **Ubuntu 14.04**, **15.10**, **16.04**
* **Windows 7**, **10**
* **Mac 10.9**, **Mac 10.10**
* **Raspberry Pi 2**

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

## Authors
* Jesús Arroyo
* Juan González (Obijuan)

## License
![](https://github.com/FPGAwars/apio/raw/master/doc/bq-logo-cc-sa-small-150px.png)

Licensed under a GPL v2 and [Creative Commons Attribution-ShareAlike 4.0 International License](http://creativecommons.org/licenses/by-sa/4.0/)
