

## Functions
- Used for performing some operation and provides code re-usability within the same program.
- Unable to provide code re-usability across programs.

## Modules
- A collection of variables, functions, and classes.
- Can re-use the code across the programs provided module name and main program present in the same folder.
- Unable to provide code re-usability across folders / drives / environments.

## Package
- A collection of modules.
- Provides code re-usability across folders / drives / environments.

### To deal with the package, we need to learn the following:
- 1. Create a package
- 2. Re-use the package

## 1) Create a package:
### Steps to create a package:
1. Create a folder.
2. Place / write an empty Python file called `__init__.py` (Optional).
3. Place / write the module(s) in the folder where it is considered as the package name.

### Example:
```
bank           <-----Package Name
-----------
    __init__.py    <----Empty Python File
    simpleint.py  <--- Module Name
    aop.py-----Module Name
    icici1.py---Module Name
    welcome.py  <--- Module Name
    greet.py<--- Module Name
```

## 2) Re-use the package
### Approaches to re-use the modules of the package across the folders / drives / environments:
1. By using `sys` module.
2. By using `PYTHONPATH` environmental variable name.

### i) By using `sys` module:
#### Syntax:
```
sys.path.append("Absolute Path of Package")
```
- `sys` is a pre-defined module.
- `path` is a pre-defined object of a list / variable present in the `sys` module.
- `append()` is a pre-defined function present in `path` and is used for locating the package name of Python (specify the absolute path).

#### Example:
```python
sys.path.append("D:\\KVR-PYTHON-6pm\\PACKAGES\\BANK")
```

### ii) By using `PYTHONPATH` environmental variables:
- `PYTHONPATH` is one of the environmental variables.
- Search for environmental variables.
#### Steps for setting:
- Variable name: `PYTHONPATH`
- Variable value: `D:\\KVR-PYTHON-11am\\PACKAGES\\BANK`

#### The overall path:
```
PYTHONPATH= D:\\KVR-PYTHON-11am\\PACKAGES\\BANK
```