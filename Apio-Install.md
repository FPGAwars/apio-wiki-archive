# Contents
  * [Usage](#usage)  
  * [Description](#description)


# Usage

```bash
apio install [OPTIONS] [PACKAGES]
```

# Description

**Install** apio packages. By default it installs the **latest stable version**. Other versions can be installed using the following notation: `package@version`  (Ex. `oss-cad-suite@0.0.8`)  

# Options

| Flag | Long Flag | Description |
| ---- | --------- | ----------- |
| `-a` | `--all`   | Install all packages |
| `-l` | `--list`  | List all available packages |
| `-f` | `--force` | Force the packages installation |
| `-p` | `--platform` | Set the platform [linux, linux_x86_64, linux_i686, linux_armv7l, linux_aarch64, windows, windows_amd64, windows_x86, darwin] (Advanced) |

