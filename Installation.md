[![](https://github.com/FPGAwars/Apio-wiki/raw/main/wiki/Logos/apio-banner.svg)](https://github.com/FPGAwars/apio/wiki)

# Contents
  * [System requirements](#system-requirements)  
  * [Install Apio](#install-apio)  
  * [Install FTDI-DRIVERs](#install-ftdi-drivers)  


**Apio** is written in [Python](https://www.python.org/downloads) and works on Linux (+ARM), Mac OS X and Windows

## System requirements

* **Operating System**: Linux (+ARM), Mac OS X or Windows  
* **Python Interpreter**: Python 3.9 or higher

> [!IMPORTANT]
> **Windows Users**: Please Download the [latest Python](https://www.python.org/downloads/) and install it  
>   **DON'T FORGET** to select `Add python.exe to Path` feature on the "Customize" stage, otherwise Python Package Manager ``pip`` command
      will not be available.
* **Terminal Application**: All commands below should be executed in [Command-line](http://en.wikipedia.org/wiki/Command-line_interface) application (Terminal). 
  * For **Mac OS X** and **Linux OS**:  *Terminal* application,
  * For **Windows OS**:  ``cmd.exe`` application

* **Access to Serial Ports** (USB/UART):
  * **Windows Users**: Please check that you have correctly installed USB driver from board manufacturer.
  * **Linux Users**: Ubuntu/Debian users may need to add own "username" to the "dialout" group if they are not "root", doing this issuing a ``sudo usermod -a -G dialout $USER``.

## Install Apio

The latest stable version of Apio may be installed or upgraded via
Python Package Manager ([pip](https://pip.pypa.io) as follows:

```bash
    $ pip install -U apio
```

Note that you may run into permissions issues running these commands. You have
a few options here:

* Run with ``sudo`` to install Apio and dependencies globally
* Specify the [pip install --user](https://pip.pypa.io/en/stable/user_guide.html#user-installs) option to install local to your user
* Run the command in a [python virtual env](https://docs.python.org/3/library/venv.html) local to a specific project working set


## Install FTDI drivers

For boards with a FTDI interface

```bash
$ apio drivers --ftdi-enable
```

To revert the FTDI drivers configuration.

```bash
$ apio drivers --ftdi-disable
```

## Install Serial drivers


For boards with a **Serial interface**.

```bash
$ apio drivers --serial-enable
```

To revert the Serial drivers configuration.

```bash
  $ apio drivers --serial-disable
```

-------
[![](https://github.com/FPGAwars/icestudio-wiki/raw/main/Logos/fgpawars-banner.svg)](https://fpgawars.github.io/)
