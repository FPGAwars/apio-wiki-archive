Examples on how to go **from scratch** to the **Blinky LED** on different **FPGA boards** in a few minutes!

# Index
  * [Ubuntu 20.04](#ubuntu-2004)
    * [Apio installation](#apio-installation)
    * [Testing the Alhambra II board](#testing-the-alhambra-ii-board)  
    * [Testing the NandLand Go board](#testing-the-nandland-go-board)  
    * [Testing the TinyFPGA-BX board](#testing-the-tinyfpga-bx-board)  
    * [Testing the IceBreaker board](#testing-the-icebreaker-board)  
  * [Window 10](#windows-10)  
    * [Apio installation](#apio-installation-1)  
    * [Testing the Alhambra-II board](#testing-the-alhambra-ii-board-1)  
    * [Testing the NandLand Go board](#testing-the-nandland-go-board-1)  
    * [Testing the TinyFPGA-BX board](#testing-the-tinyfpga-bx-board-1)
    * [Testing the IceBreaker board](#testing-the-icebreaker-board-1)
  * [Workflow](#workflow)  

## Ubuntu 20.04

### Apio installation

* Install **python3**:

```
sudo apt install python3
```

* Install **pip3**:

```
sudo apt install python3-pip
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

The LED7 is blinking!!

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

The LED1 is blinking!!

![](https://github.com/FPGAwars/apio/raw/develop/wiki/Quick-start/apio-go-board-01.gif)

### Testing the TinyFPGA-Bx Board

* Enable the **drivers** for this board:

```
apio drivers --serial-enable
```

* Give permission for accessing the serial port. Execute these two commands:

```
sudo usermod -a -G dialout $USER
exec su -l $USER
```

* Install the **tinyprog** programmer. It is a python application that can be installed with pip (an apio package is not necesary)

```
sudo pip3 install tinyprog
```

* **Download** the Blinky example for the **TinyFPGA-BX** board:

```
apio examples -d TinyFPGA-BX/Blinky
```

* Enter the example folder

```
cd TinyFPGA-BX/Blinky/
```
* Make sure the Board is in boot mode: Press the Button. The LED will be flashing

* **Synthesize** and **upload** the bitstream to the board

```
apio upload
```

The LED is blinking!! It is blinking in a different way than previously when it was in the boot mode

![](https://github.com/FPGAwars/apio/raw/develop/wiki/Quick-start/apio-tinyFPGA-01.gif)

### Testing the icebreaker Board

* Enable the **drivers** for this board:

```
apio drivers --ftdi-enable
```

* **Download** the Blinky example for the **IceBreaker** FPGA board:

```
apio examples -d iCEBreaker/Blinky/
```

* Enter the example folder

```
cd iCEBreaker/Blinky/
```

* **Synthesize** and **upload** the bitstream to the board

```
apio upload
```

The LED G (Green) is blinking!!

![](https://github.com/FPGAwars/apio/raw/develop/wiki/Quick-start/apio-icebreaker-01.gif)

## Windows 10

### Apio installation

* Install **python3.6** or **higher** from here: [https://www.python.org/downloads/](https://www.python.org/downloads/). Download the installer, execute it. Check the **Add Python 3.9 to PATH**  checkbox. Click on **Install Now**

![](https://github.com/FPGAwars/apio/raw/develop/wiki/Quick-start/win10-apio-00.png)

* **Open the command prompt** 

![](https://github.com/FPGAwars/apio/raw/develop/wiki/Quick-start/win10-apio-01.png)

All the following commands should be typed in the windows command prompt:

![](https://github.com/FPGAwars/apio/raw/develop/wiki/Quick-start/win10-apio-02.png)

* Install **apio**:

```
pip install apio
```

* Install all the available **apio packages**

```
apio install -a
```

### Testing the Alhambra II board

* Plug the Alhambra-II board to the PC

* Install the drivers for this board:

```
apio drivers --ftdi-enable
```

It will execute the **Zadig driver installation**. Select the **Alhambra-II-(Interface 0)** option on the top and then click on **Replace Driver**

![](https://github.com/FPGAwars/apio/raw/develop/wiki/Quick-start/win10-Alhambra-II-01.png)

When finished close the Zadig Windows

* **Unplug** the Alhambra II board and **Plug** it again

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

![](https://github.com/FPGAwars/apio/raw/develop/wiki/Quick-start/win10-Alhambra-II-02.png)

The LED7 is blinking!!

### Testing the Nandland Go-Board

* Enable the **drivers** for this board:

```
apio drivers --ftdi-enable
```

It will execute the **Zadig driver installation**. Select the **RS232-HS(Interface 0)** option on the top. Select the libusbK driver and then click on **Replace Driver**

![](https://github.com/FPGAwars/apio/raw/develop/wiki/Quick-start/win10-NandLand-go-board-01.png)

When finished close the Zadig Windows

* **Unplug** the NandLand Go-board and **Plug** it again

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

![](https://github.com/FPGAwars/apio/raw/develop/wiki/Quick-start/win10-NandLand-go-board-02.png)

The LED1 is blinking!!

### Testing the TinyFPGA-Bx Board

* Enable the **drivers** for this board:

```
apio drivers --serial-enable
```

It will execute the application for installing the drivers. Once it is done, just click on the **Done** button. It is very likely that the drivers have been already installed by windows when the board was plugged

![](https://github.com/FPGAwars/apio/raw/develop/wiki/Quick-start/win10-TinyFPGA-BX-01.png)

* Install the **tinyprog** programmer. It is a python application that can be installed with pip (an apio package is not necesary)

```
pip install tinyprog
```

* **Download** the Blinky example for the **TinyFPGA-BX** board:

```
apio examples -d TinyFPGA-BX/Blinky
```

* Enter the example folder

```
cd TinyFPGA-BX/Blinky/
```
* Make sure the Board is in boot mode: Press the Button. The LED will be flashing

* **Synthesize** and **upload** the bitstream to the board

```
apio upload
```

![](https://github.com/FPGAwars/apio/raw/develop/wiki/Quick-start/win10-TinyFPGA-BX-02.png)

The LED is blinking!! It is blinking in a different way than previously when it was in the boot mode

### Testing the icebreaker Board

TODO

## TODO

* icesbreaker
* Blackice
* ULX3S-12F
* icestick
* icezum Alhambra
* Lattice HX8k Breakout board
* Lattice UP5K Breakout board
* Operating System: MACos


# Workflow

Once apio is installed, the **workflow** is rather easy:

* Edit the verilog files using your favorite IDE
* Synthesize and upload the bitstream just by executing the command:

```
apio upload
```

