Information for developers

For releasing a new stable apio version, follow these steps:

* **Merge** the Apio **develop** branch into **Master**
* Change the version in the file apio/__init__.py
```python
VERSION = (0, 5, "6rc1")
```
* Execute the following command from the project top folder (where the setup.py file is located)

```
python3 setup.py sdist bdist_wheel
```

TODO