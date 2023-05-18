
- **CSV**: Comma Separated Values, a simple file format used to store tabular data.
- CSV files store tabular data in plain text, with each line representing a data record and fields separated by commas.
- Python provides the `csv` module for working with CSV files.

## Writing to CSV Files

### Using `csv.writer` class object:

- `csv.writer` class object is used to insert data into a CSV file.
- To create a `csv.writer` object, use `writer()` function from the `csv` module.
- Functions for writing:
  - `writerow()`: Writes a single row at a time, can be a field row or a data row.
  - `writerows()`: Writes multiple rows at once (list, tuple, set, or frozenset).
### Example
```python
import csv

# Example data
data = [
    ['Name', 'Age', 'City'],
    ['John', '25', 'New York'],
    ['Alice', '30', 'London'],
    ['Bob', '35', 'Paris']
]

# Writing to CSV file
with open('data.csv', 'w', newline='') as file:
    writer = csv.writer(file)
    writer.writerows(data)

```

### Using `csv.DictWriter` class object:

- `csv.DictWriter` class object is used to insert dictionary data into a CSV file.
- To create a `csv.DictWriter` object, use `DictWriter()` function from the `csv` module.
- Functions for writing:
  - `writeheader()`: Writes the first row with pre-specified field names.
  - `writerows()`: Writes dictionary values as separate rows.
### Example
```python
import csv

# Example data as dictionaries
data = [
    {'Name': 'John', 'Age': '25', 'City': 'New York'},
    {'Name': 'Alice', 'Age': '30', 'City': 'London'},
    {'Name': 'Bob', 'Age': '35', 'City': 'Paris'}
]

# Field names for CSV header
fieldnames = ['Name', 'Age', 'City']

# Writing to CSV file
with open('data.csv', 'w', newline='') as file:
    writer = csv.DictWriter(file, fieldnames=fieldnames)
    writer.writeheader()
    writer.writerows(data)

```

## Reading from CSV Files

- There are two classes provided by the `csv` module for reading data from CSV files:
  - `csv.reader`: Reads data records from a CSV file.
  - `csv.DictReader`: Reads data from a CSV file where data is in dictionary format.

### Using `csv.reader` class object:

- Create a `csv.reader` object using `csv.reader(file_pointer)`.
- Read data records from the CSV file.
### Example
```python
import csv

# Reading from CSV file
with open('data.csv', 'r') as file:
    reader = csv.reader(file)
    for row in reader:
        print(row)

```

### Using `csv.DictReader` class object:

- Create a `csv.DictReader` object using `csv.DictReader(file_pointer)`.
- Read data from the CSV file where data is in dictionary format (Key, Value pairs).

### Example

```python
import csv

# Reading from CSV file
with open('data.csv', 'r') as file:
    reader = csv.DictReader(file)
    for row in reader:
        print(row)

```
