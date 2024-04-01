[![](https://github.com/FPGAwars/Apio-wiki/raw/main/wiki/Logos/apio-banner.svg)](https://github.com/FPGAwars/apio/wiki)

# Contents
  * [Usage](#usage)  
  * [Description](#description)  
  * [Options](#options)
  * [Examples](#examples)  


# Usage

```bash
apio build [OPTIONS]
```

# Description

Synthesize the bitstream: generates a `.bin` file from the **verilog sources** and **constaint file**

Required package: `oss-cad-suite`

# Options

| Flag | Long Flag    | Description |
| ---- | ------------ | ----------- |
| `-b` | `--board`    | Select a specific board |
|      | `--fpga`     | Select a specific FPGA |
|      | `--size --type --pack`    | Select a specific FPGA size, type and pack |
| `-p` | `--project-dir` | Set the target directory for the project. |  
| `-v` | `--verbose`  | Show the entire output of the command |  
|      | `--verbose-yosys` | Show the yosys output of the command |
|      | `--verbose-pnr` | Show the pnr output of the command |  
|      | `--top-module str` | Set the top level module (w/o .v ending) for build |  


# Examples

## 1. List connected FTDI devices

```bash
apio system --lsftdi
```

```
$ apio system --lsftdi
Number of FTDI devices found: 1
Checking device: 0
Manufacturer: AlhambraBits, Description: Alhambra II v1.0A - B07-095
```


## 2. List connected USB devices

```bash
apio system --lsusb
```

```
$ apio system --lsusb
1d6b:0003 (bus 2, device 1)
04f2:b68b (bus 1, device 3) path: 7
0403:6010 (bus 1, device 5) path: 5
062a:4102 (bus 1, device 2) path: 4
8087:0aaa (bus 1, device 4) path: 10
1d6b:0002 (bus 1, device 1)
```

## 3. List connected Serial devices

```bash
apio system --lsserial
```

```
$ apio system --lsserial
Number of Serial devices found: [{'port': '/dev/ttyUSB1', 'description': 'Alhambra II v1.0A - B07-095 - Alhambra II v1.0A - B07-095', 'hwid': 'USB VID:PID=0403:6010 LOCATION=1-5:1.1'}, {'port': '/dev/ttyUSB0', 'description': 'Alhambra II v1.0A - B07-095 - Alhambra II v1.0A - B07-095', 'hwid': 'USB VID:PID=0403:6010 LOCATION=1-5:1.0'}]

/dev/ttyUSB1
Description: Alhambra II v1.0A - B07-095 - Alhambra II v1.0A - B07-095
Hardware info: USB VID:PID=0403:6010 LOCATION=1-5:1.1

/dev/ttyUSB0
Description: Alhambra II v1.0A - B07-095 - Alhambra II v1.0A - B07-095
Hardware info: USB VID:PID=0403:6010 LOCATION=1-5:1.0
```

## 4. Show system information

```bash
apio system --info
```

```
$ apio system --info
Platform: linux_x86_64

```

-------
[![](https://github.com/FPGAwars/icestudio-wiki/raw/main/Logos/fgpawars-banner.svg)](https://fpgawars.github.io/)
