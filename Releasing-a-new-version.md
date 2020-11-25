Information for developers

For releasing a new stable apio version, follow these steps:

* **Merge** the Apio **develop** branch into **Master**
* Change the version in the file apio/__init__.py
```python
VERSION = (0, 6, "rc2")
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

* You have to type "__token__" as the username and then paste your token

```
Uploading distributions to https://upload.pypi.org/legacy/
Enter your username: __token__
Enter your password: 
Uploading apio-0.6rc2-py3-none-any.whl
100%|████████████████████████████████████████████████| 77.1k/77.1k [00:01<00:00, 49.1kB/s]
Uploading apio-0.6rc2.tar.gz
100%|████████████████████████████████████████████████| 55.7k/55.7k [00:01<00:00, 44.1kB/s]

View at:
https://pypi.org/project/apio/0.6rc2/
```
You will see your new packages in this URL: https://pypi.org/project/apio/0.6rc2/ (for this example)

* Install the new package in your system (globaly):

```
$ sudo pip3 install apio==0.6rc2
```

* Check the new version:

```
$  apio --version
apio, version 0.6rc2
```

