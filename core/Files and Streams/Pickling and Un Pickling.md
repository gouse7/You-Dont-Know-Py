
## Pickling (Object Serialization)

- Let us assume there exists an object which contains multiple values. To save or write the object data from main memory into a file in secondary memory, using `write()` or `writelines()` would transfer the values one by one, resulting in a time-consuming process.
- To overcome this time-consuming process, we can use the concept of Pickling.
- Pickling allows us to save or write the entire object data from main memory into a file in secondary memory with a single write operation.

### Definition of Pickling:
The process of saving or transferring the entire object content from main memory into a file in secondary memory by performing a single write operation is called Pickling.
Pickling concept participates in write operations.

#### Steps for implementing Pickling Concept:

1. Import the `pickle` module.
2. Choose the file name and open it in write mode.
3. Create an object with a collection of values (iterable object).
4. Use the `dump()` function of the `pickle` module. The `dump()` function saves the content of any object into the file with a single write operation.
   Syntax: `pickle.dump(object, filepointer)`
5. Note that Pickling concept always takes the file in Binary Format.

## Example
```python
import pickle

# Creating an object
data = [1, 2, 3, 4, 5]

# Pickling the object and saving it to a file
with open('data.pickle', 'wb') as file:
    pickle.dump(data, file)
```


---

## Un-Pickling (Object De-Serialization)

- Let us assume there exists a record with multiple values in a file in secondary memory. To read or transfer the entire record content from the file, if we use `read()` or `readlines()`, it would read the record values one by one, resulting in a time-consuming process.
- To overcome this time-consuming process, we can use the concept of Un-pickling.
- Un-pickling allows us to read or transfer the entire record content from the file in secondary memory into the object in main memory with a single read operation.

### Definition of Un-Pickling:
The process of reading or transferring the entire record content from a file in secondary memory into the object in main memory by performing a single read operation is called Un-Pickling.
Un-Pickling concept participates in read operations.

#### Steps for implementing Un-Pickling Concept:

1. Import the `pickle` module.
2. Choose the file name and open it in read mode.
3. Use the `load()` function of the `pickle` module. The `load()` function is used to transfer or load the entire record content from the file in secondary memory into the object in main memory.
   Syntax: `objname = pickle.load(filepointer)`
4. Note that Un-Pickling concept always takes the file in Binary Format.


## Example:
```python
import pickle

# Unpickling the object from the file
with open('data.pickle', 'rb') as file:
    loaded_data = pickle.load(file)

# Printing the loaded object
print(loaded_data)
```

## Random File Access Example:
```python
import pickle

# Creating objects
person1 = {'name': 'Alice', 'age': 25}
person2 = {'name': 'Bob', 'age': 30}
person3 = {'name': 'Charlie', 'age': 35}

# Pickling the objects and saving them to a file
with open('people.pickle', 'wb') as file:
    pickle.dump(person1, file)
    pickle.dump(person2, file)
    pickle.dump(person3, file)

# Random access to the pickled objects in the file
with open('people.pickle', 'rb') as file:
    # Seek to the start of the second object
    file.seek(1 * pickle.DEFAULT_PROTOCOL)

    # Unpickling the second object
    loaded_person2 = pickle.load(file)

# Printing the loaded object
print(loaded_person2)
```

In the random file access example, we pickle multiple objects to a file and then use `seek()` to move to a specific position in the file before unpickling the desired object. This allows us to access and load a specific object from the file without loading all the objects sequentially.
