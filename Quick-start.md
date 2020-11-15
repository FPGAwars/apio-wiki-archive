## Ubuntu 20.04

### Installation

* Install python3:

```
sudo apt install python3
```

* Install apio:

```
sudo pip3 install apio
```

* Install all the available apio packages

```
apio install -a
```

### Driver configuration

* Enable the drivers for the board:

```
apio drivers --ftdi-enable
```

### Testing and example

* Download the Blinky example for the Alhambra-II FPGA board:

```
apio examples -d Alhambra-II/Blinky
```

* Enter the example folder

```
cd Alhambra-II/Blinky
```

* Synthesize and upload the bitstream to the board

```
apio upload
```
### Workflow

Once apio is installed, the workflow is rather easy:

* Edit the verilog files
* Synthesize and upload the bitstream just by executing the command:

```
apio upload
```

