# Key Concepts

Code things shown in this lab:
- String function, string methods
- List function, list creation syntax
- Methods for modifying / interacting with a list
- List utility functions
- Tuple syntax
- Dict function, dict creation syntax
- Methods for modifying / interacting with a dictionary


## Arrays
- "An array is a data structure consisting of a collection of elements (values or variables), each identified by at least one array index or key. Depending on the language, array types may overlap (or be identified with) other data types that describe aggregates of values, such as lists and strings. Array types are often implemented by array data structures, but sometimes by other means, such as hash tables, linked lists, or search trees" (Busbee and Braunschweig, "[Arrays and Lists](https://press.rebus.community/programmingfundamentals/chapter/arrays-and-lists/)")
-  "In Python, the built-in array data structure is a list" (Busbee and Braunschweig, "[Arrays and Lists](https://press.rebus.community/programmingfundamentals/chapter/arrays-and-lists/)")

For more on array structures:
- Kenneth Leroy Busbee and Dave Braunschweig, "[Arrays and Lists](https://press.rebus.community/programmingfundamentals/chapter/arrays-and-lists/)" in *Programming Fundamentals*

## Dictionaries

## Index, Indexing

## Iteration

## Key-Value Pairs

## Lists
- "An array is a data structure consisting of a collection of elements (values or variables), each identified by at least one array index or key...In Python, the built-in array data structure is a list" (Busbee and Braunschweig, "[Arrays and Lists](https://press.rebus.community/programmingfundamentals/chapter/arrays-and-lists/)")
- An list is a single-dimension array

In Python, we can create lists using square brackets `[]` or the `list()` function.

Python examples:
```Python
# creating a list of numbers using square brackets
numbers = [1, 3, 5, 7, 9]

# checking data type
type(numbers)
```

```Python
# creating a list of strings using the list function
words = list(("apple", "banana", "blueberry", "cherry")) # note the double round bracket syntax

# check data type
type(words)
```

A few other preliminary notes on lists in Python:
- We can check the number of elements in a list using `len()` 
- We can access specific elements in a list using an index operator (`[]`) and position (numeric value)
- We can add values to a list using the `.append()`, `.insert()`, and `.extend()` methods
- We can isolate elements in a list using `.pop()`
- We can remove elements from a list using `.remove()` or `del`
- We can test for membership using the `in` operator
- We can sort elements in a list using `.sort()`, `sorted()`, and `.reverse()`
- We can access descriptive statistics for list values using `sum()`, `max()`, and `min()`

TABLE WITH LIST METHODS

More on arrays/lists (general):
- Kenneth Leroy Busbee and Dave Braunschweig, "[Arrays and Lists](https://press.rebus.community/programmingfundamentals/chapter/arrays-and-lists/)" in *Programming Fundamentals*

More on lists in Python:
- [W3Schools, Python Lists](https://www.w3schools.com/python/python_lists.asp)

## Nested Lists, Sublists

## Strings
- "A string data type is traditionally a sequence of characters, either as a literal constant or as some kind of variable...A string is generally considered a data type and is often implemented as an array data structure of bytes (or words) that stores a sequence of elements, typically characters, using some character encoding" (Busbee and Braunschweig, "[String Data Type](https://press.rebus.community/programmingfundamentals/chapter/string-data-type/)")
- "Like many other popular programming languages, strings in Python are arrays of bytes representing unicode characters. However, Python does not have a character data type, a single character is simply a string with a length of 1. Square brackets can be used to access elements of the string" ([W3Schools, Python Strings](https://www.w3schools.com/python/python_strings.asp))

Python examples:
```Python
# creating a string variable
x = "Hello World!"

# checking data type
type(x)
```

```Python
# converting to a string data type
y = 7
y = str(y)

# checking data type
type(y)
```

More on strings (general):
- Kenneth Leroy Busbee and Dave Braunschweig, "[String Data Type](https://press.rebus.community/programmingfundamentals/chapter/string-data-type/)" in *Programming Fundamentals*

More on strings in Python:
- [W3Schools, Python Strings](https://www.w3schools.com/python/python_strings.asp)

## Tuples
- "Tuples are used to store multiple items in a single variable...A tuple is a collection which is ordered and unchangeable. Tuples are written with round brackets...and allow duplicate values" ([W3Schools, Python Tuples](https://www.w3schools.com/python/python_tuples.asp))

We can create a tuple in Python using the round bracket syntax `(())` or the `tuple()` method.

```Python
# creating a tuple using round brackets
sample = ("apple", "banana", "blueberry")

# checking data type
type(sample)
```

```Python
# creating tuple using tuple method
sample2 = tuple(("apple", "banana", "blueberry"))

# check data type
type(sample2)
```

Tuples are indexed, so we can access individual items using an index operator and value.

```Python
# access first item in sample tuple
sample[0]
```

Additional resources:
- [W3Schools, Python Tuples](https://www.w3schools.com/python/python_tuples.asp)
