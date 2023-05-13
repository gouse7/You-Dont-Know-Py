# Exception Handling in Python

## Purpose of Exception Handling
- Exception handling is a mechanism in Python that helps to handle errors that occur during program execution.

## Definition of Exception
- An exception is an event that interrupts the normal flow of program execution.

## Definition of Exception Handling
- Exception handling is a way to handle runtime errors, such as syntax errors or logical errors, during program execution.

## Types of Errors

The purpose of Exception Handling is to build robust applications. During the development of any application, we use a programming language to develop, compile and execute various programs. During this process, we may encounter different types of errors, which are classified into three types:

1. **Compile Time Errors**: 
   - These errors occur during the compilation process (from .py to .pyc). They occur due to a programmer not following the syntaxes of the language. These errors are solved by programmers during the development time.

2. **Logical Errors**: 
   - These errors occur during the execution time (from .pyc to PVM). They occur due to the wrong representation or invalid logic of the problem. Logical errors always produce incorrect results. These errors are also solved by programmers during development time.

3. **Runtime Errors (Implementation Errors)**: 
   - These errors occur during the runtime or execution time. They occur due to wrong or invalid inputs entered by the end-user or application user. By default, runtime errors always generate technical error messages, which are understandable by programmers but not by end-users. So, it is recommended to convert technical error messages into user-friendly error messages by using Exception Handling.

We need to handle these errors using Exception Handling to provide a better user experience and build robust applications.

## Building Points in Learning Exception Handling

- Understanding the concept of exceptions.
- Identifying and handling exceptions in Python.
- Creating custom exceptions.

## Types of Exceptions

1.  Pre-Defined or Built-In Exceptions:
    -   These are the exceptions that are already defined in Python and can be used directly in the program.
    -   Python provides a range of built-in exceptions that can be raised when certain errors occur during program execution.
    -   Examples of built-in exceptions include `TypeError`, `ValueError`, and `ZeroDivisionError`.
    
1.  Programmer or User or Custom-Defined Exceptions:
    -   These exceptions are created by programmers as per the requirements of the program.
    -   Custom exceptions can be used to handle specific errors that are not covered by the built-in exceptions.
    -   To define a custom exception, a new class can be created that inherits from the built-in `Exception` class or any of its subclasses.
    -   Custom exceptions can be raised using the `raise` statement and can be caught using a try-except block.

### Additional Points
-   It is generally recommended to use built-in exceptions whenever possible to ensure consistency and clarity in code.
-   Custom exceptions should be used sparingly and only when necessary to avoid cluttering code with unnecessary complexity.
-   It is a good practice to give custom exceptions meaningful names that accurately reflect the error being handled.
-   The Python style guide (PEP 8) recommends using the suffix "Error" for custom exception names to distinguish them from regular classes.

### Next [Exception Handling](Exception%20Handling.md)
