[![](https://github.com/FPGAwars/apio/raw/master/wiki/Logos/apio-banner.svg)](https://github.com/FPGAwars/apio/wiki)

The apio package with **all the examples** is called **apio-examples** and it is located in this repo: [apio-examples](https://github.com/FPGAwars/apio-examples). This package can be **installed** by means of the `apio install examples` command

# How to add new examples

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

## 5. Emiting a pull request

Once your example is ready **emit a pull request** for merging it with the upstream examples. In the next release cycle a new apio-exemples package will be ready with your new shiny example

# Releasing a new package version

This operation can only be done for those developers with **enough permissions** granted  
Once a **new version** of the apio-example package is **released** it could be installed easily from apio with the command *apio install examples*  
For releasing a new version follow these steps:

## 1. Create a new release

Choose a tag of the form x.y.z, where x,y and z are numbers. For example 0.0.18. Use the same tag as the number and add the description explaining what is new in this release

![](https://github.com/FPGAwars/apio/raw/develop/wiki/Adding-examples/apio-examples-pkg-05.png)

Then press the new release button. You will get something like this:

![](https://github.com/FPGAwars/apio/raw/develop/wiki/Adding-examples/apio-examples-pkg-06.png)

## 2. Download the Source .zip file

Click on the source code (zip) link for downloading the packages

![](https://github.com/FPGAwars/apio/raw/develop/wiki/Adding-examples/apio-examples-pkg-07.png)

You should get the file **apio-examples-x.y.z.zip** in your download folder

![](https://github.com/FPGAwars/apio/raw/develop/wiki/Adding-examples/apio-examples-pkg-08.png)

## 3. Upload the file to the new release

Press the **Edit release** button and attach the release file (apio-examples-x.y.z.zip). Make sure that it has exactly that format

![](https://github.com/FPGAwars/apio/raw/develop/wiki/Adding-examples/apio-examples-pkg-09.png)

Press the **Update release** button

This is how the new release should look like. Make sure that the new file appers as part of the release, with the correct format:

![](https://github.com/FPGAwars/apio/raw/develop/wiki/Adding-examples/apio-examples-pkg-10.png)

## 4. Check: Install the new apio-example package from apio

If you execute the **apio examples -l** command, you will see the list of current installed packages. In my case, i have the previous apio-examples version intalled

Type the **apio install examples** command and the new version will be automatically downloaded and installed. Ready for use

![](https://github.com/FPGAwars/apio/raw/develop/wiki/Adding-examples/apio-examples-pkg-11.png)

Once installed, you can check it with the **apio examples -l**. It should display the new package verion:

![](https://github.com/FPGAwars/apio/raw/develop/wiki/Adding-examples/apio-examples-pkg-12.png)

## 5. Test the new example

Now that the examples are installed, you can use them with the **apio example** commands. You can read more information in this section: [Downloading the Blinky example](https://github.com/FPGAwars/apio/wiki/Downloading-the-Blinky-example)

-------
[![](https://github.com/FPGAwars/icestudio-wiki/raw/main/Logos/fgpawars-banner.svg)](https://fpgawars.github.io/)