![](https://github.com/FPGAwars/apio/raw/develop/wiki/Quick-start/apio.jpg)

## What is Apio?

Apio is a **multiplatform** toolbox with **static** pre-built packages to verify, synthesize, simulate and upload your verilog designs into the supported **FPGA boards**

## What??????

Apio makes **extremelly easy** the process of working with **FPGAs**. Go from **scratch** to having a **blinky LED** in your FPGA board in minutes! This is because it is based only on **Free/Libre Open Source Software** (FLOSS). Just install it and use it as you want

![](https://github.com/FPGAwars/apio/raw/develop/wiki/Quick-start/apio-alhambra-II-01.gif)

Think of Apio as a small **FPGA distribution**, which **collects** and **packages** **FLOSS toolchains for FPGAs**. You can install packages in **Linux**, **Mac** and **Windows** for synthesizing hardware, verifying and simulating from verilog files

The goal is making it **very easy** to start with FPGAs

Apio has a **command line interface** (CLI). It is the **building block** for other **higher level tools**, like [Icestudio](https://icestudio.io/), [Apio-IDE](https://github.com/FPGAwars/apio-ide) or working with FPGAs from IDEs such as [Visual Studio Code](https://code.visualstudio.com/)

(Icestudio screenshot)  
(Apio ide screenshot)  
(Visual studio code screenshot)  

As the user **gh02t** said in this post on [Hacker-news](https://news.ycombinator.com/item?id=17912510):
> Apio is a command line tool that automates installing the toolchain for your FPGA and running it. It just simplifies things, you don't have to use it if you'd rather call the individual tools for synthesis, P&R, simulation etc. It'd be reasonable to think of it as akin to a very smart Makefile combined with an automatic package manager, specialized to FPGAs (it's based on PlatformIO). It's nice when you're still kind of getting oriented, because you don't need to know how to set up and invoke the different tools... just call `apio build` or `apio simulate`
