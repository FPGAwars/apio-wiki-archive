Example on how to go **from scratch** to the **Blinky LED** on an **FPGA board** in a few minutes!

## Ubuntu 20.04

### Installation

* Install **python3**:

```
sudo apt install python3
```

* Install **apio**:

```
sudo pip3 install apio
```

* Install all the available **apio packages**

```
apio install -a
```
### Testing the Alhambra II board

* Enable the **drivers** for this board:

```
apio drivers --ftdi-enable
```

* **Download** the Blinky example for the **Alhambra-II** FPGA board:

```
apio examples -d Alhambra-II/Blinky**
```

* Enter the example folder

```
cd Alhambra-II/Blinky
```

* **Synthesize** and **upload** the bitstream to the board

```
apio upload
```

The LED is blinking!!

![](https://github.com/FPGAwars/apio/raw/develop/wiki/Quick-start/apio-alhambra-II-01.gif)

### Workflow

Once apio is installed, the **workflow** is rather easy:

* Edit the verilog files using your favorite IDE
* Synthesize and upload the bitstream just by executing the command:

```
apio upload
```

