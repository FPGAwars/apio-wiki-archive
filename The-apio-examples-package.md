The apio package with **all the examples** is called **apio-examples** and it is located in this repo: [apio-examples](https://github.com/FPGAwars/apio-examples). This package can be **installed** by means of the **apio install examples** command

For **adding new examples** follow these steps:

1. **Fork** the [apio-examples](https://github.com/FPGAwars/apio-examples) repo and then **clone** it
2. Enter in the board folder. If the board does not exist yet, create a new folder named as the board
3. Create a new folder for the example
4. Every example should have at least 4 files:
 * info: It is a text file with a single line with the description of the example. Is the messages displayed whith the command apio example -l for listing all the examples
 * apio.ini: Apio project file. It is created with the command apio --inti -b boardname
 * A .pcf file: The constaint file with association between the top module ports and the FPGA pins
 * At least one verilog file (.v)
