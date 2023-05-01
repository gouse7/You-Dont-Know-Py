

There 4 types of function arguments and parameters

# 1. Positional Arguments
# 2. Keyword Arguments
# 3. Default Arguments
These are used to provide default values for parameters in case the user does not provide them when calling the function. 
Default arguments are optional
They are defined using the equal sign after the parameter name

```python
def print_name(first_name, last_name="Doe"):
    print(f"Hello {first_name} {last_name}!")

print_name(first_name="John")

```

# 4. Variable-length Parameters
### Positional variable-length parameters
-   A way to define a single function that can handle multiple function calls with variable numbers of values/arguments.
-   This approach saves development time as we don't need to define multiple function definitions.
-   To implement variable length parameters, we define a single function definition that takes a formal parameter preceded with a symbol called an asterisk (`*param`).
-   The formal parameter with an asterisk symbol is called a variable length parameter and can hold any number of argument values.
-   The type of a variable length parameter is `tuple`.
-   The `*param` must always be written at the end of the function heading and there should only be one.
-   When using variable length and default parameters in function heading, the default parameter should be written last, and the variable length parameter should be written before it.
-   In function calls, we should not use default parameter as a keyword argument because variable number of values are treated as positional argument value(s).

#### Syntax for function definition with variable length parameters:

```python
def functionname(list of formal params, *param1, param2=value):
```

##### \*args
This is used to pass a variable number of positional arguments to a function
\*args type is tuple, it contains all the arguments that are pass

```python

def add_numbers(*args): #args = (1,2,3,4,5) 
	sum = 0 
	for num in args:
		sum += num 
	return sum 
	
add_numbers(1, 2, 3, 4, 5)

```
#### Pitfalls

-   If the function definition contains multiple formal parameters before the variable length parameter, we need to pass values for those parameters before passing values for the variable length parameter. Otherwise, Python will raise a TypeError.
-   It is important to keep in mind that the values passed to the variable length parameter are treated as positional arguments, and not keyword arguments. Therefore, we cannot use keyword arguments for the values passed to the variable length parameter.

#### Example

Suppose we want to create a function to calculate the sum of any number of integers. We can define the function using variable length parameters as follows:
```python

def calculate_sum(*args):
    total = 0
    for num in args:
        total += num
    return total


result = calculate_sum(1, 2, 3, 4, 5)
print(result)   # Output: 15

result = calculate_sum(1, 2, 3)
print(result)   # Output: 6

result = calculate_sum(10, 20, 30, 40, 50, 60)
print(result)   # Output: 210
```
In this way, we can use variable length parameters to create flexible functions that can handle different numbers of arguments without the need to define multiple function definitions.

### Keywords Arguments with Variable Length Parameters
-   When we have multiple function calls with a variable number of keyword arguments, defining multiple function definitions can lead to more development time.
-   To overcome this process, we can use the concept of keyword variable length parameters.
-   To implement keyword variable length parameters, we must define a single function definition and take a formal parameter preceded by a double asterisk symbol (i.e., **param).
-   The formal parameter with a double asterisk symbol is called keyword variable length parameters and is used to hold any number of (key, value) pairs coming from similar function calls, and its type is `<class, 'dict'>`.
#### Syntax for Function Definition with Keyword Variables Length Parameters:

```python
def print_person_info(**kwargs):
    print(f"Name: {kwargs['name']}")
    print(f"Age: {kwargs['age']}")
    print(f"Location: {kwargs['location']}")

person_info = {"name": "John", "age": 30, "location": "New York"}
print_person_info(**person_info)

```
#### Pitfalls
-   Be careful when using default parameters and keyword variable length parameters in the same function definition. The default parameter should always be before the keyword variable length parameter in the function header, and in function calls, we should not use the default parameter as a keyword argument because variable numbers of values are treated as positional argument values.
    
-   When using keyword arguments with variable length parameters, make sure that you don't pass the same key more than once, as this will result in a TypeError. The reason is that keyword variable length parameters store their arguments in a dictionary, and a dictionary can only have one value for each key.
    
-   Be careful with the order of the arguments when calling a function with both keyword and variable length parameters. The positional arguments should come first, followed by any keyword arguments, and then the variable length arguments.
    
-   Avoid using a variable length parameter as the only parameter in a function definition, as it can make the function hard to read and maintain. It is best to use a combination of positional and keyword arguments with variable length parameters for maximum flexibility and readability.
    
-   Finally, be aware that using too many keyword arguments and variable length parameters can make your code more complex and harder to understand. Use them judiciously and only when necessary to keep your code clean and easy to maintain.
#### Example

```python
def calculate_total_price(base_price, **fees):
    total = base_price
    for fee in fees.values():
        total += fee
    return total

# call function with keyword arguments
total_price = calculate_total_price(100, tax=10, service_charge=20, delivery=5)
print(total_price) # 135

```

