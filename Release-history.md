[![](https://github.com/FPGAwars/Apio-wiki/raw/main/wiki/Logos/apio-banner.svg)](https://github.com/FPGAwars/apio/wiki)

## Introduction 

Here you can find the **release notes** for the different versions of Apio

## Index

| Version                   | Comments           |
| --------------------------|--------------------|
| [Latest changes](#latest-changes) |   | 
| [Version 0.7.6](#version-076)  | Bugs fixed. It works ok with icestudio >= 0.6.1  |
| [Version 0.7.5](#version-075) | Bug fixed. System package is obsolete |
| [Version 0.7.4](#version-074) | Documentation moved to the wiki |
| [Version 0.7.3](#version-073) | OpenFPGALoader added, oss-cad-suite package (0.0.3), refactoring |
| [Version 0.6.7](#version-067) | Bug fixed |
| [Version 0.6.3](#version-063) | New boards, Bug fixed, Github actions |
| [Version 0.6.0](#version-060) | New boards: Orange Crab, Olimex, EDU-CIAA-FPGA... |
| [Version 0.5.4](#version-054) | Bug fixed |
| [Version 0.5.0](#version-050) | New board: Blackice-MX. Toolchain updated. Bug fixed |
| [Version 0.4.1](#version-041) | Support new boards: Alchitry-Cu, Fomu  |
| [Version 0.4.0](#version-040) | New command: raw. Support new boards: UPDuino, iCEBreaker |
| [Version 0.3.6](#version-036) | Improved TinyFPGA BX integration |
| [Version 0.3.4](#version-034) | New boards: TinyFPGA BX, iCEblink40-HX1K. New command: lint |
| [Version 0.3.3](#version-033) | New board: Alhambra II |
| [Version 0.3.0](#version-030) | New commands. Updated apio drivers command |
| [Version 0.2.0](#version-020) | New commands. New boards |
| [Version 0.1.0](#version-010) | New commands: examples, init, system |
| [Version 0.0.4](#version-004) | New commandos. Boards: IceZum Alhambra, iCEstick |

## Latest changes

* Synthesis of bitstream for ECP5 12K finally solved ([Fernando mosquera](https://github.com/benitoss) (@benitoss))
* Recover the support of iCESugar-nano ([Fernando mosquera](https://github.com/benitoss) (@benitoss))
* Synthesis for ECP5 12K solved ([Fernando mosquera](https://github.com/benitoss) (@benitoss))
* Making distinction between a v0 and v1 board (Thanks to [seanybaggins](https://github.com/seanybaggins) @seanybaggins)
* Solution for all ECP5 models (thanks to [Fernando mosquera](https://github.com/benitoss) (@benitoss))
* Support for the ECP5-Evaluation-Board (thanks to [Fernando mosquera](https://github.com/benitoss) (@benitoss))
* Fixed call to non-existant function (Thanks to [seanybaggins](https://github.com/seanybaggins) @seanybaggins)
* Update iCEBreaker-bitsy board support (Thanks to [suzuki-naoto](https://github.com/suzuki-naoto) @suzuki-naoto)
* apio lint now depends only on the oss-cad-suite package
* test: apio verify passed
* Bug fixed: apio verify error in ice40
* iverilog is run from the oss-cad-suite package 
* scons upgraded to the latest version: 4.2.0
* scons is no longer an independent apio package. It is installed as a python package instead
* scons apio package is now obsolete and not installed with apio install -a
* Bug fixed: trellis and icebox environment variables fixed
* ECP5: Bug fixed: Bitstream regenerated when the .lpf is changed
* Support for the FleaFPGA-Ohm Board added (thanks to [Fernando mosquera](https://github.com/benitoss) (@benitoss))
* lib folder included in the path
* ice40 package: no longer needed for building
* Package ice40 marked as obsolete
* yosys: included in the obsolete package list
* build: package oss-cad-suite used instead of yosys 

## Version 0.7.6
* **Date**: 2021-07-26
* Bug Fixed: The checking of the installed packages was not correctly done if  they are installed in another folder different than the default 
* Now it should work ok with Icestudio >=0.6.1

## Version 0.7.5
* **Date**: 2021-07-21
* Tools-system package is no longer installed with `apio install -a` (as it is considered obsolete)  
* Security vulnerability fixed. Thanks to @Xesxen. No token used for accesing the github api: Currently only 60 petitions per hour can be made, but it should be enough by the moment (as it is only used for installing packages)
* Fixed a bug in the tests. Thanks to @Luflosi

## Version 0.7.4
* **Date**: 2021-07-20
* All the images used in the documentation wiki have been moved to the repo [Apio-wiki](https://github.com/FPGAwars/Apio-wiki) and no longer are included in the pypi apio package (so it is faster to download and to install)

## Version 0.7.3
* **Date**: 2021-07-20
* [Toolchain ECP5](https://github.com/FPGAwars/toolchain-ecp5):
  * **OpenFPGALoader** tool added for programing the ECP5 FPGAs (Thanks to [Fernando Mosquera](https://github.com/benitoss) (@benitoss)) 
* New apio package: [oss-cad-suite](https://github.com/FPGAwars/tools-oss-cad-suite/wiki)
  * Currently only with the system tools: lsusb, lsftdi, ftdi_eeprom  
* Apio [system package](https://github.com/FPGAwars/tools-system/wiki) marked as obsolete (although it can still be installed and used). Use the oss-cad-suite apio package instead
* Refactoring and documentation of the code

## Version 0.6.7
* **Date**: 2021-06-26
* Bug fixed: Extra packages are separated, so that they can be installed individually
  * blackiceprog
  * litterbox
  * tinyfpgab
  * tinyprog
  * icefunprog
* More bug fixed

## Version 0.6.3
* **Date**: 2021-06-26
* Add OK-iCE40Pro to boards.json
* Support iCESugar-nano board
* Initial support for the Colorlight boards
* Bug fixed
* Migration to flit
* Migration to Github actions
* Automatic publishing of version in pypi for every release
* Bug Fixed: Environment variables with quoted paths are allowed

## Version 0.6.0
* **Date**: 2020-12-13
* New board: OrangeCrab
* New board: olimex board
* New board: IceFun
* New board: Upduino v3.0
* New board: EDU-CIAA-FPGA
* Many Bugs fixed
* New package: fujprog
* New board: Radiona ULX3S
* New board: iCESugar v1.5
* Documentation added
* New package: dfu


## Version 0.5.4
* **Date**: 2020-02-26
* Fix ecp5 and ice40 definitions
* Bug Fixed

## Version 0.5.0

* **Date**: 2020-02-21
* New board: Blackice-MX
* Bug Fixed
* Toolchains updated

## Version 0.4.1

* **Date**:  2019-09-09

### Added
- Support new boards:
  - Alchitry-Cu (#179)
  - Fomu (#182)
- Add project structure to the docs (#177)

## Fixed
- Pytest "offline" option
- Production iCEBreaker USB strings (#181)



## Version 0.4.0

* **Date**: 2018-11-07

### Added
- New command: raw.
- Support new boards:
  - UPDuino v1.0
  - UPDuino v2.0
  - iCEBreaker
  - iCEBreaker bitsy
  - FPGA 101 Workshop Badge Board
  - iCE40 UltraPlus Breakout Board

## Version 0.3.6

* **Date**: 2018-09-16

### Changed
- Improve TinyFPGA BX integration

## Version 0.3.4

* **Date**: 2018-08-17

### Added
- New command: lint.
- Support new boards:
  - TinyFPGA BX
  - iCEblink40-HX1K


## Version 0.3.3

* **Date**: 2018-05-10

### Added
- Support new boards:
  - Alhambra II

## Version: 0.3.0

* **Date**: 2018-02-01

### Added
- Support new boards:
  - TinyFPGA B2
  - BlackIce
  - BlackIce II

### Changed
- Update "apio drivers" options: ftdi, serial.

## Version 0.2.0

- **Date**: 2016-12-01

### Added
- New commands: verify, boards, config, drivers, upgrade.
- Support new boards:
  - Nandland Go board
  - icoBOARD 1.0
  - Kéfir I iCE40-HX4K
  - iCE40-HX8K Breakout Board
  - CAT Board

### Removed
- Delete command: debug.

## Version 0.1.0

* **Date**:  2016-04-14  

### Added
- New commands: examples, init, system.


## Version 0.0.4

* **Date**: 2016-02-24 
 
### Added
- New commands: build, clean, debug, install, sim, time, uninstall, upload.
- Support new boards:
  - iCEstick Evaluation Kit
  - IceZUM Alhambra.

-------
[![](https://github.com/FPGAwars/icestudio-wiki/raw/main/Logos/fgpawars-banner.svg)](https://fpgawars.github.io/)
