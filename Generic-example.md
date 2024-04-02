[![](https://github.com/FPGAwars/Apio-wiki/raw/main/wiki/Logos/apio-banner.svg)](https://github.com/FPGAwars/apio/wiki)

# Contents

* [Generic exaple]()
 

# Generic example

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


Simulate
~~~~~~~~

Simulate your test bench using `Icarus Verilog <http://iverilog.icarus.com/>`_ and `GTKWave <http://gtkwave.sourceforge.net/>`_

.. code::

  $ apio sim

.. image:: ../resources/images/gtkwave-simulation.png

.. note::

  GTKWave must be installed.

  +---------+-------------------------+
  | Debian  | apt-get install gtkwave |
  +---------+-------------------------+
  | Mac OSX | brew install gtkwave    |
  +---------+-------------------------+
  | Windows | apio install gtkwave    |
  +---------+-------------------------+

Build
~~~~~~

Syntesize your project using `Icestorm Tools <http://www.clifford.at/icestorm/>`_

.. code::

  $ apio build


Upload
~~~~~~

Connect your FPGA board and upload the bitstream using `Icestorm Tools <http://www.clifford.at/icestorm/>`_

.. code::

  $ apio upload


All the leds should turn on after 3 seconds

.. image:: ../resources/images/apio-icestorm-hello-world.png

**Congrats! Now You have your fully open source FPGA toolchain ready!**



-------
[![](https://github.com/FPGAwars/icestudio-wiki/raw/main/Logos/fgpawars-banner.svg)](https://fpgawars.github.io/)
