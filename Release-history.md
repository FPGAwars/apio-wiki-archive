[![](https://github.com/FPGAwars/Apio-wiki/raw/main/wiki/Logos/apio-banner.svg)](https://github.com/FPGAwars/apio/wiki)

## Introduction 

Here you can find the **release notes** for the different versions of Apio

## Index

| Version                   | Comments           |
| --------------------------|--------------------|
| [Latest changes](#latest-changes) | [Latest commits in develop branch](https://github.com/FPGAwars/apio/commits/develop)  | 
| [Version 0.9.5](#version-095) | Bug fixed release: | issues #379 and #380 |
| [Version 0.9.4](#version-094) | Bug fixed release: Bug fixed: unicode character map error in Windows OS and some linux distributions with non native unicode support | 
| [Version 0.9.3](#version-093) | Bug Fixes release: Bug fixed: apio graph, apio drivers, Documentation moved to wiki |
| [Version 0.9.2](#version-092) | Bug Fixes release: Error when uploading, building, verifying from icestudio |
| [Version 0.9.1](#version-091) | Top module name is now mandatory. OSS-cad-suite@0.0.9. New commands. Bug fixed. Cleaned Code|
| [Version 0.8.4](#version-084) | Quick update release: New boards orangecrab, ButerSticr1.0 |
| [Version 0.8.3](#version-083) | Bug fixes release |
| [Version 0.8.2](#version-082) | Obsolete apio packages removed. Github api no longer used. New boards. Many Bug fixed |
| [Version 0.8.1](#version-081) | Transition to the **oss-cad-suite** complete! |
| [Version 0.8.0.post1](#version-080post1)  | Apio dependencies fixed |
| [Version 0.8.0](#version-080) | Transitional version. Migration to oss-cad-suite in progress|
| [Version 0.7.6](#version-076) | Bugs fixed. It works ok with icestudio >= 0.6.1  |
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

* [Latest commits in develop branch](https://github.com/FPGAwars/apio/commits/develop)

## Version 0.9.5
* **Date**: 2024-June-14
* **NOTE**: Bug Fix release
* Bug fixed: issue #380, missing 'packaing' package in dependencies ([Obijuan](https://github.com/Obijuan))
* Bug fixed: issue #379, oss-cad-suite download link for darwin_x86_64 not correctly generated ([Obijuan](https://github.com/Obijuan))

## Version 0.9.4
* **Date**: 2024-April-29
* **NOTE**: Bug Fix release
* Bug fixed: unicode character map error in Windows OS and some linux distributions with non native unicode support ([Cavearr](https://github.com/cavearr)).
  * This bug caused Icestudio 0.12 not working ok in some platforms. Some unicode characters have been removed from apio (screenshots not updated in the documentation). They will be restored in next versions

## Version 0.9.3
* **Date**: 2024-April-02
* **NOTE**: Quick update release
* Bug fixed: apio main help: output reformated, by ([Obijuan](https://github.com/Obijuan))
* Documentation moved to the wiki, ([Obijuan](https://github.com/Obijuan))
* Windows: Apio drivers --ftdi_enable: code refactoring, ([Obijuan](https://github.com/Obijuan))
* Bug fixed: #363: Error when executing apio graph, ([Obijuan](https://github.com/Obijuan))
* issue #361: Improve error message in windows when running apio drivers --ftdi-enable, ([Obijuan](https://github.com/Obijuan))

## Version 0.9.2
* **Date**: 2024-March-23
* **NOTE**: Quick update release
* Bug Fixed: Error when uploading, building, verifying from icestudio ([Obijuan](https://github.com/Obijuan))

## Version 0.9.1
* **Date**: 2024-March-22
* **NOTE**: The top module name is now mandatory. It should be configured in the apio.ini file (or pass as an argument). The default module name used is `main`. Apio projects created with apio < 0.9.1 may not work unless the top-module is configured
* **OSS-CAD-SUITE**: [Version 0.0.9](https://github.com/FPGAwars/tools-oss-cad-suite/releases/tag/v0.0.9). 3-Oct-2023. Yosys: 0.33+103. Nextpnr: 0.6-118. OpenFPGALoader: 0.11.0 ([Cavearr](https://github.com/cavearr)) 
* Code cleaning, documentation and refactoring ([Obijuan](https://github.com/Obijuan))
* Add top-module parameter to the apio.ini file ([Obijuan](https://github.com/Obijuan))
* apio init now includes the option parameter top-module ([Obijuan](https://github.com/Obijuan))
* TinyFPGA-BX upload messages improved ([Obijuan](https://github.com/Obijuan))
* iceprog upload messages improved ([Obijuan](https://github.com/Obijuan))
* apio install -l: Package listing improved ([Obijuan](https://github.com/Obijuan))
* apio examples -l: examples listing improved ([Obijuan](https://github.com/Obijuan))
* apio boards -l: board listing improved ([Obijuan](https://github.com/Obijuan))
* Add suport for the **Theta Machines ETH4K board** by ([will-hut](https://github.com/will-hut)) in https://github.com/FPGAwars/apio/pull/339
* Added to the **apio sim** an optional **-testbench flag**  by ([zapta](https://github.com/zapta)) in https://github.com/FPGAwars/apio/pull/341
* Extended the **apio clean** command to delete all the .out and .vcd files. by ([zapta](https://github.com/zapta)) in https://github.com/FPGAwars/apio/pull/342
* Changed the behavior of the **sim command** to require --testbench flag if more than once benchmark is found. ([zapta](https://github.com/zapta)) in https://github.com/FPGAwars/apio/pull/343
* **Apio verify/lint** commands now process also all the testbench files. by ([zapta](https://github.com/zapta)) in https://github.com/FPGAwars/apio/pull/344
* Added to the **gtkwave command** a flag to disable the splash screen. by ([zapta](https://github.com/zapta)) in https://github.com/FPGAwars/apio/pull/347
* Fixing the **apio time** command. by ([zapta](https://github.com/zapta)) in https://github.com/FPGAwars/apio/pull/349
* Changed the default zoom of gtkwave from min to max. by ([zapta](https://github.com/zapta)) in https://github.com/FPGAwars/apio/pull/350
* Added an **apio test** command.  by ([zapta](https://github.com/zapta)) in https://github.com/FPGAwars/apio/pull/352
* Tweaking the verify command warnings. by ([zapta](https://github.com/zapta)) in https://github.com/FPGAwars/apio/pull/353
* Added the **alias -h** to the existing --help flag. ([zapta](https://github.com/zapta)) in https://github.com/FPGAwars/apio/pull/355
* Added the **apio graph** command which generates a svg graph of the verilog code. by ([zapta](https://github.com/zapta)) in https://github.com/FPGAwars/apio/pull/356
* Two minor fixes. Click command metavar and yosys graph command. by ([zapta](https://github.com/zapta)) in https://github.com/FPGAwars/apio/pull/359
* Undoing a previous change in the yosys graph generation command that was apparently unnecessary.  by ([zapta](https://github.com/zapta)) in https://github.com/FPGAwars/apio/pull/360
* Added support for OSX arm 64, by ([Cavearr](https://github.com/cavearr))
* Fix *unconstrained in LPF* for ecp5 boards with the new oss cad suite, by ([Cavearr](https://github.com/cavearr)) 
* Fix SConstruct bug for ecp5 boards and support for custom top module by command line, by ([Cavearr](https://github.com/cavearr)) 

## Version 0.8.4
* **Date**: 2023-Oct-3
* **NOTE**: Quick update release
* New board: orangecrab-r02-85f ([benitoss](https://github.com/benitoss)) 
* New board: ButerSticr1.0 DFU & FT2232H ([benitoss](https://github.com/benitoss)) 
* ECP5 FPGAs: compress bitstream generation (Add flag --compress) ([benitoss](https://github.com/benitoss)) 

## Version 0.8.3
* **Date**: 2023-Oct-1
* **NOTE**: Bug fixes release
* Fix duplicate execution for deprecated tools ([Cavearr](https://github.com/cavearr))
  * It solves two bugs in icestudio
    * Bitstream uploaded twice
    * No FPGA resources shown

## Version 0.8.2
* **Date**: 2023-September-29
* **NOTE**: old apio packages fully removed
* Adding documentation about apio build --top-module ([luongb](https://github.com/luongb))
* Apio build parameter for top-lvl module ([luongb](https://github.com/luongb))
* Apio build -v(verbose) fix ([luongb](https://github.com/luongb))
* Bug fixed: wrong type of quotes used. Caused JSON decoder error ([luongb](https://github.com/luongb))
* Add fpga for iCE40-UL1K-CM36A ([Kirk Clendinning](https://github.com/kirk-clendinning))
* Adding the iCE UltraLite Breakout Board ([Kirk Clendinning](https://github.com/kirk-clendinning))
* github actions improved ([Obijuan](https://github.com/Obijuan))
* Newer iCE40-HX8K and ECP5 Versa boards supported ([Obijuan](https://github.com/Obijuan))
* Python packages upgraded (request 2.28.2, click 8.1.3, colorama 0.4.6) ([Obijuan](https://github.com/Obijuan)) 
* Bug fixed in iCESugar-Pro ([ahaberlach](https://github.com/ahaberlach))  
* New board: Pico-Ice ([benitoss](https://github.com/benitoss))  
* Newer Icestick boards supported ([himarcarmona](https://github.com/himarcarmona))  
* New FT232H programer for the ColorLight i9  ([jojo535275](https://github.com/jojo535275))  
* New USB-Blaster programer for the colorlight i9 ([jojo535275](https://github.com/jojo535275))  
* Bug fixed in Colorlight 5A-75B V6.1 ([benitoss](https://github.com/benitoss))  
* Newer Lattice iCE40UP5K Breakout boards are supported ([Kevin Lutzer](https://github.com/kevinlutzer))
* New board: ColorLight-i9-v7.2_(FT2232H) ([jojo535275](https://github.com/jojo535275))
* Old functions removed ([Obijuan](https://github.com/Obijuan))  
* Code refactoring ([Obijuan](https://github.com/Obijuan))  
* Code clean: Lint score 10/10 ([Obijuan](https://github.com/Obijuan)) 
* **Github API not accessed anymore**. The latest version of the apio packages is shown in the `VERSION` file ([Obijuan](https://github.com/Obijuan))  
* Obsolete packages no longer shown with `apio install -l` ([Obijuan](https://github.com/Obijuan))  
* Obsolete Apio packages removed: Scons, dfu, icesprog, fujprog, Yosys, ecp5, iverilator, Verilator, System-tools ([Obijuan](https://github.com/Obijuan))

## Version 0.8.1

* **Date**: 2022-April-28
* **NOTE**: Transition to the **oss-cad-suite** complete! The old packages are obsolete, but can still be installed. In the next release they will be fully removed
* Support for the iceWerx board added ([Obijuan](https://github.com/Obijuan)) 
* Examples added ([Obijuan](https://github.com/Obijuan)) 
* Test-examples: alhambra-II. Testbenches added ([Obijuan](https://github.com/Obijuan)) 
* ECP5: SConstruct: message: no time analysis ([Obijuan](https://github.com/Obijuan)) 
* ecp5: iverilog: scons: added missing " " ([Obijuan](https://github.com/Obijuan)) 
* ice40: Sconstruct. Iverilog: added missing " " ([Obijuan](https://github.com/Obijuan)) 
* Bug fixed: apio time only depends on the oss-cad-suite package ([Obijuan](https://github.com/Obijuan)) 
* Bug fixed: apio sim no longer requires the iverilog package] ([Obijuan](https://github.com/Obijuan)) 
* fixed: get_terminal_size() ([Obijuan](https://github.com/Obijuan)) 
* Added upduino v3.1 ([vr2045](https://github.com/vr2045)) 
* The Alchitry Cu board fixes ([goodney](https://github.com/goodney))
* dfu, fujprog,icesprog and ecp5 packages declared as obsoletes ([Obijuan](https://github.com/Obijuan)) 
* Verilator declared as obsolete package ([Obijuan](https://github.com/Obijuan)) 
* Package iverilog is now declared obsolete ([Obijuan](https://github.com/Obijuan)) 
* Readme: Update OrangeCrab/ButterStick ([gregdavill](https://github.com/gregdavill)) 
* Test examples for different boards: ([Obijuan](https://github.com/Obijuan)) 
  * Icesugar-1.5
  * Radiona ULX3S-12F
  * Icebreaker
  * TinyFPGA-BX
  * Fomu
  * ICE40UP
  * Blackice
  * ICE40-BreakBoard
  * Go-board
  * Alhambra II
  * Icezum Alhambra
* Add butterstick support (and fix small orangecrab typo) (Andrew Goodney)
  
## Version 0.8.0.post1

* **Date**: 2022-April-2
* Apio dependencies fixed
* Bug fixed: It fixed the "get_terminal_size" error that appears because click version 0.8.1 was automaticaly installed (since March-28-2022)
* The click version has been change to 0.7.2 temporaly for fixing the problem (it will be upgraded to 0.8.1 in the comming releases)  

## Version 0.8.0

* **Date**: 2021-12-27
* **NOTE**: Transitional version. All the old apio packages are being replaced by the **oss-cad-suite**. Many things can be broken, so use it with caution and fill issues with the problems found. 
* USE WITH **ICESTUDIO >= 8.1** (It will NOT work with icestudio <=8.0)
* Bumped to version 0.8.0 ([Obijuan](https://github.com/Obijuan) @Obijuan)
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
