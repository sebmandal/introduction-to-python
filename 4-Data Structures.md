# Chapter 4: Data Structures

Data structures are essential for organizing and managing your data in Python programs. Python comes with built-in data structures such as lists, tuples, sets, and dictionaries. In this chapter, we will discuss these data structures and their various operations.

## Lists

A list is a mutable, ordered collection of items. Items in a list can be of any data type, including other lists, and a list can contain items of different data types. Lists are created using square brackets `[ ]` and items are separated by commas.

The way we access elements in a list is by `index`, or `indices` (plural). The first element of a list is index `0`, and the next is `1`. You can access lists from the end by using a `-`. The last element of a list is index of `-1`, and the second last element is `-2`, and so on.

```python
# Creating a list
my_list = [1, 2, 3, "apple", 4.5]

# Accessing items in a list by index
print(my_list[0])   # Output: 1
print(my_list[3])   # Output: apple
print(my_list[-1])  # Output: 4.5
print(my_list[-2])  # Output: apple
```

### List Methods

Lists come with several built-in methods to add, remove, or modify items.

- `append(item)`: Adds an item to the end of the list.
- `insert(index, item)`: Inserts an item at the specified index.
- `remove(item)`: Removes the first occurrence of the item from the list.
- `pop(index)`: Removes and returns the item at the specified index. If no index is provided, it removes and returns the last item.
- `sort()`: Sorts the list items in ascending order (for numbers) or lexicographically (for strings).
- `reverse()`: Reverses the order of items in the list.

```python
my_list = [1, 2, 3]

my_list.append(4)         # Adds 4 to the end of the list
my_list.insert(0, 0)      # Inserts 0 at index 0
my_list.remove(2)         # Removes the first occurrence of 2
last_item = my_list.pop() # Removes and returns the last item (4)

my_list.sort()            # Sorts the list in ascending order
my_list.reverse()         # Reverses the order of items in the list
```

### Slicing Lists

You can extract a portion of a list, known as a slice. Sliced lists start at the given `start` index, and ends at the element before the `end` index. You can slice a list using the following syntax:

```python
sub_list = my_list[start:end]
```

For example:

```python
my_list = [0, 1, 2, 3, 4, 5]

sub_list = my_list[1:4]  # Output: [1, 2, 3]
```

## Tuples

A tuple is an immutable, ordered collection of items. Unlike lists, tuples cannot be modified once they are created. This means that you cannot add, remove, or change items in a tuple. Tuples are created using parentheses `( )` and items are separated by commas.

```python
# Creating a tuple
my_tuple = (1, 2, 3, "apple", 4.5)

# Accessing items in a tuple by index
print(my_tuple[0])   # Output: 1
print(my_tuple[3])   # Output: apple
```

## Sets

A set is an unordered collection of unique items. Sets do not allow duplicates and do not maintain the order of items. Sets are created using curly braces `{ }` and items are separated by commas, or by using the `set()` function.

```python
# Creating a set
my_set = {1, 2, 3, 4, 5}

# Creating a set from a list (removes duplicates)
my_list = [1, 2, 2, 3, 4, 4, 5]
my_set = set(my_list)  # Output: {1, 2, 3, 4, 5}
```

### Set Methods

Sets come with several built-in methods to add, remove, or perform operations on set items.

- `add(item)`: Adds an item to the set.
- `remove(item)`: Removes an item from the set.
- `discard(item)`: Removes an item from the set if it is present (does not raise an error if the item is not found).
- `union(set)`: Returns a new set containing all items from both sets.
- `intersection(set)`: Returns a new set containing the items present in both sets.
- `difference(set)`: Returns a new set containing the items present in the first set but not in the second set.

```python
set1 = {1, 2, 3, 4}
set2 = {3, 4, 5, 6}

set1.add(5)                 # Adds 5 to the set
set1.remove(2)              # Removes 2 from the set
set1.discard(2)             # Removes 2 from the set if it is present

union_set = set1.union(set2)          # Output: {1, 2, 3, 4, 5, 6}
intersection_set = set1.intersection(set2)  # Output: {3, 4}
difference_set = set1.difference(set2)      # Output: {1, 2}
```

## Dictionaries

A dictionary is an unordered collection of key-value pairs. Each key in a dictionary must be unique, and keys can be used to access their corresponding values. Dictionaries are created using curly braces `{ }` and key-value pairs are separated by commas. The key and value of a pair are separated by a colon.

```python
# Creating a dictionary
my_dict = {"name": "John", "age": 25, "city": "New York"}

# Accessing values by key
print(my_dict["name"])  # Output: John
print(my_dict["age"])   # Output: 25
```

### Dictionary Methods

Dictionaries come with several built-in methods to add, remove, or modify key-value pairs.

- `update(key_value_pairs)`: Adds the specified key-value pairs to the dictionary.
- `pop(key)`: Removes and returns the value with the specified key.
- `keys()`: Returns a list of the dictionary's keys.
- `values()`: Returns a list of the dictionary's values.

```python
my_dict = {"name": "John", "age": 25, "city": "New York"}

my_dict.update({"country": "USA", "city": "Boston"})  # Adds a new key-value pair and updates an existing one
age = my_dict.pop("age")  # Removes the "age" key-value pair and returns the value (25)

keys = my_dict.keys()   # Output: ['name', 'city', 'country']
values = my_dict.values()  # Output: ['John', 'Boston', 'USA']
```

In this chapter, we covered various data structures in Python, including lists, tuples, sets, and dictionaries. These data structures allow you to manage and manipulate your data more efficiently. In the next chapter, we will discuss defining functions, function arguments, lambda functions, importing modules, and built-in functions in Python.
