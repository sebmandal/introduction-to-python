# Chapter 6: File Handling

File handling is an important aspect of many Python programs, allowing you to read and write data to and from files. In this chapter, we will discuss opening and closing files, reading and writing files, file modes, and working with directories.

## Opening and Closing Files

Before you can read or write data to a file, you need to open it using the built-in `open()` function. This function takes two arguments: the file path and the file mode. The file mode specifies how the file should be opened (e.g., for reading, writing, or appending). Once you are done working with a file, it's essential to close it using the `close()` method to free up system resources.

```python
# Opening a file for reading (mode: 'r')
file = open("example.txt", "r")

# Perform file operations here

# Closing the file
file.close()
```

It's a best practice to use the `with` statement when working with files, as it automatically handles closing the file for you once the block of code is exited. This helps prevent issues caused by forgetting to close a file.

```python
# Using the with statement to open and close a file
with open("example.txt", "r") as file:
    # Perform file operations here
    pass  # Placeholder statement for an empty block
```

## Reading and Writing Files

Once you have opened a file, you can read its contents using various methods, such as `read()`, `readline()`, and `readlines()`.

- `read()`: Reads the entire contents of the file as a single string.
- `readline()`: Reads the next line of the file, including the newline character.
- `readlines()`: Reads all lines in the file and returns a list of strings.

```python
# Reading the entire contents of a file
with open("example.txt", "r") as file:
    content = file.read()
    print(content)

# Reading a file line by line using readline()
with open("example.txt", "r") as file:
    line = file.readline()
    while line:
        print(line, end="")
        line = file.readline()

# Reading all lines in a file using readlines()
with open("example.txt", "r") as file:
    lines = file.readlines()
    for line in lines:
        print(line, end="")
```

To write data to a file, you can use the `write()` method. This method takes a single argument: the string to be written to the file.

```python
# Writing to a file
with open("output.txt", "w") as file:
    file.write("Hello, World!\n")
```

If you want to add data to an existing file without overwriting its contents, use the append mode (`'a'`) when opening the file.

```python
# Appending to a file
with open("output.txt", "a") as file:
    file.write("This line was appended to the file.\n")
```

## File Modes

When opening a file, you can specify the mode in which the file should be opened. The most common file modes are:

- `'r'`: Read mode (default). Opens the file for reading.
- `'w'`: Write mode. Opens the file for writing, creating it if it does not exist, or truncating it (deleting its contents) if it does.
- `'a'`: Append mode. Opens the file for writing, creating it if it does not exist, or appending to it if it does.
- `'x'`: Exclusive creation mode. Opens the file for exclusive creation, raising an error if the file already exists.

Additionally, you can add a `'b'` to the mode to open the file in binary mode (e.g., `'rb'`, `'wb'`, `'ab'`). This is useful when working with non-text files, such as images or compressed archives.

## Working with Directories

Python's `os` module provides various functions for working with directories.

- `os.getcwd()`: Returns the current working directory as a string.
- `os.chdir(path)`: Changes the current working directory to the specified path.
- `os.mkdir(path)`: Creates a new directory at the specified path.
- `os.rmdir(path)`: Removes the specified directory (must be empty).
- `os.listdir(path)`: Returns a list of all files and directories in the specified path.

```python
import os

# Get the current working directory
current_dir = os.getcwd()
print(current_dir)

# Change the current working directory
os.chdir("example_directory")

# Create a new directory
os.mkdir("new_directory")

# Remove a directory
os.rmdir("new_directory")

# List all files and directories in the current directory
files_and_dirs = os.listdir()
print(files_and_dirs)
```

In this chapter, we covered file handling in Python, including opening and closing files, reading and writing files, file modes, and working with directories. With these skills, you can efficiently manage and manipulate data stored in files as part of your Python programs. In the next chapter, we will discuss error handling, including exceptions, try-except blocks, raising exceptions, and creating custom exceptions.
