[![](https://github.com/FPGAwars/Apio-wiki/raw/main/wiki/Logos/apio-banner.svg)](https://github.com/FPGAwars/apio/wiki)

# Apio Project configuration file (apio.ini)

The `apio.ini` configuration file stores the Apio configuration for each project. The file is in 'ini' format with
all the attributes stored in the ```[env]``` section and is intended for manual editing by users. A minimal
```apio.ini``` file may look like

```ini
# Sample API configuration file.
[env]
board = upduino31
top-module = main
```



The current configuration parameters are:

| Section | Parameter    | Description |
| ------- | ------------ | ----------- |
| `env`   | `board`      | The board, chosen from the list of [apio boards](https://github.com/FPGAwars/apio/wiki/Apio-Boards)  |
| `env`   | `top-module` | The design Top module name | 



-------
[![](https://github.com/FPGAwars/icestudio-wiki/raw/main/Logos/fgpawars-banner.svg)](https://fpgawars.github.io/)
