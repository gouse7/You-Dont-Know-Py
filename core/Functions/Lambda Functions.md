## Anonymous or Lambda Functions

### Definition

- Anonymous functions are functions that do not have an explicitly defined name.
- They are used to perform instant operations that are not needed elsewhere in the application or project.

### Features

- Anonymous functions are also called lambda functions because they use the keyword `lambda` to define them.
- Anonymous functions contain a single executable statement (but not multiple statements).
- They automatically return a value without needing a return statement.

### Syntax for Defining Anonymous Functions:

```python
varname = lambda params_list: statement
```

- `varname` represents an object of type `<class,'function'>`. It can be used as a function call.
- `lambda` is a keyword used for defining anonymous functions.
- `params_list` represents a list of variable names used for storing the inputs coming from function call.
- `statement` represents a single executable statement that gets executed, and its result is returned automatically by the PVM (no need to use a return statement).

### Defining a Function for Adding Two Numbers

```python
# By using Normal Functions
def sumop(a, b):
    c = a + b
    return c

# By using Anonymous Functions
addop = lambda a, b: a + b

# main program
res = sumop(10, 20)
print("sum=", res)

res = addop(100, 200)
print("sum=", res)
```