
## Keywords Used in Exception Handling

1. **try:** It is used to specify a block of code to be tested for errors.
2. **except:** It is used to specify a block of code to be executed if an error occurs in the try block.
3. **else:** It is used to specify a block of code to be executed if no errors occur in the try block.
4. **finally:** It is used to specify a block of code to be executed regardless of whether an error occurs in the try block.
5. **raise:** It is used to raise an exception explicitly in the program.

## Syntax for Handling Exceptions

- Handling the Exceptions in Python refers to converting technical error messages into user-friendly error messages.
- To handle the exceptions in Python, there are 5 keywords: try, except, else, finally, and raise.
- The syntax for handling exceptions in Python is:

  ```python
  try:
      # Block of statements that may generate exceptions
  except exception-class-name-1:
      # Block of statements to generate user-friendly error messages
  except exception-class-name-2:
      # Block of statements to generate user-friendly error messages
      .
      .
      .
  except exception-class-name-n:
      # Block of statements to generate user-friendly error messages
  else:
      # Block of statements to generate results
  finally:
      # Block of statements that execute compulsorily
  ```

- The try block contains a block of statements that may generate exceptions.
- The except block catches the exceptions and generates user-friendly error messages.
- There can be multiple except blocks for different exception classes.
- The else block executes if no exception is raised in the try block and generates the results.
- The finally block executes compulsorily, whether an exception is raised or not, and is used to clean up resources.
- The raise keyword is used to raise an exception explicitly.

## Explanation for the keywords used in Syntax of Handling Exception

## try

- `try` block is where we write a block of statements that may generate exceptions.
- The statements that generate exceptions should be written within the `try` block. Hence, the `try` block is called the exception monitoring block.
- When an exception occurs in the `try` block, the PVM (Python Virtual Machine) exits the `try` block and executes the appropriate `except` block.
- After executing the appropriate `except` block, PVM never goes to the `try` block for executing the rest of the statements in the `try` block.
- Every `try` block must be immediately followed by an `except` block (otherwise, we get a `SyntaxError`).
- Every `try` block must contain at least one `except` block. It is recommended to write multiple `except` blocks for generating user-friendly error messages.

## except

- `except` block is where we write a block of statements that generates user-friendly error messages. In other words, the `except` block suppresses technical error messages and generates user-friendly error messages. Hence, the `except` block is called the exception processing block.
- The `except` block will execute when an exception occurs in the `try` block.
- Even if we write multiple `except` blocks, PVM executes the appropriate `except` block (single block) depending on the type of exception that occurs in the `try` block.
- The place to write the `except` block is after the `try` block and before the `else` block (if present).

## else

- `else` block is where we write a block of statements that will display the results of the program. Hence, the `else` block is called the result-generated block.
- The `else` block will execute when no exception occurs in the `try` block.
- Writing the `else` block is optional.
- The place to write the `else` block is after the `except` block and before the `finally` block (if it is present).

## finally

- `finally` block is where we write a block of statements that will relinquish (release/close/give-up/clean-up) the resources (files, database software) that are obtained in the `try` block. Hence, the `finally` block is called the resource relinquishing block.
- The `finally` block will execute compulsorily.
- Writing the `finally` block is optional.
- The place to write the `finally` block is after the `else` block (if the `else` block is present).

## Notes on Various Forms of except blocks

- Exception handling is done with the help of try and except blocks.
- We can use except blocks in various forms:
 
### Form-1: 
- In this form, we can handle one exception at a time.
- We need to write one except block for one type of exception.
- It is recommended to write multiple except blocks for generating user-friendly error messages.
- Every try block must contain at least one except block.

### Form-2: 
- In this form, we can handle multiple specific exceptions with a single except block.
- This type of facility is called Multi-Exception handling block.
- We need to write multiple exception classes inside parentheses separated by commas in the except block.

### Form-3: 
- In this form, we can handle one exception at a time with an alias name for capturing technical error messages occurring due to exception occurrence.
- We need to write the exception class name with the alias name after the except block.

### Form-4: 
- In this form, we can write a default except block which matches with all types of exceptions.
- Industry does not recommend writing a single default except block because it gives common messages for all types of exceptions.
- Hence, it is highly recommended to write the default except block at the end of all types of specific except blocks.

- The final syntax for try and except block:
```python
	try:
		#statements generating exceptions
	except exception-class-name-1:
		#statements to handle the exception of exception-class-name-1
	except exception-class-name-2:
		#statements to handle the exception of exception-class-name-2
	except:
		#statements to handle the default exception
	else:
		#statements to be executed if no exception occurs in the try block
	finally:
		#statements to be executed regardless of whether an exception occurs or not
```

## Implementation of ATM Operations
- A case study is presented that demonstrates the implementation of exception handling in ATM operations.