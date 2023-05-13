
<aside> 😎 **Functions in Python** Functions are used to encapsulate reusable code that can be called from other parts of a program. They allow you to break up a large program into smaller, more manageable parts, making your code easier to read, understand, and maintain.

</aside>

# 1. Function Definition and Calling

>[!Intro] Defining a Function
The **`def`** keyword is used to define the function.


**Syntax:**

```python
def function_name(parameters):
    # code block (indented)
    return value #not mandatory if function does not return anything

def greet(name):
    print(f"Hello, {name}!")
```

**Simple Example:**

```python
def greet(name):
    """
    This is a docstring that explains what the function does.
    In this case, it takes a name argument and prints a greeting.
    """
    print(f"Hello, {name}!")

# This is the function definition, which starts with the "def" keyword.
# "greet" is the name of the function.
# "name" is the parameter that the function takes. It's enclosed in parentheses.
# The colon at the end of the first line indicates that the function definition is starting.

# The docstring is a triple-quoted string that explains what the function does.
# It's not required, but it's good practice to include one.

# The body of the function is indented underneath the function definition.
# In this case, it contains one line that prints a greeting.

# The function doesn't return anything, but it could if we used the "return" keyword.

# To use the function, we can call it with an argument:
greet("John")
# This will print "Hello, John!" to the console.
```

-   The **`def`** keyword is used to define the function.
-   The function name follows the **`def`** keyword, and it should be descriptive of what the function does.
-   The parameters are specified in parentheses and separated by commas. If there are no parameters, you can leave the parentheses empty.
-   The code block that makes up the function's body is indented.
-   The **`return`** statement is used to specify the value that the function should return.



## Calling a Function

<aside> 😎 **Calling Functions in Python:** Once you have defined a function in Python, you can call it from your code using the function name followed by parentheses.

</aside>

**Syntax to call a function:**

```python
function_name(arguments)
```

-   The function name should match the name you used when defining the function.
-   The arguments you pass to the function should match the number and order of the parameters specified in the function definition.

When calling a function, it's important to keep the following things in mind:

-   Make sure you are calling the correct function by checking its name.
-   Make sure you are passing the correct number and order of arguments to the function.
-   If a function returns a value, make sure you are capturing and using that value in your code.
-   A function cannot be called before it is defined




## Code Examples

-   **Example 1: Finding if a number is armstrong number or not.**
    
    <aside> 😎 Armstrong number is a number which is equal to sum of its digits raised to power of number of digits. Ex: 153 ⇒ 1^3 + 5^3 + 3^3 = 153.
    
    </aside>
    
    ```python
    def is_armstrong_number(num):
        """
        This function checks if a given number is Armstrong number or not
        :param num: an integer to be checked
        :return: True if the number is Armstrong, False otherwise
        """
        num_str = str(num)
        num_digits = len(num_str)
    
        sum: int = 0
        for digit in num_str:
            sum += int(digit) ** num_digits
    
        return sum == num
    
    isArmStrong = is_armstrong_number(153)
    
    print(isArmStrong)
    ```
    
-   **Example 2: Finding the greatest common divisor (GCD) of two numbers.**
    
    <aside> 😎 The GCD is the largest number that divides both input numbers without leaving a remainder
    
    </aside>
    
    ```python
    def gcd(a, b):
        """
        This function finds the greatest common divisor (GCD) of two numbers using the Euclidean algorithm
        :param a: first number
        :param b: second number
        :return: GCD of a and b
        """
        if b == 0:
            return a
        else:
            return gcd(b, a % b)
        # In this function, the Euclidean algorithm is used to repeatedly find the remainder of a divided by b, 
        # until b becomes zero. At that point, the GCD is equal to 'a'. The function uses recursion to implement this 
        # algorithm, calling itself with b and a % b as arguments until b becomes zero.
    ```


# 2. Pass Statement

<aside> 😎 The **`pass`** statement is a placeholder statement that does nothing. It is used in situations where Python syntax requires a statement, but you don't want to execute any code.

</aside>

For example, it can be used as a placeholder when defining a function or a class that you haven't implemented yet

**Syntax:**

```python
pass
```

Here are some key points to keep in mind when using the **`pass`** statement:

-   The **`pass`** statement does nothing. It simply serves as a placeholder.
-   The **`pass`** statement is often used when defining functions, classes, and conditional statements that you haven't implemented yet.
-   The **`pass`** statement can also be used as a placeholder in loops or other control flow statements, but this is less common.
-   Be careful not to use the **`pass`** statement too frequently in your code, as it can make your code harder to read and understand.





# 3. Return Statement

> The `return` statement is used in Python to end the execution of a function and return a value to the caller.

**Syntax of the return statement:**

```python
def function_name(parameters):
	# code block 
	return value
```

 **Using the `return` statement**
 
 ```python
 # Function to add two numbers and return the result
def add_numbers(a, b):
    result = a + b
    return result

# Function to check if a number is even and return True or False
def is_even(number):
    if number % 2 == 0:
        return True
    else:
        return False

# Function to return a list of even numbers from a given list
def get_even_numbers(numbers):
    result = []
    for number in numbers:
        if number % 2 == 0:
            result.append(number)
    return result

```

**Additional usages of return statement**

A function can return multiple values using a tuple or a list. 
For example:

```python
def get_name_and_age(): 
	name = "Alice"
	age = 25
	return name, age

name, age = get_name_and_age() # this is called unpacking, here function returning a tuple
print(f"Name: {name}, Age: {age}")
```

**Unpacking in python**
- The process of extracting individual elements from an iterable like a list or tuple
```python
my_tuple = (1, 2, 3)

a,b,c = my_tuple;
# Now, the value of `a` will be `1`, `b` will be `2`, and `c` will be `3`.
```

### Pitfalls
- If a function doesn't have a `return` statement, it will return `None` by default.
- You can use the `return` statement to exit a function early if a certain condition is met. For example:

```python
	def is_even(num):
		if num % 2 == 0:
			return True
		else:
			return False
```

- Depending on the data type function returns, that can be assigned to a variable at the left side of the function call
- In Python, you can use the `yield` keyword instead of `return` to create a generator function that generates a sequence of values on the fly, instead of generating all of them at once. This is useful when dealing with large amounts of data that won't fit into memory all at once.
# 4. [Arguments and Parameters](Arguments%20and%20Parameters.md)
# 5. [Local variables and Global Variables](Local%20variables%20and%20Global%20Variables.md)
# 6. [Lambda Functions](Lambda%20Functions.md)
# 7. [Comprehensions](Comprehensions.md)
# 8. [Special Functions](Special%20Functions.md)


