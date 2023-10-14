[![](https://github.com/FPGAwars/Apio-wiki/raw/main/wiki/Logos/apio-banner.svg)](https://github.com/FPGAwars/apio/wiki)

Information for developers

For releasing a new stable apio version, follow these steps:

* **Merge** the Apio **develop** branch into **Master**
* Change the version in the file `apio/__init__.py`
```python
VERSION = (0, 7, 4)
```
* Change the `packages.json` file. Make sure it has the `VERSION` file in the `url_version` attribute:  
```
"url_version": "https://github.com/FPGAwars/tools-oss-cad-suite/raw/main/VERSION_DEV"
```
* Create a new Release from Github. It should start with the letter `v` followed by the version number. Add the changes from the previous release

Example:
```
v0.7.4
```

* **Publish the release** from github

* **Execute manually** the Github-action: **Publish Pypi**. Go to the [Actions menu](https://github.com/FPGAwars/apio/actions), select **Publish Pypi** and Run the workflow on the **master** branch

![](https://github.com/FPGAwars/Apio-wiki/raw/main/wiki/Releasing-stable-version/github-action-1.png)

* The new version will be available in the pypi repo: [Apio in pypi repo](https://pypi.org/project/apio/)  

* Install the new package in your system (globaly):

```
$ sudo pip3 install apio==0.7.4
```

* Check the new version:

```
$  apio --version
apio, version 0.7.4
```

-------
[![](https://github.com/FPGAwars/icestudio-wiki/raw/main/Logos/fgpawars-banner.svg)](https://fpgawars.github.io/)