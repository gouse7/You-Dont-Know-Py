
## Indentation

We first need to know about Indentation.

1.  **Most Critical Concept**
    
    1.  Indentation is _used to define code blocks_ in Python. Unlike other programming languages, Python uses indentation instead of curly braces or other characters to delimit blocks of code. This means that the _spacing of each line is significant and affects the meaning_ of the code.
    2.  Indentation should be consistent throughout your code. Use either spaces or tabs to indent your code, _but not both_. In general, it is recommended to use four spaces for each level of indentation.
    3.  Incorrect indentation can cause syntax errors or change the meaning of your code. For example, if the indentation is not consistent, the interpreter may not be able to determine which lines of code belong to which block.
    4.  Python uses the colon character (:) to indicate the start of a new code block. For example:
    ```python
    if x > 0:
        print("x is positive")  # this line is indented and part of the code block
    ```
    6.  Nested code blocks can be indented further, creating a hierarchy of code blocks. For example:
    
    ```python
    if x > 0:
        print("x is positive")  # this line is indented and part of the first code block
        # Check if x is even
        if x % 2 == 0:
            print("x is even")  # this line is indented further and part of the nested code block
    ```
    
    7.  Blank lines and whitespace are ignored by Python, except when they are used to delimit code blocks. This means that you can use blank lines and additional whitespace to make your code more readable and easier to understand.
    8.  In addition to defining code blocks, indentation is also used to align code in a visually pleasing way. For example:
    
    ```python
    def my_function(x, y, z):
        result = (x * y) + z  # this line is indented to align with the opening parentheses
        return result
    ```
    
    <aside> 🧠 In summary, indentation is a critical aspect of Python syntax and is used to define code blocks, create hierarchies, and make code more readable. Consistent and correct indentation is essential for writing clear and maintainable Python code.
    
    </aside>
    

## if statement

<aside> 😎 **if statement:** The if statement is used to execute a block of code if a condition is true. It follows the syntax:

</aside>

Syntax

```python
if condition:
    # code block to execute if condition is true
```

For example, to check if a number is positive or not:

```python
num = 5
if num > 0:
    print("The number is positive")
```

#### if-else statement

<aside> 😎 **if-else statement:** The if-else statement is used to execute one block of code if a condition is true, and another block of code if the condition is false.

</aside>

It follows the syntax:

```python
if condition:
    # code block to execute if condition is true
else:
    # code block to execute if condition is false
```

For example, to check if a number is positive or negative:

```python
num = -2
if num > 0:
    print("The number is positive")
else:
    print("The number is negative")
```

#### if-elif-else statement

<aside> 😎 **if-elif-else statement:** The if-elif-else statement is used to execute one of several code blocks, depending on which condition is true.

</aside>

It follows the syntax:

```python
if condition1:
    # code block to execute if condition1 is true
elif condition2:
    # code block to execute if condition2 is true and condition1 is false
else:
    # code block to execute if all conditions are false
```

For example, to check if a number is positive, negative, or zero:

```python
num = 0
if num > 0:
    print("The number is positive")
elif num < 0:
    print("The number is negative")
else:
    print("The number is zero")
```

#### Nested if statements

<aside> 😎 **Nested if statements:** It's possible to use if statements inside other if statements, creating nested conditions.

</aside>

For example, to check if a number is even or odd and positive or negative:

```python
num = -6
if num >= 0:
    if num % 2 == 0:
        print("The number is positive and even")
    else:
        print("The number is positive and odd")
else:
    if num % 2 == 0:
        print("The number is negative and even")
    else:
        print("The number is negative and odd")
```

##### Pitfalls

1.  Always include a colon at the end of an if or else statement to indicate the start of the code block.
2.  Use parentheses around the condition for clarity and readability.
3.  Be careful not to use the assignment operator (=) instead of the comparison operator (==).
4.  Understand that non-zero values and non-empty containers are considered True in Python.
5.  Make sure to handle all possible cases and unexpected input.
6.  Avoid nesting if-else statements too deeply to keep your code readable and easy to understand.

## match case statement

<aside> 😎 The **`match`**statement, also known as pattern matching, is a control flow statement that allows you to match a value against a set of patterns, and execute the code block associated with the first pattern that matches the value.

</aside>

**Syntax:**

```python
match expression:
    pattern1:
        # code to execute if expression matches pattern1
    pattern2:
        # code to execute if expression matches pattern2
    ...
    patternN:
        # code to execute if expression matches patternN
    [case _:]
        # code to execute if expression does not match any of the patterns
```

In the above syntax, the **`match`**statement takes an **`expression`**that is matched against a set of **`patterns`.** Each **`pattern`**can be a value, a variable, a tuple of values and/or variables, or a combination of these.

If the **`expression`**matches one of the **`patterns`**, the code block associated with that **`pattern`**is executed. If none of the **`patterns`**match the **`expression`**, the **`case _:`**block is executed.

**Example:**

```python
def get_day_of_week(day):
    match day:
        case 1:
            return "Monday"
        case 2:
            return "Tuesday"
        case 3:
            return "Wednesday"
        case 4:
            return "Thursday"
        case 5:
            return "Friday"
        case 6:
            return "Saturday"
        case 7:
            return "Sunday"
        case _:
            return "Invalid day"

print(get_day_of_week(3))  # Output: Wednesday
print(get_day_of_week(8))  # Output: Invalid day
```

In this example, the **`get_day_of_week`**function uses a **`match`** statement to match the **`day`**argument against a set of **`patterns`** corresponding to the days of the week. If the **`day`** argument matches one of the **`patterns`**, the name of the corresponding day is returned. If the **`day`** argument does not match any of the **`patterns`**, the message "Invalid day" is returned.

**Usage:**

1.  Match against a single value: You can use the **`case value:`** pattern to match against a single value, such as an integer, string, or boolean.
2.  Match against multiple values: You can use the **`case value1 | value2 | value3:`** pattern to match against multiple values.
3.  Match against a range of values: You can use the **`case range(x, y):`** pattern to match against a range of values.
4.  Match against a regular expression: You can use the **`case re.match(pattern, value):`** pattern to match against a regular expression.
5.  Match against a container membership: You can use the **`case value in container:`** pattern to match against a container membership, such as a list, tuple, or set.
6.  Match against a type: You can use the **`case type(value):`** pattern to match against a type.
7.  Match against any value: You can use the **`case _:`**, or **`case ...:`** pattern to match against any value, or any value that matches the specified type or pattern.

#### Pitfalls

1.  Forgetting the **`:`** after each **`case`** statement: The **`case`** statement must end with a colon (**`:`**), otherwise you'll get a syntax error.
2.  Mismatch between the pattern and the value being matched: If the pattern and the value being matched are of different types, the **`match`** statement will not work as expected. For example, if you're trying to match a string against an integer pattern, the match will always fail.
3.  Forgetting the default **`case _:`** block: If you forget to include a default **`case`** block at the end of the **`match`** statement, and the expression being matched doesn't match any of the patterns, a **`TypeError`** will be raised.
4.  Overcomplicating the patterns: It's important to keep the patterns simple and straightforward. If you try to match too many values or use too many nested patterns, your code can become hard to read and maintain.
5.  Using **`match`** statement in older versions of Python: The **`match`** statement is a relatively new feature in Python 3.10, so it may not be available in older versions of Python. If you try to use the **`match`** statement in an older version of Python, you'll get a syntax error.

## while loop

<aside> 😎 A while loop is used to repeatedly execute a block of code as long as a boolean expression (condition) remains true.

</aside>

Syntax:

```python
while condition:
    # code block to execute while the condition is true
```

The condition is checked at the beginning of each iteration. If the condition is true, the code block is executed, and the condition is checked again for the next iteration. If the condition is false, the loop is exited, and the program continues with the code after the loop.

For example, to print the numbers from 1 to 5 using a while loop:

```python
num = 1
while num <= 5:
    print(num)
    num += 1
```

In this example, the condition **`num <= 5`** is checked at the beginning of each iteration. The loop continues to execute as long as the condition is true, and the variable **`num`** is incremented by 1 at the end of each iteration. The loop exits when the condition becomes false (i.e., **`num`** becomes 6).

#### while—else

<aside> 😎 **`while...else`**loop A **`while`** loop can also have an **`else`** block, which is executed when the condition becomes false. The **`else`** block is executed only if the loop completes all its iterations without encountering a **`break`**statement. If there is a break present, else block will not be executed.

</aside>

Example:

```python
x = 1

while(x <= 10):
	print(x)
	x = x+1
else:
	print("Done")
```

The above code will first print the numbers from 1 to 10. When x is 11, the while condition will fail, triggering the else condition.

#### nested while loop

<aside> 🧠 A **`while`**loop can also be nested inside another **`while`** loop. This can be useful when you need to iterate over multiple conditions or data structures. Here is an example:

</aside>

```python
outer_num = 1
while outer_num <= 3:
    inner_num = 1
    while inner_num <= 3:
        print(outer_num, inner_num)
        inner_num += 1
    outer_num += 1
```

In this example, the outer **`while`** loop runs 3 times, and the inner **`while`** loop runs 3 times for each iteration of the outer loop. The output of this code will be:

```python
1 1
1 2
1 3
2 1
2 2
2 3
3 1
3 2
3 3
```

#### pitfalls

1.  Infinite loops: One of the most common mistakes with **`while`** loops is creating an infinite loop, which occurs when the condition never becomes false. This can happen when the condition is not properly defined or updated within the loop. Always make sure to check your loop conditions and ensure that they will eventually become false.
2.  Off-by-one errors: Another common mistake is off-by-one errors, where the loop runs for one iteration too many or too few. This can happen when the loop condition is not properly defined or when the loop variable is not properly initialized or updated.
3.  Not updating the loop variable: It's important to ensure that the loop variable is properly updated within the loop so that the loop condition will eventually become false. Forgetting to update the loop variable can cause an infinite loop or other unexpected behavior.
4.  Using a mutable variable as the loop condition: When using a mutable variable (such as a list or dictionary) as the loop condition, be aware that changes to the variable within the loop may affect the loop condition. This can lead to unexpected behavior or an infinite loop.
5.  Not using **`break`** or **`continue`** statements carefully: **`break`** and **`continue`** statements can be useful for controlling the flow of a loop, but they can also be a source of confusion and errors if not used carefully. Make sure to use them only when necessary and ensure that they are placed in the correct part of the loop.

#### break statement

<aside> 😎 The break statement, is used to stop the loop even if the condition is true

</aside>

Syntax:

```python
while condition:
    # code block
    if some_condition:
        break
```

In the above syntax, the **`break`**statement is used to exit the loop if **`some_condition`**is met, even if **`condition`** is still true. After the **`break`**statement is executed, the program continues to execute from the next statement after the loop.

Example:

```python
i = 1
while i < 6:
  print(i)
  if i == 3:
    break
  i += 1
# other code
```

In the above example, if i is equal to 3, the loop is stopped and exit out of loop.

Some additional notes on the **`break`** statement:

-   The **`break`** statement is commonly used in combination with conditional statements (such as **`if`** statements) to exit a loop when a certain condition is met.
-   The **`break`** statement can be used with any type of loop in Python, including **`while`** loops and **`for`** loops.
-   If the **`break`** statement is not used carefully, it can result in unexpected behavior or an infinite loop. Therefore, it's important to make sure that the **`break`** statement is used only when necessary and placed in the correct part of the loop.

#### continue statement

<aside> 😎 The continue statement is used to skip over the current iteration of a loop and move on to the next iteration

</aside>

**Syntax**:

```python
while condition:
    # code block
    if some_condition:
        continue
    # code block to execute if some_condition is false
```

In the above syntax, the **`continue`**statement is used to skip over the rest of the code block for the current iteration of the loop if **`some_condition`**is met. The program then moves on to the next iteration of the loop.

**Example:**

```python
i = 0
while i < 6:
  i += 1
  if i == 3:
    continue
  print(i)
```

In the above example, if i is equal to 3, print is not called and continued to next iteration.

Some additional notes on the **`continue`** statement:

-   The **`continue`** statement is commonly used in combination with conditional statements (such as **`if`** statements) to skip over certain iterations of a loop when a certain condition is met.
-   The **`continue`** statement can be used with any type of loop in Python, including **`while`** loops and **`for`** loops.
-   If the **`continue`** statement is not used carefully, it can result in unexpected behavior or an infinite loop. Therefore, it's important to make sure that the **`continue`** statement is used only when necessary and placed in the correct part of the loop.

## for loop

<aside> 😎 The **`for`**loop is used to iterate over a sequence of values, such as a list, tuple, or string, and perform a certain action on each value.

</aside>

**Syntax:**

```python
for variable in sequence:
    # code block to execute for each value in sequence
```

In the above syntax, the **`for`**loop is used to iterate over the values in the **`sequence`** , and the **`variable`** takes on the value of each item in the sequence for each iteration of the loop. The code block inside the loop is executed once for each value in the sequence.

Some additional notes on the **`for`** loop:

-   The **`sequence`** can be any type of iterable object in Python, such as a list, tuple, string, or range object.
-   The **`for`** loop can also be used with the **`enumerate()`** function to iterate over both the values and the indices of a sequence.
-   The **`break`** and **`continue`** statements can also be used inside a **`for`** loop to prematurely exit the loop or skip over certain iterations, respectively.
-   In Python, the **`for`** loop is often used with the **`range()`** function to iterate a certain number of times. For example:

```python
for i in range(5):
    print(i)
```

In the above example, the **`range(5)`**function creates a sequence of values from 0 to 4, and the **`for`** loop iterates over these values, printing each value to the console.

#### for-else loop

<aside> 😎 The **`for`**loop can also be used with the **`else`** block, similar to the **`while`** loop, to execute a certain code block _after the loop has finished iterating over all the values_ in the sequence. The **`else`** block is executed only if the loop completes all its iterations without encountering a **`break`** statement.

</aside>

Syntax:

```python
for value in sequence:
    # code block to execute for each value in sequence
else:
    # code block to execute after the loop has finished
```

In the above syntax, the **`else`**block is optional and will only be executed when the loop has completed all its iterations without encountering a **`break`**statement.

**Example 1:**

```python
fruits = ['apple', 'banana', 'cherry']
for fruit in fruits:
    print(fruit)
else:
    print("All fruits have been printed")
```

In this example, the **`for`**loop will iterate over the **`fruits`**list and print each fruit. After all the iterations have been completed, the **`else`**block will be executed and the message "All fruits have been printed" will be printed to the console.

**Example 2:**

If we add a **`break`** statement to the loop, the **`else`** block will not be executed:

```python
fruits = ['apple', 'banana', 'cherry']
for fruit in fruits:
    print(fruit)
    if fruit == 'banana':
        break
else:
    print("All fruits have been printed")
```

In this example, the **`break`** statement is triggered when the loop reaches the **`'banana'`** element, so the **`else`** block is not executed.

