Information for developers

For releasing a new stable apio version, follow these steps:

* **Merge** the Apio **develop** branch into **Master**
* Change the version in the file apio/__init__.py
```python
VERSION = (0, 5, "6rc1")
```
* Open a terminal at the project top foler (where the setup.py file is locate)

```
obijuan@corellia:~/Develop/FPGAwars/apio$
```

* Clean previous generated packages. This is very important, as **ALL** the packages inside the `dist` folder will be uploaded

```
rm dist/*
```

* **Generate** the package for your current version. The files will be stored in the `dist` folder

```
python3 setup.py sdist bdist_wheel
```

* **Upload** the new package:

```
python3 -m twine upload dist/*
```

TODO