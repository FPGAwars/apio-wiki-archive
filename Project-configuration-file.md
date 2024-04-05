[![](https://github.com/FPGAwars/Apio-wiki/raw/main/wiki/Logos/apio-banner.svg)](https://github.com/FPGAwars/apio/wiki)

# Apio Project configuration file (apio.ini)

The `apio.ini` configuration file stores the Apio configuration for each project. The file is in 'ini' format with
all the attributes stored in the `[env]` section and is intended for manual editing by users. A minimal
`apio.ini` file may look like

```ini
# Comment line.
[env]
board = alhambra-ii
top-module = main
```

The supported configuration attributes are:

---

## board

Type: `String` | Required: `Yes` | Default: `none`

The ID of the supported board model. The list supported boards is available [apio boards](https://github.com/FPGAwars/apio/wiki/Apio-Boards) or by running the command `apio boards --list`.

Example:
```ini
board = upduino31
```
> [!NOTE]
**NOTE:** Some APIO commands allow to override the `board` setting using the `--board` command line flag. 
```shell
apio build --board upduino31
```
---

## exe-mode

Type: `String` | Required: `No` | Default: `default`

Specifies the **execution mode** of the project build. The valid values are `default` and `native`.

The `default` behaviour of apio is to run the toolchains that were installed from apio packages (Ex. apio install oss-cad-suite). It is the easiest choice for a normal user: let apio install and manage the executables

But it is also possible (`native` mode) to let apio execute the installed toolchains in the system. In this case, is the user (advanced) who should install all the toolchains needed. Apio will find them if they are in system PATH 


Example:
```ini
exe-mode = native
```

---

## top-module

Type: `String` | Required: `No` | Default: `main`

The name of the Verilog module to be used as top module when building the project. Not that this is the name as it appears in the verilog `module` statement such as `module main` and not a file name such as `main.v`.

Example:
```ini
top-module = main
```
> [!NOTE]
**NOTE:** Some APIO commands allow to override the `top-module` setting using the `--top-module` command line flag. 

```shell
apio build --top-module my_top-module
```


-------
[![](https://github.com/FPGAwars/icestudio-wiki/raw/main/Logos/fgpawars-banner.svg)](https://fpgawars.github.io/)
