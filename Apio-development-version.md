## Contents

* [Introduction](#introduction)  
* [Installation](#installation)  

## Introduction

Apio is being develop in [this github repo](https://github.com/FPGAwars/apio). There are two branches: **master** and **develop**. The stable version is locate in master. This is the versión that installed when you invoke the *pip install apio* command

The **development version** is **unstable** as it contains the latest features

## Installation

You can install the **latest development version** with the following command. Use it if you want to play with an FPGA board that is not yet supported in the stable version but it has experimental support in development

```
pip3 install -U git+https://github.com/FPGAwars/apio.git@develop#egg=apio
```
You need [git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git), as this command will clone the github repository and install it. Make sure you have it installed

## Development workflow

If you want to help with the develpment of apio and test your new features added follow these steps:

### Fork the apio repo in your account

Just fork the project by pressin on the **fork button** located in the top right corner

![](https://github.com/FPGAwars/apio/raw/develop/wiki/Apio-Development/development-01.png)

### Clone the repo

Clone the forked repo in your local computer. For example, as I am the user Obijuan, I should type this command:

```
$ git clone https://github.com/Obijuan/apio.git
```

### Enter the apio folder

Once it is cloned, enter into the apio directory

```
cd apio
```

These are the files and folders under apio:

```
$ ls 
apio          docs    LICENSE    setup.py  tox.ini
CHANGELOG.md  FAQ.md  README.md  test      wiki
```

### Install virtual-env

For developing apio it is better to use a **virtual python environment**, so that you are sure that there are no conflicts with the python packages in your system

You can install it very easily with these command on Linux:

```
sudo apt install python3-venv
```

### Create the APIO virtual env

You should create the APIO virtual env the first time. Just type this command

```
python3 -m venv APIO
```

It will create the APIO folder, with the virtual environment. All the python packages will be installed there