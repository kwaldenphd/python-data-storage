# Data Storage in Python (strings, lists, tuples, dictionaries)

CC STATEMENT

GOALS/OVERVIEW

ACKNOWLEDGEMENTS

# Table of Contents
- [Lecture & Live Coding](#lecture--live-coding)
- [Key Concepts](#key-concepts)
- [Lab Notebook Template](#lab-notebook-template)


# Lecture & Live Coding

# Key Concepts

[Click here](https://github.com/kwaldenphd/python-data-storage/blob/main/key-concepts.md) for a full list of key concepts and definitions for this lab.

# Lab Notebook Template

# BIG PICTURE PSEUDOCODE OVERVIEW

Data storage concepts/options big picture

What those look like in Python:
- String, list, tuple, set, dictionary

# Strings

- Structure big picture
- Examples we’ve seen before
- Creating them 
- Methods (title)
- Concatenation
- Length/access
- Other common operations (len, properties, sort, concatenation, in operator, search)
  * LAY GROUNDWORK FOR ITERATION HERE
  * Thread in if-else and comparison operators

## Comprehension Check

## Application


# Lists

- Structure big picture
- Examples we've seen before (composite variables)
- Creating them
- Length/access
- Modifying (growing, deleting, inserting, appending)
- Other common operations (length, sort, concatenation, copying, in operator, search, utility functions, max/min, sum)
- Nested lists, sublists (selection syntax, modifying)

- "An array is a data structure consisting of a collection of elements (values or variables), each identified by at least one array index or key...In Python, the built-in array data structure is a list" (Busbee and Braunschweig, "[Arrays and Lists](https://press.rebus.community/programmingfundamentals/chapter/arrays-and-lists/)")
- An list is a single-dimension array

## Creating Lists

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

## List Properties

We can check the number of values or elements in a list using the length function `len()`.

PYTHON EXAMPLE

We can access specific elements in a list using an index operator (`[]`) and position (numeric value).

PYTHON EXAMPLE

## List Methods

TABLE WITH LIST METHODS

## Modifying Lists

We can modify elements in a list using index and assignment operators.

PYTHON EXAMPLE

We can add values to a list using the `.append()`, `.insert()`, and `.extend()` methods. 
- `.append()` adds values to the end of a list
- `.insert()` adds a value at a specific position
- `.extend()` extends the numeric range for a list of integers

PYTHON EXAMPLES

We can isolate elements in a list using the `.pop()` method.

PYTHON EXAMPLE

We can remove elements from a list using the `del` statement.

PYTHON EXAMPLE

## Working With Lists

in operator

copying, concatenation

Sorting, reversing (INPLACE)

Summary statistics 

## Additional Resources

More on arrays/lists (general):
- Kenneth Leroy Busbee and Dave Braunschweig, "[Arrays and Lists](https://press.rebus.community/programmingfundamentals/chapter/arrays-and-lists/)" in *Programming Fundamentals*

More on lists in Python:
- [W3Schools, Python Lists](https://www.w3schools.com/python/python_lists.asp)

## Comprehension Check

## Application

# Tuples

- "Tuples are used to store multiple items in a single variable...A tuple is a collection which is ordered and unchangeable. Tuples are written with round brackets...and allow duplicate values" ([W3Schools, Python Tuples](https://www.w3schools.com/python/python_tuples.asp))

## Creating Tuples

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

## Tuple Properties

LEN FUNCTION

Tuples are indexed, so we can access individual items using an index operator and value.

```Python
# access first item in sample tuple
sample[0]
```

## Modifying Tuples

MODIFYING TUPLES

For more on tuples in Python:
- [W3Schools, Python Tuples](https://www.w3schools.com/python/python_tuples.asp)

## Comprehension Check

## Application

# Sets

## Comprehension Check

# Dictionaries

- Big picture concept
- Structure
- Creating
- Accessing
- Modifying
- More iteration/loop groundwork with keys, items, values methods

## Comprehension Check

## Application

# Putting It All Together

# Lab Notebook Questions
