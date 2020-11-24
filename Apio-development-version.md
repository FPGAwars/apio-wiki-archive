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

Apio is being develop in [this github repo](https://github.com/FPGAwars/apio). There are two branches: **master** and **develop**. The stable version is locate in master. This is the versión that installed when you invoke the *pip install apio* command

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

### Activate the virtual environment

Execute the following command to access to the virtual environment:

```
$ source APIO/bin/activate
```

Your terminal prompt will be changed. The APIO will apear at the begining:

```
(APIO) $ 
```

All the **python packages** installed from now on will be installed only on this **virtual environment** and not in the system or user environment

### Install the apio development version

Just execute this command. It will install the apio version you have previously cloned

```
(APIO)$ pip install -U .
```

You can check that everything was ok executing this command:

```
(APIO)$ apio --version
apio, version 0.5.5
```

It will display the current development version

Everytime you change something in the apio sources and you want to test it you have to "pip install -U ." it 

In addition, you should install the [tox python package](https://tox.readthedocs.io/en/latest/):

```
pip install tox pytest-mccabe pytest pytest-flakes pytest-cov
```
It is used for performing test, and making sure that the new apio package will install correctly on different environments

### You are ready for developing!

Now you can start adding features to apio: new boards, new documentation,  bug fixing... Just edit the python files with your favorite IDE

Everytime you want to test something, just execute this command from the apio top folder:

```
(APIO)$ pip install -U .
```

and then execute the apio commands/actions you want to test

### Testing your contributions

Once you have finished your contribution (a bug fixed, a feature or whatever) you should test that everything is ok.

* Install tox:

```
pip install tox
```

* Check your code: 

```
(APIO) $ tox
```

After some time, it will finish and you will see this information on the console:

```
[...]
============= 166 passed, 38 warnings in 6.89s ===================
_______________________ summary __________________________________
  py38: commands succeeded
  congratulations :)
```

### Emit a pull request

Now you are ready to do a pull request to apio. Thanks for your contribution!

### Deactivating the virtual environment

You can leave the virtual environment anytime executing this command:

```
(APIO) $ deactivate
$
```

Notice how the APIO prefix is no longer printed

