[![](https://github.com/FPGAwars/Apio-wiki/raw/main/wiki/Logos/apio-banner.svg)](https://github.com/FPGAwars/apio/wiki)

## Contents

* [Introduction](#introduction)  
* [Installation](#installation)  
* [Development workflow](#development-workflow)  
  * [Fork the apio repo in your account](#fork-the-apio-repo-in-your-account)  
  * [Clone the repo](#clone-the-repo)  
  * [Enter the apio folder](#enter-the-apio-folder)  
  * [Install virtual-env](#install-virtual-env)  
  * [Create the APIO virtual-env](#create-the-apio-virtual-env)  
  * [Activate the virtual environment](#activate-the-virtual-environment)  
  * [Install the Apio development version](#install-the-apio-development-version)  
  * [You are ready for developing!](#you-are-ready-for-developing)  
  * [Testing your contributions](#testing-your-contributions)  
  * [Emit a pull request](#emit-a-pull-request)  
  * [Deactivating the virtual environment](#deactivating-the-virtual-environment)

## Introduction

Apio is being develop in [this github repo](https://github.com/FPGAwars/apio). There are two branches: **master** and **develop**. The stable version is located in master. This is the versión that is installed when you invoke the *pip install apio* command

The **development version** is **unstable** as it contains the latest features

## Installation

You can install the **latest development version** with the following command. Use it if you want to play with an FPGA board that is not yet supported in the stable version but it has experimental support in development

* **Linux** and **Mac**:

```
sudo pip3 install -U git+https://github.com/FPGAwars/apio.git@develop#egg=apio
```
* **Windows**:
```
pip3 install -U git+https://github.com/FPGAwars/apio.git@develop#egg=apio
```

You need [git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git), as this command will clone the github repository and install it. Make sure you have it installed

## Development workflow

If you want to help with the develpment of apio and test your new features added follow these steps:

### Fork the apio repo in your account

Just fork the project by pressin on the **fork button** located in the top right corner

![](https://github.com/FPGAwars/Apio-wiki/raw/main/wiki/Apio-Development/development-01.png)


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
apio  LICENSE   pyproject.toml  test           tox.ini
docs  Makefile  README.md       test-examples
```

### Install virtual-env

For developing apio it is better to use a **virtual python environment**, so that you are sure that there are no conflicts with the python packages in your system

You can install it very easily with these command on Linux:

```
sudo apt install python3-venv
```

### Create the APIO virtual env

You should create the APIO virtual env the **first time**. Just type this command

```
python3 -m venv venv 
```

It will create the `venv` folder, with the virtual environment. All the python packages will be installed there

Make sure to upgrade all the python dependencies. Execute this command:

```
python3 -m venv venv --upgrade
```

### Activate the virtual environment

All the apio development **must** be done inside the virtual environment. Before executing apio we have to enter to this virtual environment

Execute the following command to access to the virtual environment:

```
. venv/bin/activate
```

Your terminal prompt will be changed. The `venv` word will apear at the begining:

```
(venv) $ 
```

All the **python packages** installed from now on will be installed only on this **virtual environment** and not in the system or user environment

### Install the dependencies for developing apio

Inside the virtual environment execute these commands:

```
python -m pip install --upgrade pip
```

It will upgrade the `pip` tool to the latest version

Install all the required tools:

```
pip install flit black flake8 pylint pytest
```

* [Flit](https://pypi.org/project/flit/): Create pypi packages easely
* [Black](https://pypi.org/project/black/): Python code formatter  
* [Flake8](https://pypi.org/project/flake8/): Lint 
* [Pylint](https://pypi.org/project/pylint/): Another lint  
* [Pytest](https://pypi.org/project/pytest/): Environment for executing the tests   

### Executing apio development version

For running `apio` just execute this command:

```
flit install
```

It will create a **local apio package** from the sources and **install** it in your virtual environment

Now you can invoke `apio` normally

### You are ready for developing!

Now you can start adding features to apio: new boards, new documentation,  bug fixing... Just edit the python files with your favorite IDE

Everytime you want to test something, just execute this command from the apio top folder, inside the virtual env:

```
flit install
```

and then execute the apio commands/actions you want to test

### Testing your contributions

Once you have finished your contribution (a bug fixed, a feature or whatever) you should test that everything is ok.

Execute the following commands:

```
black apio
```

It will automatically format the files you've changed, so that the code always maintan the same style (regardless of the contributor)

```
flake8 apio
```
This is a linter, for static analysis of your code

```
pylint apio
```
Another linter that assign a code score to your code. Make sure your score is 10/10!

```
pytest apio test
```

It run a battery of tests, for checking that your contribution has not broken Apio behaviour


### Emit a pull request

Now you are ready to do a pull request to apio. Thanks for your contribution!

### Deactivating the virtual environment

You can leave the virtual environment anytime executing this command:

```
deactivate
```

-------
[![](https://github.com/FPGAwars/icestudio-wiki/raw/main/Logos/fgpawars-banner.svg)](https://fpgawars.github.io/)
