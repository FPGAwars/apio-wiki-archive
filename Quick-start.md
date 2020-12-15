Examples on how to go **from scratch** to the **Blinky LED** on different **FPGA boards** in a few minutes!

# Index
  * [Ubuntu 20.04](#ubuntu-2004)
    * [Apio installation](#apio-installation)
    * [Testing the Alhambra II board](#testing-the-alhambra-ii-board)  
    * [Testing the NandLand Go board](#testing-the-nandland-go-board)  
    * [Testing the TinyFPGA-BX board](#testing-the-tinyfpga-bx-board)  
    * [Testing the IceBreaker board](#testing-the-icebreaker-board)  
    * [Testing the Mystorm BlackIce board](#testing-the-mystorm-blackice-board)  
    * [Testing the Radiona ULX3S board](#testing-the-radiona-ulx3s-12f-board) 
    * [Testing the Fomu board](#testing-the-Fomu-board)  
  * [Window 10](#windows-10)  
    * [Apio installation](#apio-installation-1)  
    * [Testing the Alhambra-II board](#testing-the-alhambra-ii-board-1)  
    * [Testing the NandLand Go board](#testing-the-nandland-go-board-1)  
    * [Testing the TinyFPGA-BX board](#testing-the-tinyfpga-bx-board-1)
    * [Testing the IceBreaker board](#testing-the-icebreaker-board-1)  
    * [Testing the mystorm Blackice board](#testing-the-mystorm-blackice-board-1)  
    * [Testing the Radiona ULX3S-12F board](#testing-the-radiona-ulx3s-12f-board-1) 
    * [Testing the Fomu board](#testing-the-fomu-board-1) 
  * [MacOS Catalina (10.15.7)](#macos-catalina-10157)
    * [Apio Installation](https://github.com/FPGAwars/apio/wiki/Quick-start#apio-installation-2)  
    * [Testing the Alhambra-II board](#testing-the-alhambra-ii-board-2)  
  * [Workflow](#workflow)  
  * [Troubleshooting](#troubleshooting)  
    * [Windows 10](#windows-10-1)
      * [Radiona ULX3S board](#radiona-ulx3s-board)  
        * [I get the error cannot find JTAGA cable](#i-get-the-error-cannot-find-jtag-cable)  
  * [Credits](#credits)  

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
sudo pip3 install -U apio
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

* Connect the board to USB port, turn it into bootloader mode, and check whether it is being detected as an USB device with VID:PID equal to 1d50:6130. There are boards that report different identifiers (e.g. 1209:2100). If you have this case with your board, update the bootloader with:

```
tinyprog --update-bootloader
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

### Testing the Mystorm BlackIce board

* Enable the **drivers** for this board:

```
apio drivers --serial-enable
```

* Give permission for accessing the serial port. Execute these two commands:

```
sudo usermod -a -G dialout $USER
exec su -l $USER
```

* Install the **blackiceprog** programmer. It is a python application that can be installed with pip (an apio package is not necesary)

```
sudo pip3 install blackiceprog
```

* **Download** the Blinky example for the **Mystorm Blackice** board:

```
apio examples -d blackice/Blinky
```

* Enter the example folder

```
cd blackice/Blinky/
```

* **Synthesize** and **upload** the bitstream to the board

```
apio upload
```

The blue LED (LED1) is blinking!!

![](https://github.com/FPGAwars/apio/raw/develop/wiki/Quick-start/apio-blackice-01.gif)

### Testing the Radiona ULX3S-12F board

* **Note**: This example is for ULX3S-12F. Nevertheless all these steps can be applied to the other models just by **changing** the **12F sufix** for **85F** or **45F**

* Install the programmer for the ULX3S board:

```
apio install fujprog
```

* Enable the **drivers** for this board:

```
apio drivers --ftdi-enable
```

* **Download** the Blinky example for the **ULX3S-12F** FPGA board:

```
apio examples -d ulx3s-12f/Blinky
```

* Enter the example folder

```
cd ulx3s-12f/Blinky
```

* **Synthesize** and **upload** the bitstream to the board

```
apio upload
```

The LED7 (Blue) is blinking!!

![](https://github.com/FPGAwars/apio/raw/develop/wiki/Quick-start/apio-ulx3-01.gif)

### Testing the Fomu board

* **Install the programmer** for the Fomu board:

```
apio install dfu
```

* Enable the **drivers** for this board:

```
apio drivers --ftdi-enable
```

* **Download** the Blinky example for the **fomu** FPGA board:

```
apio examples -d fomu/Blinky
```

* Enter the example folder

```
cd fomu/Blinky
```

* **Synthesize** and **upload** the bitstream to the board

```
apio upload
```

The RGB LED should be blinking!!

TODO: animated gif with the result

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

* Check that the drivers are ok. Execute this command:

```
apio system --lsserial
```

You should get an output similar to this (the COM8 may vary):

```
Number of Serial devices found: 1

COM14
Description: Dispositivo serie USB (COM14)
Hardware info: USB VID:PID=1D50:6130 SER=7 LOCATION=1-7.1.4
```

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

* Plug the IceBreaker board to the PC

* Install the drivers for this board:

```
apio drivers --ftdi-enable
```

It will execute the **Zadig driver installation**. Select the **icebreaker-(Interface 0)** option on the top and then click on **Replace Driver**

![](https://github.com/FPGAwars/apio/raw/develop/wiki/Quick-start/win10-icebreaker-01.png)

When finished close the Zadig Windows

* **Unplug** the Icebreaker board and **Plug** it again

* **Download** the Blinky example for the **icebreaker** FPGA board:

```
apio examples -d iCEBreaker\Blinky
```

* Enter the example folder

```
cd cd iCEBreaker\Blinky
```

* **Synthesize** and **upload** the bitstream to the board

```
apio upload
```

The LED G (Green) is blinking!!

![](https://github.com/FPGAwars/apio/raw/develop/wiki/Quick-start/win10-icebreaker-02.png)

The LED7 is blinking!!

### Testing the Mystorm BlackIce board

* Enable the **drivers** for this board: Connect the board and execute this command

```
apio drivers --serial-enable
```

It will execute the application for installing the drivers. Once it is done, just click on the **Done** button. It is very likely that the drivers have been already installed by windows when the board was plugged

![](https://github.com/FPGAwars/apio/raw/develop/wiki/Quick-start/win10-TinyFPGA-BX-01.png)

* Check that the drivers are ok. Execute this command:

```
apio system --lsserial
```

You should get an output similar to this (the COM8 may vary):

```
Number of Serial devices found: 1

COM8
Description: Dispositivo serie USB (COM8)
Hardware info: USB VID:PID=0483:5740 SER=00000000001A LOCATION=1-7.1.2
```

* Install the **blackiceprog** programmer

```
pip install -U apio[blackiceprog]
```

* **Download** the Blinky example for the **Mystorm Blackice** board:

```
apio examples -d blackice/Blinky
```

* Enter the example folder

```
cd blackice/Blinky/
```

* **Synthesize** and **upload** the bitstream to the board

```
apio upload
```

The blue LED (LED1) is blinking!!

![](https://github.com/FPGAwars/apio/raw/develop/wiki/Quick-start/win10-Blackice-01.png)

### Testing the Radiona ULX3S-12F board

* **Note**: This example is for ULX3S-12F. Nevertheless all these steps can be applied to the other models just by **changing** the **12F sufix** for **85F** or **45F**

* Install the programmer for the ULX3S board:

```
apio install fujprog
```

* Enable the **drivers** for this board:

```
apio drivers --serial-enable
```
It will execute the application for installing the drivers. Once it is done, just click on the **Done** button. It is very likely that the drivers have been already installed by windows when the board was plugged

![](https://github.com/FPGAwars/apio/raw/develop/wiki/Quick-start/win10-TinyFPGA-BX-01.png)

* Check that the drivers are ok. Execute this command:

```
apio system --lsserial
```

You should get an output similar to this (the COMx number may vary):

```
Number of Serial devices found: 1

COM12
Description: USB Serial Port (COM12)
Hardware info: USB VID:PID=0403:6015 SER=K00102A
```

* **Download** the Blinky example for the **ULX3S-12F** board:

```
apio examples -d ulx3s-12f\blinky
```

* Enter the example folder

```
cd ulx3s-12f\blinky
```

* **Synthesize** and **upload** the bitstream to the board

```
apio upload
```

![](https://github.com/FPGAwars/apio/raw/develop/wiki/Quick-start/win10-ulx3s-12F-02.png)

![](https://github.com/FPGAwars/apio/raw/develop/wiki/Quick-start/win10-ulx3s-12F-03.png)

The blue LED (LED7) is blinking!!

**NOTE**: If you get the error `Cannot find JTAG cable`, please check this [troubleshooting section for ulx3s on Windows 10](https://github.com/FPGAwars/apio/wiki/Quick-start#i-get-the-error-cannot-find-jtag-cable)

### Testing the Fomu board

* **Install the programmer** for the Fomu board:

```
apio install dfu
```

* You do not need to install any driver if you in Windows 10 or later. For checking that the board is detected, plug it and execute this command:

```
apio raw "dfu-util -l"
```

**TODO**: Screenshot with the output when the fomu is connected

* **Download** the Blinky example for the **fomu** FPGA board:

```
apio examples -d fomu/Blinky
```

* Enter the example folder

```
cd fomu/Blinky
```

* **Synthesize** and **upload** the bitstream to the board

```
apio upload
```

The RGB LED should be blinking!!

TODO: animated gif with the result

## MacOS Catalina (10.15.7)

### Apio installation

* Install [homebrew](https://brew.sh/). Just open the macOS Terminal and paste this command:

```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"
```
* **Check** that homebrew has been correctly installed. Type this command:

```
% brew --version
Homebrew 2.5.11
```

* Install **python3**. Execute the following commands:

```
% brew update        
```

and

```
% brew install python
```

* **Check** that you have **python3** and **pip3** installed. Open a terminal and execute the following commands:

```
% python3 --version
Python 3.8.2
```

```
% pip3 --version
pip 19.2.3 from /Library/Developer/CommandLineTools/Library/Frameworks/Python3.framework/Versions/3.8/lib/python3.8/site-packages/pip (python 3.8)
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

## TODO

* fomu
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

## Troubleshooting

### Windows 10

#### Radiona ULX3S board

##### I get the error "Cannot find JTAG cable"

* Error messages: 

```
Cannot find JTAG cable
scons: *** [upload] Error  1
```

* Solution:

If you have been using another FPGA board with apio it is likely that you already **have installed the libusbK drivers**. In order to make ulx3s works in Windows with apio, you should **uninstall** that driver and uses the **standard ftdi drivers** that windows 10 install by default. Follow these steps:

1. Uninstall the libusbK driver. Follow the instructions given on this link: https://github.com/kost/fujprog#change-ulx3s-driver-to-ftdi
2. Unplug the ulx3s board, for 30 seconds
3. Plug it again. Windows 10 will install automatically the standar FTDI driver

## Credits

* Thanks to **Antonio Pascual** for his help on testing apio in MacOS
* Thanks to **Sergio Cuenta** for the Troubleshooting for the ULX3S board
