[![](https://github.com/FPGAwars/Apio-wiki/raw/main/wiki/Logos/apio-banner.svg)](https://github.com/FPGAwars/apio/wiki)

# Contents
  * [Usage](#usage)  
  * [Description](#description)  
  * [Options](#options)
  * [Examples](#examples)  


# Usage

```bash
apio examples [OPTIONS]
```

# Description

Manage [verilog examples](https://github.com/FPGAwars/apio-examples): 

This command requires the **examples package**.

# Options

| Flag | Long Flag | Description |
| ---- | --------- | ----------- |
| `-l` | `--list`  | List all available examples |
| `-d` | `--dir`   | Copy the selected example directory |
| `-f` | `--files` | Copy the selected example files |
| `-p` | `--project-dir` | Set the target directory for the examples |  
| -`-n`| `--sayno` | Automatically answer NO to all the questions |


# Examples

## 1. Show all available examples

```bash
apio examples --list
```

```
$ apio examples --list

────────────────────────────────────────────────────────────────────────────────
Alhambra-II/ledon
Hello world for the Alhambra-II board: Turn on the LED0
────────────────────────────────────────────────────────────────────────────────
Alhambra-II/Template
Project template for the Alhambra-II board
────────────────────────────────────────────────────────────────────────────────
Alhambra-II/Blinky
Blinking LED 7
────────────────────────────────────────────────────────────────────────────────
Cat-board/blinky
Hello world example for the Cat Board: blinking an LED.
────────────────────────────────────────────────────────────────────────────────
ColoLight-5A-75E-V71_FT2232H/Blinky
Blinking LED
────────────────────────────────────────────────────────────────────────────────
ColoLight-5A-75E-V71_FT2232H/Ledon
Blinking LEDs D0-D5
────────────────────────────────────────────────────────────────────────────────
ColorLight-5A-75B-V8/Blinky
Blinking LED
────────────────────────────────────────────────────────────────────────────────
ColorLight-5A-75B-V8/Ledon
Blinking LEDs D0-D5
────────────────────────────────────────────────────────────────────────────────
EDU-CIAA-FPGA/Template
Project template for the EDU-CIAA-FPGA board
────────────────────────────────────────────────────────────────────────────────
EDU-CIAA-FPGA/Blinky
Blinking LED 0 (D6)
────────────────────────────────────────────────────────────────────────────────
EDU-CIAA-FPGA/led_green
Hello world example for the EDU-CIAA-FPGA board. Turning the led green on
────────────────────────────────────────────────────────────────────────────────
TinyFPGA-B2/blink13
Blink the led on pin 13 of the TinyFPGA-B2 board
────────────────────────────────────────────────────────────────────────────────
TinyFPGA-B2/template
Project template for the TinyFPGA-B2 board
────────────────────────────────────────────────────────────────────────────────
TinyFPGA-BX/clock_divider
A simple clock divider. It produces two clocks with 1/4 of the input frequency. One with the original phase and one shifted by 90 degrees. This divider by itself could run at >200 MHz.
────────────────────────────────────────────────────────────────────────────────
TinyFPGA-BX/Blinky
Blinking LED for the TinyFPGA
────────────────────────────────────────────────────────────────────────────────
TinyFPGA-BX/template
Project template for the TinyFPGA-BX board
────────────────────────────────────────────────────────────────────────────────
TinyFPGA-BX/blinkSOS
Blink SOS pattern on the led of the TinyFPGA-BX board
────────────────────────────────────────────────────────────────────────────────
blackice/Blinky
Blink LED 1 (blue)
────────────────────────────────────────────────────────────────────────────────
blackice/blink
It just blinks the red led 4 of the mystorm blackice board
────────────────────────────────────────────────────────────────────────────────
fomu/Blink
Simple tri-colour LED blink example
────────────────────────────────────────────────────────────────────────────────
fomu/Blinky
Simple tri-colour LED blink example
────────────────────────────────────────────────────────────────────────────────
go-board/Blinky
Blinking LED for the Nandland go board
────────────────────────────────────────────────────────────────────────────────
go-board/template
Project template for the Nandland go-board
────────────────────────────────────────────────────────────────────────────────
go-board/leds
Hello world example for the Nandland go board. Turning all the leds on
────────────────────────────────────────────────────────────────────────────────
go-board/pcf
Nandland go board constraint file
────────────────────────────────────────────────────────────────────────────────
iCE40-HX1K-EVB/leds
Verilog example for controlling leds with but on iCE40-HX1K-EVB.
────────────────────────────────────────────────────────────────────────────────
iCE40-HX8K/leds
Hello world example for the iCE40-HX8K board. Turning all the leds on
────────────────────────────────────────────────────────────────────────────────
iCE40-HX8K-EVB/leds
Verilog example for controlling leds with but on iCE40-HX1K-EVB.
────────────────────────────────────────────────────────────────────────────────
iCE40-UP5K/switches
Example of using 3 switches for setting the color of the RGB led
────────────────────────────────────────────────────────────────────────────────
iCE40-UP5K/led-green
Turning the RGB LED into Green
────────────────────────────────────────────────────────────────────────────────
iCE40-UP5K/blink
Blink the RGB LED
────────────────────────────────────────────────────────────────────────────────
iCEBreaker/buttons
Example of controlling the LED using the tact buttons on the board.
────────────────────────────────────────────────────────────────────────────────
iCEBreaker/Blinky
Blink the on board Green LED
────────────────────────────────────────────────────────────────────────────────
iCEBreaker/led-green
Turning the on board Green LED on but all the other controllable LED off.
────────────────────────────────────────────────────────────────────────────────
iCEBreaker/blink
Blink the on board Red and Green LEDs as well as the 5 LEDs found on the default PMOD P2 module.
────────────────────────────────────────────────────────────────────────────────
iCESugar_1_5/Blinky
Blink the on board Red, Green and Blue LEDs
────────────────────────────────────────────────────────────────────────────────
iceWerx/ledon
Hello world for the iceWerx board: Turn on the Red LED
────────────────────────────────────────────────────────────────────────────────
iceWerx/Blinky
Blinking the Green LED
────────────────────────────────────────────────────────────────────────────────
icestick/template
Project template for the icestick board
────────────────────────────────────────────────────────────────────────────────
icestick/leds
Hello world example for the Icestick board. Turning all the leds on
────────────────────────────────────────────────────────────────────────────────
icestick/pcf
Icestick board constraint file
────────────────────────────────────────────────────────────────────────────────
icezum/template
Project template for the icezum board
────────────────────────────────────────────────────────────────────────────────
icezum/leds
Hello world example for the Icezum board. Turning all the leds on
────────────────────────────────────────────────────────────────────────────────
icezum/pcf
Icezum board constraint file
────────────────────────────────────────────────────────────────────────────────
icezum/Marcha-Imperial
Project template for the icezum board
────────────────────────────────────────────────────────────────────────────────
icezum/wire
Verilog example on how to describe a simple wire
────────────────────────────────────────────────────────────────────────────────
icoboard/template
Project template for the icoboard board
────────────────────────────────────────────────────────────────────────────────
icoboard/leds
Hello world example for the Icoboard board. Turning all the leds on
────────────────────────────────────────────────────────────────────────────────
icoboard/pcf
Icoboard constraint file
────────────────────────────────────────────────────────────────────────────────
kefir/template
Project template for the Kéfir I board
────────────────────────────────────────────────────────────────────────────────
kefir/leds
Hello world example for the Kéfir I board. Turning all the leds on
────────────────────────────────────────────────────────────────────────────────
kefir/pcf
Kéfir I board constraint file
────────────────────────────────────────────────────────────────────────────────
ulx3s-12f/ledon
Hello world for the ulx3s board: Turn on the LED0
────────────────────────────────────────────────────────────────────────────────
ulx3s-12f/Blinky
Blinking LEDs D0-D5
────────────────────────────────────────────────────────────────────────────────
ulx3s-45f/Blinky
Blinking LEDs D0-D5
────────────────────────────────────────────────────────────────────────────────
ulx3s-85f/Blinky
Blinking LEDs D0-D5
────────────────────────────────────────────────────────────────────────────────
upduino31/testbench
A testbench with an automatic testing a sequential module.
────────────────────────────────────────────────────────────────────────────────
upduino31/pll
Using the PLL to generate 30Mhz clock from the external 12Mhz clock.
────────────────────────────────────────────────────────────────────────────────
upduino31/blinky
Blinking the RGB LEDs using the SB_RGBA_DRV primitive.
────────────────────────────────────────────────────────────────────────────────
Total: 61

To get an example, use the command:
   apio examples -d/-f name

Example of use:
   apio examples -f leds
Copy the leds example files to the current directory
```


## 2. Copy the ledon example files for the Alhambra II board

```bash
apio examples --files Alhambra-II/ledon
```

![](https://github.com/FPGAwars/Apio-wiki/blob/main/wiki/Apio-commands/apio-examples-01.png)  

## 3. Copy the ledon example directory for the Alhambra II board

```bash
apio examples --dir Alhambra-II/ledon
```

![](https://github.com/FPGAwars/Apio-wiki/blob/main/wiki/Apio-commands/apio-examples-02.png)  


-------
[![](https://github.com/FPGAwars/icestudio-wiki/raw/main/Logos/fgpawars-banner.svg)](https://fpgawars.github.io/)
