# Chapter 5: Functions and Modules

Functions and modules are essential components of Python programming, allowing you to organize your code into reusable, modular blocks. In this chapter, we will discuss defining functions, function arguments, lambda functions, importing modules, and built-in functions.

## Defining Functions

A function is a block of organized, reusable code that performs a specific task. Functions help you to break down your code into smaller, more manageable pieces, making it easier to understand, maintain, and reuse.

In Python, you can define a function using the `def` keyword, followed by the function name, a pair of parentheses, and a colon. The function's code block is then indented.

```python
def greet():
    print("Hello, World!")

# Calling the function
greet()  # Output: Hello, World!
```

### Function Arguments

You can pass values, known as arguments, into a function. Arguments allow you to customize the behavior of a function based on the provided input. To define a function with arguments, simply add the argument names inside the parentheses when declaring the function.

```python
def greet(name):
    print("Hello, " + name + "!")

# Calling the function with an argument
greet("John")  # Output: Hello, John!
```

You can define a function with multiple arguments, separated by commas.

```python
def add(x, y):
    result = x + y
    print(f"{x} + {y} = {result}")

# Calling the function with multiple arguments
add(3, 5)  # Output: 3 + 5 = 8
```

### Return Values

Functions can also return values, allowing you to use the result of a function elsewhere in your code. To return a value, use the `return` keyword followed by the value or expression to be returned.

```python
def add(x, y):
    return x + y

# Calling the function and storing the returned value
result = add(3, 5)
print(result)  # Output: 8
```

## Lambda Functions

Lambda functions are small, anonymous functions that can be created using the `lambda` keyword. They are useful for creating simple, one-time-use functions that you don't want to define with a full `def` statement.

Lambda functions can have any number of arguments but can only contain a single expression.

```python
# Defining a lambda function to add two numbers
add = lambda x, y: x + y

# Calling the lambda function
result = add(3, 5)
print(result)  # Output: 8
```

## Importing Modules

A module is a file containing Python definitions and statements. Python comes with a large standard library containing built-in modules that provide a wide range of functionality.

You can import a module using the `import` keyword, followed by the module name.

```python
import math

# Using functions from the imported module
result = math.sqrt(25)
print(result)  # Output: 5.0
```

You can also import specific functions or objects from a module using the `from ... import ...` statement.

```python
from math import sqrt

# Using the imported function directly
result = sqrt(25)
print(result)  # Output: 5.0
```

## Built-in Functions

Python provides several built-in functions that are available by default, without the need to import any modules. Some common built-in functions include:

- `len(obj)`: Returns the number of items in a sequence (e.g., list, tuple, string) or mapping (e.g., dictionary).
- `min(iterable)`: Returns the smallest item in an iterable or the smallest of two or more arguments.
- `max(iterable)`: Returns the largest item in an iterable or the largest of two or more arguments.
- `sum(iterable)`: Returns the sum of all items in an iterable.
- `abs(x)`: Returns the absolute value of a number.
- `round(x, n)`: Rounds a number `x` to `n` decimal places (default is 0).

The following built-in type functions throw errors if the types are unable to be converted. Some common type functions include:

- `int(x)`: Turns a value into an integer.
- `float(x)`: Turns a value into a float.
- `string(x)`: Turns a value into a string.

```python
my_list = [1, 2, 3, 4, 5]

length = len(my_list)
minimum = min(my_list)
maximum = max(my_list)
total = sum(my_list)

print(length)  # Output: 5
print(minimum)  # Output: 1
print(maximum)  # Output: 5
print(total)    # Output: 15

num = -3.14159
print(abs(num))    # Output: 3.14159
print(round(num, 2))  # Output: -3.14

num = "5"
print(type(num)) # Output: string
num = int(num)
print(type(num)) # Output: int
```

In this chapter, we covered defining functions, function arguments, lambda functions, importing modules, and built-in functions in Python. With these tools, you can create modular, reusable code and take advantage of Python's extensive standard library. In the next chapter, we will discuss file handling, including opening and closing files, reading and writing files, file modes, and working with directories.
