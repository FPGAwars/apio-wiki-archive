# Support a new board

In order to support a new board follow these steps:

1. Make sure your board (or FPGA) is supported by the [OSS CAD Suite](https://github.com/YosysHQ/oss-cad-suite-build)

2. **Find or add your FPGA name** in the [fpgas.json](https://github.com/FPGAwars/apio/blob/develop/apio/resources/fpgas.json) file

Ex.
```json
[...]
"iCE40-HX1K-TQ144": {
  "type": "hx",
  "size": "1k",
  "pack": "tq144"
}

"iCE40-HX8K-CT256": {
  "type": "hx",
  "size": "8k",
  "pack": "ct256"
}

"iCE40-LP8K-CM81": {
  "type": "lp",
  "size": "8k",
  "pack": "cm81"
}
[...]
```    

2. **Find or add your programmer** in `programmers.json <https://github.com/FPGAwars/apio/blob/develop/apio/resources/programmers.json>`_.

```json
"iceprog": {
  "command": "iceprog",
  "args": "-d i:0x${VID}:0x${PID}:${FTDI_ID}"
}

"icoprog": {
  "command": "export WIRINGPI_GPIOMEM=1; icoprog",
  "args": "-p <"
}

"tinyprog": {
  "command": "tinyprog",
  "args": "--pyserial -c ${SERIAL_PORT} --program",
  "pip_packages": [ "tinyprog" ]
}
```

**NOTE**: if your programmer uses a python package, add this package and its version range to `distribution.json <https://github.com/FPGAwars/apio/blob/develop/apio/resources/distribution.json>`

```json
"pip_packages": {
  "blackiceprog": ">=2.0.0,<3.0.0",
  "litterbox": ">=0.2.1,<0.3.0",
  "tinyfpgab": ">=1.1.0,<1.2.0",
  "tinyprog": ">=1.0.21,<1.1.0"
}
```

3. **Add your board** to `boards.json <https://github.com/FPGAwars/apio/blob/develop/apio/resources/boards.json>` with the following format:

```json
"icezum": {
  "name": "IceZUM Alhambra",
  "fpga": "iCE40-HX1K-TQ144",
  "programmer": {
    "type": "iceprog"
  },
  "usb": {
    "vid": "0403",
    "pid": "6010"
  },
  "ftdi": {
    "desc": "IceZUM Alhambra.*"
  }
}


"icoboard": {
  "name": "icoBOARD 1.0",
  "fpga": "iCE40-HX8K-CT256",
  "programmer": {
    "type": "icoprog"
  },
  "platform": "linux_armv7l"
}

"TinyFPGA-BX": {
  "name": "TinyFPGA BX",
  "fpga": "iCE40-LP8K-CM81",
  "programmer": {
    "type": "tinyprog"
  },
  "usb": {
    "vid": "1d50",
    "pid": "6130"
  },
  "tinyprog": {
    "desc": "TinyFPGA BX"
  }
}
```
