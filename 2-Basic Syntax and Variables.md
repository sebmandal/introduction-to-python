# Chapter 2: Basic Syntax and Variables

In this chapter, we will introduce you to the basic syntax of Python and explain how to work with variables and data types. These foundational concepts will help you to write, read, and understand Python code more effectively.

## Comments

Comments are lines of text in your code that are not executed by the Python interpreter. They are useful for providing explanations or notes about your code, making it easier to understand and maintain. In Python, you can create comments using the hash symbol (#).

```python
# This is a single-line comment

# You can also use comments
# to break up your code into
# more readable sections
```

Python does not have a specific syntax for multi-line comments, but you can use triple quotes (either single or double) to create a multi-line string, which can serve as a multi-line comment if not assigned to a variable.

```python
'''
This is a
multi-line
comment
'''

"""
Another example of a
multi-line
comment
"""
```

## Variables and Data Types

A variable is a named container that stores a value in your program. You can think of it as a label attached to a piece of data. In Python, you can create a variable by assigning a value to a name using the equal sign (=).

```python
x = 10  # Creates a variable named x with the value 10
```

Python has several built-in data types, including:

- **Integers**: Whole numbers, such as 42 or -7
- **Floats**: Decimal numbers, such as 3.14 or -0.001
- **Booleans**: True or False values
- **Strings**: Sequences of characters, such as "Hello, World!"

You can determine the data type of a variable using the `type()` function.

```python
x = 10
y = 3.14
z = "Hello, World!"
w = True

print(type(x))  # Output: <class 'int'>
print(type(y))  # Output: <class 'float'>
print(type(z))  # Output: <class 'str'>
print(type(w))  # Output: <class 'bool'>
```

In Python, you don't need to declare a variable's data type explicitly, as the language is dynamically typed. This means that Python automatically determines the data type based on the assigned value, and you can change a variable's data type by assigning a new value of a different type.

```python
x = 10          # x is an integer
x = "Python"    # x is now a string
```

## Arithmetic Operators

Python supports various arithmetic operators to perform calculations with numeric values.

- Addition: `+`
- Subtraction: `-`
- Multiplication: `*`
- Division: `/`
- Modulus (remainder): `%`
- Exponentiation: `**`
- Floor division (quotient): `//`

Examples:

```python
x = 5
y = 3

print(x + y)  # Output: 8
print(x - y)  # Output: 2
print(x * y)  # Output: 15
print(x / y)  # Output: 1.6666666666666667
print(x % y)  # Output: 2
print(x ** y) # Output: 125
print(x // y) # Output: 1
```

## String Manipulation

Strings are sequences of characters enclosed in either single or double quotes. Python provides several built-in functions and operators to manipulate strings.

Concatenation:

```python
first_name = "John"
last_name = "Doe"

full_name = first_name + " " + last_name
print(full_name)  # Output: John Doe
```

String repetition:

```python
repeat_string = "abc" * 3
print(repeat_string)  # Output: abcabcabc
```

String slicing:

```python
text = "Python Programming"

# Extract a substring from the original string
# using the syntax: text[start:end]
print(text[0:6])   # Output: Python
print(text[7:18])  # Output: Programming
```

## Basic Input and Output

You can read input from the user using the `input()` function and display output using the `print()` function.

Reading input:

```python
name = input("Enter your name: ")
print("Hello, " + name + "!")
# Output: Hello, [name]!
```

Displaying output:

```python
x = 10
y = 5
result = x + y

print("The sum of ", x, " and ", y, " is ", result)
# Output: The sum of 10 and 5 is 15
```

An alternative to using `+` in prints, is to use `formatted strings`. You can do this by putting `f` in front of your strings, and putting code inside `{}` tags in the string.

Reading input using formatted strings:

```python
name = input("Enter your name: ")
print(f"Hello, {name}!")
# Output: Hello, [name]!
```

Displaying output:

```python
x = 10
y = 5
result = x + y

print(f"The sum of {x} and {y} is {result}")
# Output: The sum of 10 and 5 is 15
```

In the next chapter, we will explore control structures in Python, including conditional statements and looping constructs, to add more complex logic and behavior to your programs.
