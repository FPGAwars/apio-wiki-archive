[![](https://github.com/FPGAwars/Apio-wiki/raw/main/wiki/Logos/apio-banner.svg)](https://github.com/FPGAwars/apio/wiki)

# Contents
  * [Usage](#usage)  
  * [Description](#description)  
  * [Options](#options)
  * [Examples](#examples)  

# Usage

```bash
apio init [OPTIONS]
```

# Description

Manage apio projects. In addition to the code, an apio project may include a configuration file **apio.ini** and a Scons script **SConstruct**.

# Options

| Flag | Long Flag | Description |
| ---- | --------- | ----------- |
| `-s` | `--scons` | Create a default SConstruct file. This file can be modified and it will be used instead of the default script |
| `-b` | `--board`  | Create a configuration file with the selected board. This will be the default board used by the commands `build`, `upload` and others |
| `-p` | `--project-dir` | Set the target directory for the project |
| `-y` | `--sayyes`  | Automatically answer YES to all the questions |


# Examples

## 1. Create a SConstruct file

```bash
apio init --scons
```

![]()  

## 2. Create an apio.ini file with the icezum board

```bash
```

![]() 

-------
[![](https://github.com/FPGAwars/icestudio-wiki/raw/main/Logos/fgpawars-banner.svg)](https://fpgawars.github.io/)
