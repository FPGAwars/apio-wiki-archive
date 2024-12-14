[![](https://github.com/FPGAwars/Apio-wiki/raw/main/wiki/Logos/apio-banner.svg)](https://github.com/FPGAwars/apio/wiki)

**TODO:** Update the table of content (how?)

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
  * [Executing Apio development version](#executing-apio-development-version)   
  * [You are ready for developing!](#you-are-ready-for-developing)  
  * [Testing your contributions](#testing-your-contributions)  
  * [Emit a pull request](#emit-a-pull-request)  
  * [Deactivating the virtual environment](#deactivating-the-virtual-environment)


***

## Trying the latest apio version

This document describes the setup of the apio development environment. However, if all you want is to try the latest apio development version you can install it directly using the commands below. Please be aware that the development version may be **unstable** since it's a work in progress.

A quick trial of the latest apio development package.
```
# Delete the .apio directory under the user home page. On windows, use the Explorer window to delete it.
rm -rf ~/.apio

# Install the apio pip package.
pip install --force-reinstall -U git+https://github.com/FPGAwars/apio.git@develop#egg=apio 

# Install the apio packages.
apio packages --install
```

***


## Setting up a basic apio development environment.

If your goal is to change and apio code and possibly sending 'pull requests' to the apio team, the instructions below will help you to setup a development environment. The development can be done on Linux, Mac OSX, and Windows computers.


### Fork the apio repo in your github account

Just fork the project by pressing on the **fork button** located in the top right corner

![](https://github.com/FPGAwars/Apio-wiki/raw/main/wiki/Apio-Development/development-01.png)


### Clone the repo on your local computer. 

Clone the forked repo in your local computer. For example, as I am the user Obijuan on github, I should type this command the command below. This will create in the current directory a new directory called ``apio-repo`` with the content of the apio repo.

```
git clone -b develope https://github.com/Obijuan/apio.git apio-repo
```

### Enter the apio-repo folder

Once it is cloned, enter into the apio directory

```
cd apio-repo
```

The list of files will look similar to this:

```
DEVELOPERS.md	Makefile	apio		pyproject.toml	test		test-examples
LICENSE		README.md	apio_run.py	scons_run.py	test-boards	tox.ini
```

### Install the repository as the python ``apio`` package.

While in the ``apio-repo`` directory, run the command below to install its content as the pip ``apio`` package. This will allow you tests you make to the apio code by simply running the ``apio`` command.

NOTE: Pip is safe and will not modify the content of ``apio-repo``, even if you will later run ``pip uninstall apio``.

```
pip install --force-reinstall -U --editable .

```

You can verify the location of pip's apio package by typing

```
pip show apio
```

### Factory reset apio's state

This step delete any left-over state and packages from previous apio installations. Simply delete the ``.apio`` directory from your user home directory on your computer. 

```
# On linux and Mac OSX.
rm -rf ~/.apio

# On windows, delete the .apio directory using the Windows Explorer.
```

### Install apio packages

This will install the apio managed packages such as the YosysHQ verilog toolchain.

```
apio packages --install
```

Apio should not be read for use, and any changes you make in the ``apio-repo`` code will be reflected when you run the ``apio`` command.


***

## Advanced apio development environment setup

### Install virtual-env

For developing apio it may be useful to use a  **virtual python environment**, so that you are sure that there are no conflicts with the python packages in your system

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
source venv/bin/activate
```

Your terminal prompt will be changed. The `venv` word will apear at the begining:

```
(venv) $ 
```

All the **python packages** installed from now on will be installed only on this **virtual environment** and not in the system or user environment


***


## Testing your contributions

Once you have finished your contribution (a bug fixed, a feature or whatever) you should test that everything is ok.

Make sure that the python tox package is installed

```
pip install tox.

```

And then run the tests in from the ``apio-repo`` directory

```
make check
```

NOTE: For other useful ``make`` targets see the file ``apio-repo/Makefile``.


NOTE: If your system doesn't have the ``make`` command you will need to install it.

**TODO:** How to install ``make``.


***

## Send a pull request

Now you are ready to do a pull request to apio. Thanks for your contribution!


-------
[![](https://github.com/FPGAwars/icestudio-wiki/raw/main/Logos/fgpawars-banner.svg)](https://fpgawars.github.io/)
