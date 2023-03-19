# Chapter 3: Control Structures

Control structures allow you to add logic and flow control to your Python programs. In this chapter, we will discuss conditional statements, looping constructs, and loop control statements.

## Conditional Statements (if, elif, else)

Conditional statements allow you to execute different parts of your code based on whether specific conditions are met. In Python, we use the `if`, `elif`, and `else` keywords to define conditional statements.

The `if` statement checks whether a condition is `True`. If it is, the indented block of code following the `if` statement is executed. If the condition is `False`, the code block is skipped.

```python
x = 10

if x > 5:
    print("x is greater than 5")
```

The `else` statement can be used in conjunction with `if` to define a block of code that will be executed if the `if` condition is `False`.

```python
x = 3

if x > 5:
    print("x is greater than 5")
else:
    print("x is not greater than 5")
```

The `elif` (short for "else if") statement allows you to check multiple conditions in a single `if` statement. It is used between `if` and `else` to test additional conditions if the previous condition(s) are `False`.

```python
x = 10

if x > 20:
    print("x is greater than 20")
elif x > 10:
    print("x is greater than 10 but not greater than 20")
else:
    print("x is not greater than 10 or 20")
```

## Looping (for, while)

Loops enable you to execute a block of code multiple times. Python supports two types of loops: `for` loops and `while` loops.

### for Loop

A `for` loop iterates over a sequence (such as a list, tuple, or string) and executes the indented code block for each item in the sequence.

```python
fruits = ["apple", "banana", "orange"]

for fruit in fruits:
    print(fruit)
```

You can also use the `range()` function to generate a sequence of numbers for iteration.

```python
# The range() function generates a sequence of numbers from 0 to 4 (5-1)
for i in range(5):
    print(i)
```

### while Loop

A `while` loop repeatedly executes a block of code as long as its condition remains `True`.

```python
x = 0

while x < 5:
    print(x)
    x += 1  # Increment x by 1
# Output: 0 1 2 3 4
```

## Loop Control (break, continue)

Loop control statements allow you to alter the flow of loops. The `break` and `continue` keywords are used for this purpose.

### break

The `break` statement immediately terminates the current loop and resumes execution after the loop.

```python
for i in range(10):
    if i == 5:
        break
    print(i)
# Output: 0 1 2 3 4
```

### continue

The `continue` statement skips the remaining code in the current iteration of the loop and starts the next iteration.

```python
for i in range(10):
    if i % 2 == 0:  # Check if i is even
        continue
    print(i)
# Output: 1 3 5 7 9
```

In this chapter, we covered control structures in Python, including conditional statements and looping constructs. With these tools, you can create more complex and dynamic programs. In the next chapter, we will explore data structures such as lists, tuples, sets, and dictionaries, which enable you to organize and manipulate your data more efficiently.
