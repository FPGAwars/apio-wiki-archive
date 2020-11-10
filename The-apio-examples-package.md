The apio package with **all the examples** is called **apio-examples** and it is located in this repo: [apio-examples](https://github.com/FPGAwars/apio-examples). This package can be **installed** by means of the **apio install examples** command

For **adding new examples** follow these steps:

## Fork the apio-examples github repo

**Fork** the [apio-examples](https://github.com/FPGAwars/apio-examples) repo and then **clone** it

![](https://github.com/FPGAwars/apio/raw/develop/wiki/Adding-examples/apio-examples-pkg-01.png)

## 2. Select the board folder

Once the repo is cloned, enter into the apio-examples folder

![](https://github.com/FPGAwars/apio/raw/develop/wiki/Adding-examples/apio-examples-pkg-02.png)

There you will see many folder with the names of the **supported boards**. Find the board you want to use for your example and enter into that folder. If your board does not exist yet, create a new folder with that name

## 3. Select the example folder

Inside your board folder you will find more folders with the names of the examples. Select the example you want to modify or creat a new folder if it is a new example

In this screenshot you can see that there are **three examples** inside the folder **Alhambra-II**

![](https://github.com/FPGAwars/apio/raw/develop/wiki/Adding-examples/apio-examples-pkg-03.png)

## 4. Files in the example folder

Inside the **example folder** there should be at least **four files**:

![](https://github.com/FPGAwars/apio/raw/develop/wiki/Adding-examples/apio-examples-pkg-04.png)

|  File        | Description |
|--------------|-------------|
| **info**     | Text file with a single line with the description of the example. Is the messages displayed with the command *apio example -l* when listing all the examples |
| **apio.ini** | Apio project file. It is created with the command *apio --init -b boardname*
| .pcf         | The **constaint file** with associations between the top module ports and the FPGA pins |
| .v           | One or more verilog files |
