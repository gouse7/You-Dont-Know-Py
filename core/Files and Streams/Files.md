## Definition
- A file is a collection of records.
- Files reside in secondary memory (HDD).
- Technically, a file name is a named location in secondary memory.
- The purpose of files is to achieve data persistence.
- All the object data in the main memory becomes records in the file of secondary memory, and the records in the file of secondary memory become the objects in the main memory.

## Types of Files in Python

In Python programming, there are two types of files:

1. Text Files:
   - Text files contain alphabets, digits, and symbols.
   - Text files are denoted by the letter 't'.
   - By default, every file is treated as a text file.
   - Examples of text files: `.c`, `.cpp`, `.txt`, `.docx`, `.xlsx`, `.py`, etc.

2. Binary Files:
   - Binary files contain data in binary form.
   - Binary files are denoted by the letter 'b'.
   - Examples of binary files: All types of image files (`.jpeg`, `.gif`, `.jpg`, `.png`), all types of audio and video files.
  
## Operations on Files

### Write Operation:
- The purpose of the write operation is to transfer or save the object data from the main memory as a record in the file of secondary memory.
- Steps for performing a write operation:
  1. Choose the File Name.
  2. Open the File Name in Write Mode.
  3. Perform a cycle of Write Operations.
- Exceptions encountered during write operations:
  - IOError
  - OSError
  - FileExistError

### Read Operation:
- The purpose of the read operation is to transfer or read the record from the file of secondary memory into the object of the main memory.
- Steps for performing a read operation:
  a. Choose the file name.
  b. Open the file name in Read Mode.
  c. Perform a cycle of read operations.
- Exceptions encountered during read operations:
  - FileNotFoundError
  - EOFError

## File Opening Modes in Python

File opening modes in Python determine how a file is opened and what operations can be performed on it. There are 8 file opening modes available in Python:

1. **`'r'` (Read Mode)**:
   - Opens the file in read mode.
   - Performs read operations on the file.
   - If the file does not exist, a `FileNotFoundError` is raised.
   - This is the default file mode.

2. **`'w'` (Write Mode)**:
   - Creates a new file or opens an existing file in write mode.
   - Allows write operations on the file.
   - If a new file is chosen, it is created and opened in write mode.
   - If an existing file is chosen, the existing data is overlapped with new data.

3. **`'a'` (Append Mode)**:
   - Creates a new file or opens an existing file in append mode.
   - Allows write operations on the file.
   - If a new file is chosen, it is created and opened in write mode.
   - If an existing file is chosen, new data is appended to the existing data.

4. **`'r+'` (Read and Write Mode):**
   - Opens the file in read mode.
   - If the file does not exist, a `FileNotFoundError` is raised.
   - Allows both read and write operations on the file.

5. **`'w+'` (Write and Read Mode)**:
   - Creates a new file or opens an existing file in write mode.
   - Allows write operations on the file.
   - If a new file is chosen, it is created and opened in write mode.
   - If an existing file is chosen, the existing data is overlapped with new data.
   - Allows both write and read operations on the file.

6. **`'a+'` (Append and Read Mode)**:
   - Creates a new file or opens an existing file in append mode.
   - Allows write operations on the file.
   - If a new file is chosen, it is created and opened in write mode.
   - If an existing file is chosen, new data is appended to the existing data.
   - Allows both write and read operations on the file.

7. **`'x'` (Exclusive Creation Mode**):
   - Creates a new file exclusively in write mode.
   - If the file already exists, a `FileExistsError` is raised.

8. **`'x+'` (Exclusive Creation and Read Mode)**:
   - Creates a new file exclusively in write mode.
   - If the file already exists, a `FileExistsError` is raised.
   - Allows both write and read operations on the file.

Note: Each mode supports different combinations of read and write operations. The selected mode determines the behavior of file operations.


Next,
## [File Open, Read and Writing](File%20Open,%20Read%20and%20Writing.md)

## [Pickling and Un Pickling](Pickling%20and%20Un%20Pickling.md)

## [Working with CSV Files](Working%20with%20CSV%20Files.md)

