The apio package with **all the examples** is called **apio-examples** and it is located in this repo: [apio-examples](https://github.com/FPGAwars/apio-examples). This package can be **installed** by means of the **apio install examples** command

For **adding new examples** follow these steps:

## Fork the apio-examples github repo

**Fork** the [apio-examples](https://github.com/FPGAwars/apio-examples) repo and then **clone** it

![](https://github.com/FPGAwars/apio/raw/develop/wiki/Adding-examples/apio-examples-pkg-01.png)

## 2. Select the board folder

Once the repo is cloned, enter into the apio-examples folder

![](https://github.com/FPGAwars/apio/raw/develop/wiki/Adding-examples/apio-examples-pkg-02.png)

There you will see many folder with the names of the **supported boards**. Find the board you want to use for your example and enter into that folder. If your board does not exist yet, create a new folder with that name


3. Create a new folder for the example
4. Every example should have at least 4 files:
 * info: It is a text file with a single line with the description of the example. Is the messages displayed whith the command apio example -l for listing all the examples
 * apio.ini: Apio project file. It is created with the command apio --inti -b boardname
 * A .pcf file: The constaint file with association between the top module ports and the FPGA pins
 * At least one verilog file (.v)
