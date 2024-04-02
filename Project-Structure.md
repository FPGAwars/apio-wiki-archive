[![](https://github.com/FPGAwars/Apio-wiki/raw/main/wiki/Logos/apio-banner.svg)](https://github.com/FPGAwars/apio/wiki)

# Project Structure

An Apio project consist of the following files:

* The `apio.ini`. This is generated using [apio init](https://github.com/FPGAwars/apio/wiki/Apio-init)
* A **constraint file** (`.pcf` or `.lpf`). There should be exactly one constraint file per Apio project
  The first constraint file that is found will be used for mapping wires to the physical FPGA pins for [apio build](https://github.com/FPGAwars/apio/wiki/Apio-Build)
* **Verilog source** files. All files ending in ``.v`` will be selected and included in the project automatically.
  If you don't want to include a Verilog file automatically, name it as ``.vh`` (Verilog Header) to exclude it.
  If you are using multiple files or including headers above your top module, mark the top module like so:

```verilog
  (* top *)
  module my_top_module(
      output led_r,
      input serial_rxd,
  );
  ....
  endmodule
```
* Optionally, a testbench file ending in `_tb.v`. This file will be excluded by [apio build](https://github.com/FPGAwars/apio/wiki/Apio-Build), but become the main module for [apio sim](https://github.com/FPGAwars/apio/wiki/Apio-Sim).


-------
[![](https://github.com/FPGAwars/icestudio-wiki/raw/main/Logos/fgpawars-banner.svg)](https://fpgawars.github.io/)
