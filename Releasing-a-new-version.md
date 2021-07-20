[![](https://github.com/FPGAwars/Apio-wiki/raw/main/wiki/Logos/apio-banner.svg)](https://github.com/FPGAwars/apio/wiki)

Information for developers

For releasing a new stable apio version, follow these steps:

* **Merge** the Apio **develop** branch into **Master**
* Change the version in the file `apio/__init__.py`
```python
VERSION = (0, 7, 3)
```
* Create a new Release from Github. It should start with the letter `v` followed by the version number. Add the changes from the previous release

Example:
```
v0.7.3
```

* Publish the release from github. It will trigger a github action that automatically upload the package to pypi  

* The new version will be available in the pypi repo: [Apio in pypi repo](https://pypi.org/project/apio/)  

* Install the new package in your system (globaly):

```
$ sudo pip3 install apio==0.7.3
```

* Check the new version:

```
$  apio --version
apio, version 0.7.3
```

-------
[![](https://github.com/FPGAwars/icestudio-wiki/raw/main/Logos/fgpawars-banner.svg)](https://fpgawars.github.io/)