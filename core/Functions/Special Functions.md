There are 3 types of special functions in python,
1. map
2. filter
3. reduce

## `filter()`

The `filter()` function in Python is used to filter out elements from a sequence based on a given function. It returns an iterator that contains only the elements for which the function returns `True`.

The syntax for `filter()` is as follows:
```python
result = filter(function, iterable)
```
where `function` is the function that takes one argument and returns a Boolean value, and `iterable` is the sequence that you want to filter.

Here are some key points to note about the `filter()` function:

- The function that you pass to `filter()` should take one argument and return a Boolean value (`True` or `False`).
- The `filter()` function applies the given function to each element of the sequence, and returns only those elements for which the function returns `True`.
- The result of `filter()` is an iterator of type `filter`, which means you can convert it to a list, tuple, or any other iterable object.
- If the function that you pass to `filter()` is `None`, it will return all the elements of the sequence that are true.

For example, here's how you can use `filter()` to filter out even numbers from a list:
```python
numbers = [1, 2, 3, 4, 5, 6]
filtered_numbers = filter(lambda x: x % 2 == 0, numbers)
print(list(filtered_numbers)) # Output: [2, 4, 6]
```
In this example, we're using a lambda function to check whether each number in the `numbers` list is even or not. The `filter()` function then returns an iterator that contains only the even numbers. The result is stored in the `filtered_numbers` variable, which is an object of type `filter`. You can convert this object to a list by using the `list()` function, as shown in the example.




## `map()`

The `map()` function in Python is used to apply a given function to each element of a sequence (such as a list) and return a new sequence with the results.

The syntax for `map()` is as follows:
```python
result = map(function, iterable)
```
where `function` is the function that takes one argument and returns a value, and `iterable` is the sequence that you want to apply the function to.

Here are some key points to note about the `map()` function:

- The function that you pass to `map()` should take one argument and return a value.
- The `map()` function applies the given function to each element of the sequence, and returns a new sequence with the results.
- The result of `map()` is an iterator of type `map`, which means you can convert it to a list, tuple, or any other iterable object.
- If the function that you pass to `map()` is `None`, it will return the original sequence.

For example, here's how you can use `map()` to square each number in a list:
```python
numbers = [1, 2, 3, 4, 5]
squared_numbers = map(lambda x: x**2, numbers)
print(list(squared_numbers)) # Output: [1, 4, 9, 16, 25]
```
In this example, we're using a lambda function to square each number in the `numbers` list. The `map()` function then applies this function to each element of the list, and returns a new list with the squared values. The result is stored in the `squared_numbers` variable, which is an object of type `map`. You can convert this object to a list by using the `list()` function, as shown in the example.
## `reduce()`

The `reduce()` function in Python is used to apply a given function to the elements of a sequence (such as a list) and return a single value that is the result of the cumulative computation.

The syntax for `reduce()` is as follows:

```python
result = reduce(function, iterable)
```

where `function` is the function that takes two arguments and returns a value, and `iterable` is the sequence that you want to apply the function to.

Here are some key points to note about the `reduce()` function:

- The function that you pass to `reduce()` should take two arguments and return a value.
- The `reduce()` function applies the given function to the first two elements of the sequence, and then applies the same function to the result and the next element, and so on, until all elements of the sequence have been processed.
- The result of `reduce()` is a single value that is the result of the cumulative computation.
- The `reduce()` function is not a built-in function in Python 3. Instead, it is part of the `functools` module, so you need to import it first before you can use it.

For example, here's how you can use `reduce()` to find the product of all numbers in a list:

```python
from functools import reduce

numbers = [1, 2, 3, 4, 5]
product = reduce(lambda x, y: x*y, numbers)
print(product) # Output: 120
```

In this example, we're using a lambda function to multiply each pair of numbers in the `numbers` list. The `reduce()` function then applies this function to the first two elements of the list, and then applies the same function to the result and the next element, and so on, until all elements of the list have been processed. The result is stored in the `product` variable, which is the product of all the numbers in the list.

## Common pitfalls
Here are some common pitfalls to watch out for when using `map()`, `filter()`, and `reduce()` in Python:

- **Not using a function**: All three functions (`map()`, `filter()`, and `reduce()`) require a function to be passed as the first argument. If you forget to pass a function or pass the wrong function, you'll get a `TypeError`.
- **Forgetting to iterate**: `map()`, `filter()`, and `reduce()` return an iterator object, which means you need to iterate over the object to get the results. If you forget to iterate over the object or try to access its elements directly, you'll get a `TypeError`.
- **Not casting the result**: `map()`, `filter()`, and `reduce()` return iterator objects, which means you need to cast the result to a list, tuple, or other iterable if you want to use it as such. If you forget to cast the result or try to use it as an iterator, you'll get a `TypeError`.
- **Using `map()` and `filter()` together**: Sometimes, people try to use `map()` and `filter()` together to transform and filter a sequence at the same time. While this can be done, it's often more readable and efficient to use a list comprehension or generator expression instead.
- **Using `reduce()` for everything**: While `reduce()` is a powerful tool, it's not always the best choice for the job. In some cases, it can be more readable and efficient to use a loop or list comprehension instead.

By being aware of these pitfalls and carefully testing your code, you can avoid many common errors when using `map()`, `filter()`, and `reduce()` in Python.