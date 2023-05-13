

## Fundamental category

#### int (integer)

<aside> 🧠 The **`int`** data type represents integer numbers, which can be either positive, negative, or zero. (numbers which do not have fractional component) Ex: 1, 2, -1, -5, 0 etc

</aside>

```python
# Creating integer variables
x = 10
y = -5
z = 0

# Performing arithmetic operations on integers
sum = x + y
difference = x - y
product = x * y
quotient = x / y
floor_quotient = x // y  # Will see details later
remainder = x % y
power = x ** 2
```

1.  In Python, **`int`** objects have unlimited precision, meaning that they can represent arbitrarily large numbers.
2.  Integers can be created using numeric literals, or by using arithmetic operators on other integers or floating-point numbers.
3.  In Python, **`int`** objects are immutable, which means that once an **`int`** object is created, it cannot be modified.
4.  Python automatically promotes smaller integers to larger integers as necessary, depending on the arithmetic operation being performed.
5.  The **`int`** data type supports bitwise operations, such as AND, OR, XOR, and bit shifting, which can be used for low-level manipulation of binary data.

**Binary, Ocatal, Hexadeciaml**

<aside> 🧠 Python provides support for binary, hexadecimal, and octal literals for creating **`int`** objects in non-decimal bases.

In the decimal number system (base 10), numbers are represented using 10 digits (0-9), with each digit representing a different power of 10. For example, the number 1234 in decimal notation is equal to:

1_10^3 + 2_10^2 + 3_10^1 + 4_10^0 = 1000 + 200 + 30 + 4 = 1234

Binary numbers, on the other hand, use only 2 digits (0 and 1) to represent numbers. Each digit in a binary number represents a power of 2, starting from the rightmost digit with 2^0. For example, the binary number 1011 is equal to:

1_2^3 + 0_2^2 + 1_2^1 + 1_2^0 = 8 + 0 + 2 + 1 = 11

Hexadecimal numbers use 16 digits (0-9 and A-F) to represent numbers. Each digit in a hexadecimal number represents a power of 16, starting from the rightmost digit with 16^0. For example, the hexadecimal number AB is equal to:

10_16^1 + 11_16^0 = 160 + 11 = 171

Octal numbers use 8 digits (0-7) to represent numbers. Each digit in an octal number represents a power of 8, starting from the rightmost digit with 8^0. For example, the octal number 73 is equal to:

7_8^1 + 3_8^0 = 56 + 3 = 59

</aside>

> specific prefixes (`0b`for binary, `0x`for hexadecimal, and `0o`for octal).

1.  A binary literal is prefixed with **`0b`** or **`0B`**, a hexadecimal literal is prefixed with **`0x`** or **`0X`**, and an octal literal is prefixed with **`0o`** or **`0O`**.
2.  The **`bin()`**, **`hex()`**, and **`oct()`** functions can be used to convert an integer to its binary, hexadecimal, or octal representation, respectively.
3.  The **`int()`** function can be used to convert a string containing a binary, hexadecimal, or octal representation of an integer to an **`int`** object.
4.  To convert an **`int`** object to a binary string representation, use the **`bin()`** function, which returns a string prefixed with **`0b`**.
5.  To convert an **`int`** object to a hexadecimal string representation, use the **`hex()`** function, which returns a string prefixed with **`0x`**.
6.  To convert an **`int`** object to an octal string representation, use the **`oct()`** function, which returns a string prefixed with **`0o`**.

#### float (floating-point number)

<aside> 🧠 The **`float`** data type represents floating-point numbers, which can represent both whole numbers and fractional values.

</aside>

```python
# Creating float variables
x = 3.14
y = -2.5
z = 0.0

# Performing arithmetic operations on floats
sum = x + y
difference = x - y
product = x * y
quotient = x / y
power = x ** 2

# Converting other data types to floats
int_to_float = float(10)
string_to_float = float("3.14")
```

1.  In Python, **`float`** objects represent decimal values and can represent both whole numbers and fractional values.
2.  Floating-point values can be created using numeric literals, or by using arithmetic operators on other floats or integers.
3.  The **`float`** data type supports common arithmetic operations such as addition, subtraction, multiplication, division, and exponentiation.
4.  Python automatically promotes integers to floats when necessary, depending on the arithmetic operation being performed.
5.  Floating-point values are often used to represent real-world quantities, such as measurements or scientific values. However, due to the way that computers store and manipulate floating-point numbers, there can be some precision and rounding issues when performing arithmetic operations with them.

<aside> 🧠 **Important**

-   Float objects in Python are represented in binary-point form, which can lead to precision errors due to the limitations of binary representation.
-   Not all decimal values can be represented exactly in binary form, leading to approximations.
-   The precision of float values is limited by the number of bits used to represent the number, which is 64 bits by default in Python, providing around 15 decimal digits of precision.
-   Performing arithmetic operations on float values can lead to rounding errors due to the limitations of binary-point representation.
-   To minimize precision errors when working with float values, the decimal module in Python can be used, which supports decimal arithmetic for precise calculations.
-   When comparing float values for equality, it is recommended to use a tolerance or "epsilon" value, which allows for small differences in values due to rounding errors. </aside>

#### complex (complex number)

<aside> 🧠

The **`complex`** data type represents complex numbers, which have a real part and an imaginary part. Complex numbers can be created by using the `complex()` constructor, or by using the `j` or `J` suffix to indicate the imaginary part. Ex: 2 + 3j, -4j, etc.

</aside>


#### Creating complex variables
z1 = 2 + 3j
z2 = complex(1, 4)

#### Accessing real and imaginary parts
real_x = x.real
imag_x = x.imag

#### Converting other data types to complex
int_to_complex = complex(3)
float_to_complex = complex(3.14)

#### Performing arithmetic operations on complex numbers
sum = z1 + z2
difference = z1 - z2
product = z1 * z2
quotient = z1 / z2
conjugate = z1.conjugate()
real_part = z1.real
imag_part = z1.imag
```

1.  In Python, complex numbers are represented using the **`j`** suffix, where **`j`** represents the imaginary unit.
2.  Complex numbers can also be created using the built-in **`complex()`** function, which takes two arguments representing the real and imaginary parts, respectively.
3.  Complex numbers support arithmetic operations such as addition, subtraction, multiplication, and division, as well as more advanced operations such as computing the conjugate or absolute value.
4.  The real and imaginary parts of a complex number can be accessed using the **`real`** and **`imag`** attributes, respectively.
5.  Other data types such as integers and floating-point numbers can be converted to complex numbers using the **`complex()`** function.
6.  Complex numbers are often used in scientific and engineering applications, particularly in the fields of signal processing, control systems, and electromagnetics.

**Internal Working**

Internally, complex numbers in Python are represented as a pair of floating-point numbers, one representing the real part and the other representing the imaginary part. These floating-point numbers are stored in binary format using a fixed number of bits.

For example, a complex number with real part 2.0 and imaginary part 3.0 is represented internally as the pair of floating-point numbers (2.0, 3.0).

Complex numbers in Python support all of the arithmetic operations that are available for floating-point numbers, such as addition, subtraction, multiplication, and division. These operations are performed using the standard rules of complex arithmetic, which are based on the algebraic properties of the real and imaginary parts of the complex numbers.

For example, to add two complex numbers **`a`** and **`b`**, we add their real parts and their imaginary parts separately:

```python
(a.real + b.real) + (a.imag + b.imag)*1j
```

The **`1j`** at the end represents the imaginary unit, which is defined as the square root of -1.

Similarly, to multiply two complex numbers **`a`** and **`b`** , we apply the distributive property and the fact that the square of the imaginary unit is -1:

```python
(a.real*b.real - a.imag*b.imag) + (a.real*b.imag + a.imag*b.real)*1j
```

<aside> 🧠 Common Pitfall

Because complex numbers are represented internally as pairs of floating-point numbers, there can be precision errors when performing arithmetic operations on complex numbers, just like with float numbers. It is recommended to use the **`cmath`** module for complex arithmetic operations, which provides more accurate results than the built-in complex arithmetic operations.

One common pitfall when using complex numbers in Python is forgetting to add the **`j`** suffix to represent the imaginary part. For example, **`2i`** is not a valid complex number in Python, but **`2j`** is.

</aside>

#### bool (boolean)

<aside> 

🧠 **`bool`** data type represents Boolean values, which can only be either **`True`** or **`False`**.

</aside>

```python
# Creating boolean variables
x = True
y = False

# Performing logical operations on booleans
and_result = x and y
or_result = x or y
not_result = not x

# Comparing values using comparison operators
equal_result = x == y
not_equal_result = x != y
greater_than_result = x > y
less_than_result = x < y
greater_than_or_equal_result = x >= y
less_than_or_equal_result = x <= y

```

1.  In Python, **`bool`** objects represent logical values that can only be either **`True`** or **`False`**.
3.  Boolean values can be created using the **`True`** and **`False`** literals, or by using logical operators such as **`and`**, **`or`**, and **`not`**.
4.  Boolean values are often used to represent the result of a logical comparison, such as testing whether one value is equal to another.
5.  In Python, **`bool`** objects are also considered a subtype of integers, with **`True`** being equivalent to the integer value 1, and **`False`** being equivalent to the integer value 0.
6.  Boolean values are often used to control the flow of program execution using conditional statements such as **`if`** and **`while`** statements.

#### str (string)

#### None (null object)

```python
# Initialize a variable to None
my_var = None

# Do some work that may or may not set a value for my_var
if some_condition:
    my_var = 42

# Check if my_var has a value
if my_var is not None:
    print("my_var has a value:", my_var)
else:
    print("my_var does not have a value")
```

The **`None`** data type in Python represents the absence of a value. It is commonly used to indicate that a variable or function parameter has no value, or to represent the result of a function that doesn't return anything.

**Properties:**

-   **`None`** is a built-in singleton object in Python, meaning that there is only one instance of it in memory.
-   **`None`** is considered to be a falsey value in Python, meaning that it evaluates to **`False`** in a boolean context.

**Features:**

-   **`None`** is often used as a default value for function parameters that are optional or have no default value specified.
-   Functions that don't return anything explicitly will automatically return **`None`** by default.
-   **`None`** can be used to initialize a variable or data structure before it is assigned a real value.

**Built-in functions:**

-   **`type(None)`**: returns the type of the **`None`** object, which is **`NoneType`**.
-   **`bool(None)`**: returns **`False`**, since **`None`** is considered to be falsey.

**Pitfalls:**

-   **`None`** can sometimes be mistakenly used as a value in a conditional expression, which can lead to unexpected behavior. For example, **`if x is None`** is correct to check if x is None, while **`if x == None`** is not correct, because **`==`** checks for value equality, not identity. The correct way is to use **`is`** operator to check for identity.
-   If you try to access an attribute or method on a variable that is **`None`**, you will get an **`AttributeError`** at runtime, since **`None`** doesn't have any attributes or methods.

********************Additional********************

-   **`None`** is a keyword in Python and not a function, so it cannot be called or passed as a function argument.
-   An object of **`NoneType`** class cannot be created explicitly since it is a pre-defined class in Python.
-   The value of **`None`** is not equivalent to False, an empty string, an empty list, or the number 0, as these are different data types in Python.

```python
# Example 1: Checking if a key exists in a dictionary
my_dict = {'name': 'John', 'age': 25}
if my_dict.get('city') is None:
    print("The key 'city' does not exist in my_dict")

# Example 2: Defining a function with an optional parameter
def my_function(arg1, arg2=None):
    if arg2 is not None:
        print(arg1, arg2)
    else:
        print(arg1)

my_function("Hello")      # Output: Hello
my_function("Hello", 42)  # Output: Hello 42

# Example 3: Using None as a placeholder in a list
my_list = [None] * 5
print(my_list)  # Output: [None, None, None, None, None]
```


## Sequence category


## List category


## Set category
#### Set Data Type

```python
s1 = {10, "Gouse", 34.56, "Python", "Hyd"}

```
#### 1. add()

Add an element to set

no effect if the element is already present

#### 2. clear()

Remove all elements from this set

#### 3. copy()

Return shallow copy of a set

#### 4. discard()

-   ****************************************************************************************************************This function is used to remove the value from set Object****************************************************************************************************************
-   ********************************************************************************************************************************If the specified value does not exist we will not get any error********************************************************************************************************************************

```python
s = {25,30,40,55,17}
s.discard(10)
```

#### 5. difference()

Returns difference of two or more sets as a new set

#### 6. difference_update()

Remove all ements of another set from this set

#### 7. intersection()

Return the intersection of two sets as new set

i.e. all elements that are in both sets.

#### 8. isdisjoint()

Return True if two sets have a null intersection

#### 9. issubset()

Return True if this set contains another set

#### 10. pop()

Remove and return an arbitary set element

Raises KeyError if element is not a memeber

#### 11. remove()

Remove an element from a set; it must be a member

KeyError if element is not a member

#### 12. union()

Return the union of serts as new set

#### 13. update()

Update a set with the union of itself and others





## Dict category
#### Dict Data Type

```python
# Create an empty dictionary
my_dict = {}

# Add some key-value pairs
my_dict['name'] = 'John'
my_dict['age'] = 25
my_dict['city'] = 'New York'

# Access a value by its key
print(my_dict['name'])  # Output: John

# Modify a value
my_dict['age'] = 26

# Remove a key-value pair
del my_dict['city']

# Iterate over the keys and values
for key, value in my_dict.items():
    print(key, value)
# Output: 
# name John
# age 26
```

**Features**

1.  Optimized for performance and memory and hence preferred for data intensive tasks
2.  Provide faster lookup with keys, hence useful in cache
3.  Useful to handle with JSON or XML data structures

The dictionary data type in Python is a collection of key-value pairs, where each key is unique and associated with a value. The dictionary is an unordered collection, meaning that the order in which items are added to the dictionary is not preserved.

Properties:

-   Keys in a dictionary must be unique and immutable (e.g., strings, numbers, or tuples), while values can be of any type.
-   Dictionaries are mutable, meaning that you can modify their contents by adding, deleting, or modifying key-value pairs.
-   A dictionary can have nested dictionaries as values, allowing you to create complex data structures.

**Features**:

-   Dictionaries provide a fast way to look up values by their keys, making them ideal for tasks like caching or indexing.
-   They can be used to store and manipulate data in a variety of formats, including JSON and XML.
-   Python's built-in **`dict`** data type is highly optimized for performance and memory usage, making it a popular choice for data-intensive applications.

**Built-in methods:**

-   **`dict[key]`** or **`dict.get(key)`**: returns the value associated with the specified key, or **`None`** if the key is not found.
-   **`dict[key] = value`**: adds or updates the value associated with the specified key.
-   **`del dict[key]`**: removes the key-value pair associated with the specified key.
-   **`len(dict)`**: returns the number of key-value pairs in the dictionary.
-   **`dict.items()`**: returns a view object containing the key-value pairs of the dictionary.

**Pitfalls:**

-   Dictionaries are unordered, meaning that the order of the key-value pairs may not be what you expect. If you need to maintain a specific order, consider using a **`collections.OrderedDict`** instead.
-   Dictionaries can raise **`KeyError`** if you try to access a key that doesn't exist. To avoid this, you can use the **`get`** method, which returns **`None`** if the key is not found.
-   Since dictionaries are mutable, you need to be careful when using them as keys in other dictionaries or sets. Immutable types like strings or tuples are a safer choice for this purpose.






## None Type category


## Print()

The **`print()`** function in Python is used to output text or other data to the console or standard output stream. Here are some of the ways the **`print()`** function can be used in Python:

1.  Print a string:
    
    ```python
    
    print("Hello, World!")
    ```
    
2.  Print multiple strings:
    
    ```python
    print("Hello,", "World!")
    ```
    
3.  Print variables:
    
    ```python
    x = 42
    print(x)
    ```
    
4.  Print variables and strings:
    
    ```python
    x = "Hello"
    y = "World"
    print(x, y)
    ```
    
5.  Print formatted strings using placeholders:
    
    ```python
    x = "John"
    y = 25
    print("My name is %s and I am %d years old." % (x, y))
    ```
    
6.  Print formatted strings using f-strings (Python 3.6+):
    
    ```python
    x = "John"
    y = 25
    print(f"My name is {x} and I am {y} years old.")
    ```
    
7.  Redirect output to a file:
    
    ```python
    with open("output.txt", "w") as f:
        print("Hello, World!", file=f)
    ```
    
8.  Specify the separator between arguments (default is a space):
    
    ```python
    print("Hello", "World", sep="-")
    ```
    
9.  Specify the end character (default is a newline):
    
    ```python
    print("Hello,", end=" ")
    print("World!")
    ```
    

