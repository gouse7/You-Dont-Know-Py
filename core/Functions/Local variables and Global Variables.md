
## Local Variables

The variables used inside the function body are called local variables. The purpose of local variables is to store temporary results.

### Syntax

```python
def functionname(list of formal Params if any):
    var1 = val1
    var2 = val2
    .
    .
    .
    var-n = val-n
```

Here, `var1`, `var2`, ... `var-n` are called local variables.

## Global Variables

Global variables are those which have common values for different function calls. In other words, if the value is common for all different function calls, then such type of values must be taken as global variables. To access the values of global variables, they must be defined before function calls only otherwise we get a `NameError`.

### Syntax

```python
var1 = val1
var2 = val2
.
.
.
var-n = val-n

def fun1():
    .
    .
    .

def fun2():
    .
    .
    .

def fun-n():
    .
    .
    .
```

Here, `var1`, `var2`, ... `var-n` are called global variables and we can access those values inside of `fun1()`, `fun2()`, ... `fun-n()`.

## Global Keyword

When we want to modify the global variable values inside of a function definition, then global variable names must be preceded with the `global` keyword; otherwise, we get an `UnboundLocalError: local variable names referenced before assignment`.

### Syntax

```python
var1 = val1
var2 = val2
.
.
.
var-n = val-n    # var1, var2, ... var-n are called global variable names.

def fun1():
    .
    .
    .
    global var1, var2, ... var-n
    # Modify var1, var2, ... var-n
    .
    .
    .

def fun2():
    .
    .
    .
    global var1, var2, ... var-n
    # Modify var1, var2, ... var-n
    .
    .
    .
```

Here, `var1`, `var2`, ... `var-n` are called global variable names. We can modify these global variables inside the function definition by using the `global` keyword.

## `globals()`

When we come across the same global variable names and local variable names in the same function definition, then PVM gives preference to local variables but not for global variables.

In this context, to extract/retrieve the values of global variable names along with local variables, we must use `globals()`, and it returns an object of `<class, 'dict'>`, and this dict object stores all global variable names as keys and global variable values as values of value.

### Syntax

```python
var1 = val1
var2 = val2
.
.
.
var-n = val-n  # var1, var2, ... var-n are called global Variables

def functionname():
    var1 = val11
    var2 = val22
    .
    .
    .
    var-n = val-nn  # var1, var2, ... var-n are called local Variables
    # Extract the global variables values
    dictobj = globals()
    globalval1 = dictobj['var1']  # or dictobj.get("var1") or globals()['var1'] or global().get('var1')
    globalval2 = dictobj['var2']  # or dictobj.get("var2") or globals()['var2']
    .
    .
    .
```

Here, `var1`, `var2`, ... `var-n` are called global variables, and `var1`, `var2`, ... `var-n` are called local variables.

### Examples:

```python
# globalsfunex3.py

a = 10
b = 20
c = 30
d = 40

def operations():
    obj = globals()
    for gvn, gvv in obj.items():
        print("\t{}---->{}".format(gvn, gvv))
    print("=" * 50)
    print("\nProgrammer-defined Global Variables")
    print("=" * 50)
    print("Val of a=", obj['a'])
    print("Val of b=", obj['b'])
    print("Val of c=", obj['c'])
    print("Val of d=", obj['d'])
    print("=" * 50)
    print("\nProgrammer-defined Global Variables")
    print("=" * 50)
    print("Val of a=", obj.get('a'))
    print("Val of b=", obj.get('b'))
    print("Val of c=", obj.get('c'))
    print("Val of d=", obj.get('d'))
    print("=" * 50)
    print("\nProgrammer-defined Global Variables")
    print("=" * 50)
    print("Val of a=", globals().get('a'))
    print("Val of b=", globals().get('b'))
    print("Val of c=", globals().get('c'))
    print("Val of d=", globals().get('d'))
    print("=" * 50)
    print("\nProgrammer-defined Global Variables")
    print("=" * 50)
    print("Val of a=", globals()['a'])
    print("Val of b=", globals()['b'])
    print("Val of c=", globals()['c'])
    print("Val of d=", globals()['d'])
    print("=" * 50)

# main program
operations()
```

```python
# globalsfunex2.py

a = 10
b = 20
c = 30
d = 40    # Here a, b, c, d are called Global Variables.

def operation():
    a = 100
    b = 200
    c = 300
    d = 400    # Here a, b, c, d are called Local Variables.
    res = a + b + c + d + globals()['a'] + globals().get('b') + globals()['c'] + globals()['d']
    print(res)

# main program
operation()
```

In the first example (`globalsfunex3.py`), we have defined global variables `a`, `b`, `c`, and `d`, and then we have defined a function `operations()` that retrieves the values of these global variables using the `globals()` function. We are using different methods to retrieve the values of these global variables, such as `obj['a']`, `obj.get('a')`, and `globals().get('a')`.

In the second example (`globalsfunex2.py`), we have defined global variables `a`, `b`, `c`, and `d`, and then we have defined a function `operation()` that defines local variables with the same names as the global variables. Inside the function, we are calculating the sum of the local variables and the global variables using the `globals()` function. We are accessing the values of the global variables using `globals()['a']`, `globals().get('b')`, etc.