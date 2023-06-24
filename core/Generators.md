# Generators in Python

- A generator is a special type of function in Python.
- Generator functions always contain the `yield` keyword.
- If a function contains a `return` statement, it is called a normal function and can return multiple values if required.
- If a function contains the `yield` keyword, it is called a generator function. The `yield` statement returns a value only on demand, reducing memory space usage.
- Syntax:
  ```python
  def function_name(start, stop, step):
      # Generator function body
      yield value
      # ...
  ```
- The `yield` keyword is used to provide a value back to the function call from the function definition and allows the function execution to continue until a condition becomes false.
- Generators have an advantage over regular functions when dealing with large amounts of data. They save a significant amount of memory space. Functions provide all the results at once, taking up more memory, while generators provide one value at a time when requested, minimizing memory usage.

Generators are a powerful feature in Python that allow efficient memory usage and lazy evaluation of data. They are particularly useful when working with large data sets or when generating sequences of values on demand.


# Iterators in Python

Iterators in Python are objects used to iterate over iterable objects such as lists, tuples, dictionaries, strings, and sets. They offer the following advantages:

1. Memory Efficiency: When dealing with large amounts of data, iterators allow us to work with the data in small, manageable chunks instead of loading everything into memory at once. This helps prevent memory overflow issues and allows for efficient processing of large datasets.

2. Lazy Evaluation: Iterators provide a mechanism for lazy evaluation. Instead of computing and storing all the items upfront, iterators generate and supply items on demand. This means that only the necessary items are computed and retrieved as needed, reducing unnecessary computations and memory usage.

To work with iterators in Python, we use the following concepts:

- Initialization: An iterator object is created using the `iter()` function. It takes an iterable object as an argument and returns an iterator object.

- Iteration: The `next()` function is used to obtain the next element from the iterator object. It retrieves the next item in the iteration sequence. If there are no more items, a `StopIteration` exception is raised.

Note: Iterators do not support indexing or slicing operations because they supply values on demand, rather than having all the items available at once.

Example 1: Iterating over a string using an iterator
```python
s = 'Python'
it = iter(s)
while True:
    try:
        item = next(it)
        print(item)
    except StopIteration:
        break
```

Example 2: Iterating over a tuple using an iterator
```python
my_tuple = ("apple", "banana", "cherry")
my_iter = iter(my_tuple)
print(next(my_iter))  # Output: apple
print(next(my_iter))  # Output: banana
print(next(my_iter))  # Output: cherry
```

	Iterators are a valuable tool for efficient handling of large datasets, enabling lazy evaluation and reducing memory consumption. They allow us to process data in a more manageable and optimized manner, making them useful in various data analysis and manipulation scenarios.