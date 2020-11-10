### Windows drivers

https://github.com/FPGAwars/libftdi-cross-builder/wiki#testing-on-windows-7

## Notes

* List of all the apio packages included: apio/apio/resources/packages.json

## Development version

For working with the development version follow these steps:

* Clone the repo (the development branch is the default branch)

```
git clone https://github.com/FPGAwars/apio.git 
```

* Enter the apio folder

```
cd apio
```

* Install the python3-venv package, with the python virtual environment:

```
$ sudo apt install python3-venv
```

* Create a virtual environment called APIO:

```
python3 -m venv APIO
```

* Activate the virtual environomet:

```
$ source APIO/bin/activate
(APIO)$
```

* Install the apio development version, for testing:

```
(APIO)$ pip install -U .
```

* Execute apio and check the version (it is for making sure that the correct devel version was installed):

```
(APIO)$ apio --version
apio, version 0.5.5
```

Everytime you change something in the apio sources and you want to test it you have to "pip install -U ." it 


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

