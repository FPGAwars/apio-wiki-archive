[![](https://github.com/FPGAwars/Apio-wiki/raw/main/wiki/Logos/apio-banner.svg)](https://github.com/FPGAwars/apio/wiki)

# Contents
  * [Usage](#usage)  
  * [Description](#description)  
  * [Options](#options)
  * [Examples](#examples)  


# Usage

```bash
apio boards [OPTIONS]
```

# Description

Show FPGA boards information

> [!NOTE]
> Check the [Supported boards](https://github.com/FPGAwars/apio/wiki/Supported-boards) page for a list of all the available boards 

# Options

| Flag | Long Flag | Description |
| ---- | --------- | ----------- |
| `-l` | `--list`  | List all available packages |
| `-f` | `--fpga` | List all supported FPGAs |

# Examples

## 1. Show all available boards

```bash
apio boards --list
```

```
────────────────────────────────────────────────────────────────────────────────
Board (FPGA, Arch, Type, Size, Pack)
────────────────────────────────────────────────────────────────────────────────
• Alchitry-Cu  (FPGA:iCE40-HX8K-CB132, ice40, hx, 8k, cb132)
• Butterstick-r10-2g-85k
      (FPGA:ECP5-LFE5UM5G-85F-CABGA381, ecp5, um5g-85k, 85k, CABGA381)
• Butterstick-r10-2g-85k_(FT2232H)
      (FPGA:ECP5-LFE5UM5G-85F-CABGA381, ecp5, um5g-85k, 85k, CABGA381)
• Butterstick-r10-2g-85k_(FT232H)
      (FPGA:ECP5-LFE5UM5G-85F-CABGA381, ecp5, um5g-85k, 85k, CABGA381)
• Cat-board  (FPGA:iCE40-HX8K-CT256, ice40, hx, 8k, ct256)
• ColorLight-5A-75B-V61
      (FPGA:ECP5-LFE5U-25F-CABGA381, ecp5, 25k, 25k, CABGA381)
• ColorLight-5A-75B-V7
      (FPGA:ECP5-LFE5U-25F-CABGA256, ecp5, 25k, 25k, CABGA256)
• ColorLight-5A-75B-V8
      (FPGA:ECP5-LFE5U-25F-CABGA256, ecp5, 25k, 25k, CABGA256)
• ColorLight-5A-75E-V6
      (FPGA:ECP5-LFE5U-25F-CABGA256, ecp5, 25k, 25k, CABGA256)
• ColorLight-5A-75E-V71_(FT2232H)
      (FPGA:ECP5-LFE5U-25F-CABGA256, ecp5, 25k, 25k, CABGA256)
• ColorLight-5A-75E-V71_(FT232H)
      (FPGA:ECP5-LFE5U-25F-CABGA256, ecp5, 25k, 25k, CABGA256)
• ColorLight-5A-75E-V71_(USB-Blaster)
      (FPGA:ECP5-LFE5U-25F-CABGA256, ecp5, 25k, 25k, CABGA256)
• ColorLight-i5-v7.0_(FT2232H)
      (FPGA:ECP5-LFE5U-25F-CABGA381, ecp5, 25k, 25k, CABGA381)
• ColorLight-i5-v7.0_(FT232H)
      (FPGA:ECP5-LFE5U-25F-CABGA381, ecp5, 25k, 25k, CABGA381)
• ColorLight-i5-v7.0_(USB-Blaster)
      (FPGA:ECP5-LFE5U-25F-CABGA381, ecp5, 25k, 25k, CABGA381)
• ColorLight-i9-v7.2_(FT2232H)
      (FPGA:ECP5-LFE5U-45F-CABGA381, ecp5, 45k, 45k, CABGA381)
• ColorLight-i9-v7.2_(FT232H)
      (FPGA:ECP5-LFE5U-45F-CABGA381, ecp5, 45k, 45k, CABGA381)
• ColorLight-i9-v7.2_(USB-Blaster)
      (FPGA:ECP5-LFE5U-45F-CABGA381, ecp5, 45k, 45k, CABGA381)
• ECP5-Evaluation-Board
      (FPGA:ECP5-LFE5UM5G-85F-CABGA381, ecp5, um5g-85k, 85k, CABGA381)
• ECP5-Mini-12
      (FPGA:ECP5-LFE5U-12F-CABGA256, ecp5, 12k, 12k, CABGA256)
• ECP5-Mini-25
      (FPGA:ECP5-LFE5U-25F-CABGA256, ecp5, 25k, 25k, CABGA256)
• FleaFPGA-Ohm_(FT2232H)
      (FPGA:ECP5-LFE5U-25F-CABGA381, ecp5, 25k, 25k, CABGA381)
• FleaFPGA-Ohm_(FT232H)
      (FPGA:ECP5-LFE5U-25F-CABGA381, ecp5, 25k, 25k, CABGA381)
• FleaFPGA-Ohm_(USB-Blaster)
      (FPGA:ECP5-LFE5U-25F-CABGA381, ecp5, 25k, 25k, CABGA381)
• OK-iCE40Pro  (FPGA:iCE40-UP5K-SG48, ice40, up, 5k, sg48)
• ThetaMachines-ETH4K  (FPGA:iCE40-HX4K-TQ144, ice40, hx, 8k, tq144:4k)
• TinyFPGA-B2  (FPGA:iCE40-LP8K-CM81, ice40, lp, 8k, cm81)
• TinyFPGA-BX  (FPGA:iCE40-LP8K-CM81, ice40, lp, 8k, cm81)
• TinyFPGA-EX-rev1
      (FPGA:ECP5-LFE5U-85F-CSFBGA285, ecp5, 85k, 85k, CSFBGA285)
• TinyFPGA-EX-rev2
      (FPGA:ECP5-LFE5UM5G-85F-CSFBGA285, ecp5, um5g-85k, 85k, CSFBGA285)
• alhambra-ii  (FPGA:iCE40-HX4K-TQ144, ice40, hx, 8k, tq144:4k)
• arice1  (FPGA:iCE40-UP5K-SG48, ice40, up, 5k, sg48)
• blackice  (FPGA:iCE40-HX4K-TQ144, ice40, hx, 8k, tq144:4k)
• blackice-ii  (FPGA:iCE40-HX4K-TQ144, ice40, hx, 8k, tq144:4k)
• blackice-mx  (FPGA:iCE40-HX4K-TQ144, ice40, hx, 8k, tq144:4k)
• edu-ciaa-fpga  (FPGA:iCE40-HX4K-TQ144, ice40, hx, 8k, tq144:4k)
• fomu  (FPGA:iCE40-UP5K-UWG30, ice40, up, 5k, uwg30)
• fpga101  (FPGA:iCE40-UP5K-SG48, ice40, up, 5k, sg48)
• go-board  (FPGA:iCE40-HX1K-VQ100, ice40, hx, 1k, vq100)
• iCE40-HX1K-EVB  (FPGA:iCE40-HX1K-VQ100, ice40, hx, 1k, vq100)
• iCE40-HX8K  (FPGA:iCE40-HX8K-CT256, ice40, hx, 8k, ct256)
• iCE40-HX8K-EVB  (FPGA:iCE40-HX8K-CT256, ice40, hx, 8k, ct256)
• iCE40-UL1K-Breakout  (FPGA:iCE40-UL1K-CM36A, ice40, ul, 1k, cm36a)
• iCE40-UP5K  (FPGA:iCE40-UP5K-SG48, ice40, up, 5k, sg48)
• iCEBreaker  (FPGA:iCE40-UP5K-SG48, ice40, up, 5k, sg48)
• iCEBreaker-bitsy0  (FPGA:iCE40-UP5K-SG48, ice40, up, 5k, sg48)
• iCEBreaker-bitsy1  (FPGA:iCE40-UP5K-SG48, ice40, up, 5k, sg48)
• iCESugar-Pro_(FT2232H)
      (FPGA:ECP5-LFE5U-25F-CABGA256, ecp5, 25k, 25k, CABGA256)
• iCESugar-Pro_(FT232H)
      (FPGA:ECP5-LFE5U-25F-CABGA256, ecp5, 25k, 25k, CABGA256)
• iCESugar-Pro_(USB-Blaster)
      (FPGA:ECP5-LFE5U-25F-CABGA256, ecp5, 25k, 25k, CABGA256)
• iCESugar-nano  (FPGA:iCE40-LP1K-CM36, ice40, lp, 1k, cm36)
• iCESugar_1_5  (FPGA:iCE40-UP5K-SG48, ice40, up, 5k, sg48)
• iceWerx  (FPGA:iCE40-HX8K-CB132, ice40, hx, 8k, cb132)
• iceblink40-hx1k  (FPGA:iCE40-HX1K-VQ100, ice40, hx, 1k, vq100)
• icefun  (FPGA:iCE40-HX8K-CB132, ice40, hx, 8k, cb132)
• icestick  (FPGA:iCE40-HX1K-TQ144, ice40, hx, 1k, tq144)
• icezum  (FPGA:iCE40-HX1K-TQ144, ice40, hx, 1k, tq144)
• icoboard  (FPGA:iCE40-HX8K-CT256, ice40, hx, 8k, ct256)
• kefir  (FPGA:iCE40-HX4K-TQ144, ice40, hx, 8k, tq144:4k)
• orangecrab-r02-25f
      (FPGA:ECP5-LFE5U-25F-CSFBGA285, ecp5, 25k, 25k, CSFBGA285)
• orangecrab-r02-85f
      (FPGA:ECP5-LFE5U-85F-CSFBGA285, ecp5, 85k, 85k, CSFBGA285)
• pico-ice  (FPGA:iCE40-UP5K-SG48, ice40, up, 5k, sg48)
• ulx3s-12f  (FPGA:ECP5-LFE5U-12F-CABGA381, ecp5, 12k, 12k, CABGA381)
• ulx3s-25f  (FPGA:ECP5-LFE5U-25F-CABGA381, ecp5, 25k, 25k, CABGA381)
• ulx3s-45f  (FPGA:ECP5-LFE5U-45F-CABGA381, ecp5, 45k, 45k, CABGA381)
• ulx3s-85f  (FPGA:ECP5-LFE5U-85F-CABGA381, ecp5, 85k, 85k, CABGA381)
• upduino  (FPGA:iCE40-UP5K-SG48, ice40, up, 5k, sg48)
• upduino2  (FPGA:iCE40-UP5K-SG48, ice40, up, 5k, sg48)
• upduino21  (FPGA:iCE40-UP5K-SG48, ice40, up, 5k, sg48)
• upduino3  (FPGA:iCE40-UP5K-SG48, ice40, up, 5k, sg48)
• upduino31  (FPGA:iCE40-UP5K-SG48, ice40, up, 5k, sg48)
• versa  (FPGA:ECP5-LFE5UM-45F-CABGA381, ecp5, um-45k, 45k, CABGA381)
────────────────────────────────────────────────────────────────────────────────
Total: 72 boards

Use `apio init --board <boardname>` to create a new apio project for that board
```


## 2. Show all available FPGAs

```bash
apio boards --fpga
```

```
────────────────────────────────────────────────────────────────────────────────
FPGA                            Arch     Type         Size  Pack      
────────────────────────────────────────────────────────────────────────────────
• ECP5-LFE5U-12F-CABGA256         ecp5     12k          12k   CABGA256  
• ECP5-LFE5U-12F-CABGA381         ecp5     12k          12k   CABGA381  
• ECP5-LFE5U-12F-CSFBGA285        ecp5     12k          12k   CSFBGA285 
• ECP5-LFE5U-25F-CABGA256         ecp5     25k          25k   CABGA256  
• ECP5-LFE5U-25F-CABGA381         ecp5     25k          25k   CABGA381  
• ECP5-LFE5U-25F-CSFBGA285        ecp5     25k          25k   CSFBGA285 
• ECP5-LFE5U-45F-CABGA256         ecp5     45k          45k   CABGA256  
• ECP5-LFE5U-45F-CABGA381         ecp5     45k          45k   CABGA381  
• ECP5-LFE5U-45F-CABGA554         ecp5     45k          45k   CABGA554  
• ECP5-LFE5U-45F-CSFBGA285        ecp5     45k          45k   CSFBGA285 
• ECP5-LFE5U-85F-CABGA381         ecp5     85k          85k   CABGA381  
• ECP5-LFE5U-85F-CABGA554         ecp5     85k          85k   CABGA554  
• ECP5-LFE5U-85F-CABGA756         ecp5     85k          85k   CABGA756  
• ECP5-LFE5U-85F-CSFBGA285        ecp5     85k          85k   CSFBGA285 
• ECP5-LFE5UM-25F-CABGA256        ecp5     um-25k       25k   CABGA256  
• ECP5-LFE5UM-25F-CABGA381        ecp5     um-25k       25k   CABGA381  
• ECP5-LFE5UM-25F-CSFBGA285       ecp5     um-25k       25k   CSFBGA285 
• ECP5-LFE5UM-45F-CABGA256        ecp5     um-45k       45k   CABGA256  
• ECP5-LFE5UM-45F-CABGA381        ecp5     um-45k       45k   CABGA381  
• ECP5-LFE5UM-45F-CABGA554        ecp5     um-45k       45k   CABGA554  
• ECP5-LFE5UM-45F-CSFBGA285       ecp5     um-45k       45k   CSFBGA285 
• ECP5-LFE5UM-85F-CABGA381        ecp5     um-85k       85k   CABGA381  
• ECP5-LFE5UM-85F-CABGA554        ecp5     um-85k       85k   CABGA554  
• ECP5-LFE5UM-85F-CABGA756        ecp5     um-85k       85k   CABGA756  
• ECP5-LFE5UM-85F-CSFBGA285       ecp5     um-85k       85k   CSFBGA285 
• ECP5-LFE5UM5G-25F-CABGA256      ecp5     um5g-25k     25k   CABGA256  
• ECP5-LFE5UM5G-25F-CABGA381      ecp5     um5g-25k     25k   CABGA381  
• ECP5-LFE5UM5G-25F-CSFBGA285     ecp5     um5g-25k     25k   CSFBGA285 
• ECP5-LFE5UM5G-45F-CABGA256      ecp5     um5g-45k     45k   CABGA256  
• ECP5-LFE5UM5G-45F-CABGA381      ecp5     um5g-45k     45k   CABGA381  
• ECP5-LFE5UM5G-45F-CABGA554      ecp5     um5g-45k     45k   CABGA554  
• ECP5-LFE5UM5G-45F-CSFBGA285     ecp5     um5g-45k     45k   CSFBGA285 
• ECP5-LFE5UM5G-85F-CABGA381      ecp5     um5g-85k     85k   CABGA381  
• ECP5-LFE5UM5G-85F-CABGA554      ecp5     um5g-85k     85k   CABGA554  
• ECP5-LFE5UM5G-85F-CABGA756      ecp5     um5g-85k     85k   CABGA756  
• ECP5-LFE5UM5G-85F-CSFBGA285     ecp5     um5g-85k     85k   CSFBGA285 
• iCE40-HX1K-CB132                ice40    hx           1k    cb132     
• iCE40-HX1K-TQ144                ice40    hx           1k    tq144     
• iCE40-HX1K-VQ100                ice40    hx           1k    vq100     
• iCE40-HX4K-BG121                ice40    hx           8k    bg121:4k  
• iCE40-HX4K-CB132                ice40    hx           8k    cb132:4k  
• iCE40-HX4K-TQ144                ice40    hx           8k    tq144:4k  
• iCE40-HX8K-BG121                ice40    hx           8k    bg121     
• iCE40-HX8K-CB132                ice40    hx           8k    cb132     
• iCE40-HX8K-CM225                ice40    hx           8k    cm225     
• iCE40-HX8K-CT256                ice40    hx           8k    ct256     
• iCE40-LP1K-CB121                ice40    lp           1k    cb121     
• iCE40-LP1K-CB81                 ice40    lp           1k    cb81      
• iCE40-LP1K-CM121                ice40    lp           1k    cm121     
• iCE40-LP1K-CM36                 ice40    lp           1k    cm36      
• iCE40-LP1K-CM49                 ice40    lp           1k    cm49      
• iCE40-LP1K-CM81                 ice40    lp           1k    cm81      
• iCE40-LP1K-QN84                 ice40    lp           1k    qn84      
• iCE40-LP1K-SWG16TR              ice40    lp           1k    swg16tr   
• iCE40-LP384-CM36                ice40    lp           384   cm36      
• iCE40-LP384-CM49                ice40    lp           384   cm49      
• iCE40-LP384-QN32                ice40    lp           384   qn32      
• iCE40-LP4K-CM121                ice40    lp           8k    cm121:4k  
• iCE40-LP4K-CM225                ice40    lp           8k    cm225:4k  
• iCE40-LP4K-CM81                 ice40    lp           8k    cm81:4k   
• iCE40-LP8K-CM121                ice40    lp           8k    cm121     
• iCE40-LP8K-CM225                ice40    lp           8k    cm225     
• iCE40-LP8K-CM81                 ice40    lp           8k    cm81      
• iCE40-UL1K-CM36A                ice40    ul           1k    cm36a     
• iCE40-UP5K-SG48                 ice40    up           5k    sg48      
• iCE40-UP5K-UWG30                ice40    up           5k    uwg30     
────────────────────────────────────────────────────────────────────────────────
Total: 66 fpgas
```


-------
[![](https://github.com/FPGAwars/icestudio-wiki/raw/main/Logos/fgpawars-banner.svg)](https://fpgawars.github.io/)
