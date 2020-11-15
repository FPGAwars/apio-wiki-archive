Example on how to go **from scratch** to the **Blinky LED** on an **FPGA board** in a few minutes!

# Index
  * [Ubuntu 20.04](#ubuntu-2004)
    * [Apio installation](#apio-installation)
    * [Testing the Alhambra II board](#testing-the-alhambra-ii-board)  
    * [Testing the NandLand Go board](#testing-the-nandland-go-board)  
  * [Workflow](#workflow)  

## Ubuntu 20.04

### Apio installation

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
apio examples -d Alhambra-II/Blinky
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

### Testing the Nandland Go-Board

* Enable the **drivers** for this board:

```
apio drivers --ftdi-enable
```

* **Download** the Blinky example for the **NandLand Go-Board** FPGA board:

```
apio examples -d go-board/Blinky
```

* Enter the example folder

```
cd go-board/Blinky/
```

* **Synthesize** and **upload** the bitstream to the board

```
apio upload
```

The LED is blinking!!

![](https://github.com/FPGAwars/apio/raw/develop/wiki/Quick-start/apio-go-board-01.gif)

### Testing the TinyFPGA-Bx Board

TODO

# Workflow

Once apio is installed, the **workflow** is rather easy:

* Edit the verilog files using your favorite IDE
* Synthesize and upload the bitstream just by executing the command:

```
apio upload
```

