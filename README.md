# Data Structures in Python

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

PYTHON DATA TYPE DIAGRAM

Up to this point, we've been working with what are called "primitive" data types in Python. These include `integer`, `float`, `string`, and `Boolean`.

But we can imagine scenarios where we want to be able to work with more complex data structures or more complex ways of storing and accessing information in a programming language. 

In this lab, we're going to focus on some of the one-dimensional (or linear) data structures available to us in Python. These include `strings`, `lists`, `tuples`, `sets`, and `dictionaries`.

TABLE WITH EXAMPLES/SYNTAX

## Linear Arrays

ARRAY DIAGRAM

"An array is a data structure consisting of a collection of elements (values or variables), each identified by at least one array index or key. Depending on the language, array types may overlap (or be identified with) other data types that describe aggregates of values, such as lists and strings. Array types are often implemented by array data structures, but sometimes by other means, such as hash tables, linked lists, or search trees" (Busbee and Braunschweig, "[Arrays and Lists](https://press.rebus.community/programmingfundamentals/chapter/arrays-and-lists/)")

"In computer science, an array is a data structure consisting of a collection of elements (values or variables), each identified by at least one array index or key...The simplest type of data structure is a linear array, also called one-dimensional array" ([Wikipedia, "Array (data structure)](https://en.wikipedia.org/wiki/Array_(data_structure))")

We can think of arrays as one-dimensional, linear data structures made up of a collection of items. As the definitions note, we can access specific elements in the array by using an index or key value. 

"In Python, the built-in array data structure is a list" (Busbee and Braunschweig, "[Arrays and Lists](https://press.rebus.community/programmingfundamentals/chapter/arrays-and-lists/)"). Python also includes a few other built-in array-like data structures, including `sets` and `tuples`. We'll come back to these later in this lab. We can also think of string objects, which are a sequence of characters, as a type of one-dimiensional, linear array.

These **one-dimensional or linear array structures** have a few key properties that differentiate the structures and shape how we can interact with or manipulate them in a programming environment.

Those properties include:
- Mutable: Can values in the structure be changed once it has been created or assigned to a variable?
- Order: Does the order of values in the structure have meaning/significance, or is order not significant?
- Indexing/Slicing: Can values in the structure be accessed using their position or index? Can we isolate values in the structure using their position?
- Duplicates: Does the structure allow duplicate values?

How these properties show up for Python's built-in data structures:

PYTHON ARRAY COMPARISON DIAGRAM

Each structure has its own specific vocabulary and syntax, but some common operations we can use with these structures:
- Getting number of values in the structure (using the `len()` function)
- For structures that are mutable, adding, modifying, and removing values
- Sorting values in the structure
- Testing for membership, if specific value(s) are present in the structure (using the `in` and `not in` operators)
- For structures that are ordered or indexed, accessing elements using their position

### Index/Indexing and Counting in Python

DIAGRAM

In Python, **indexing** allows us to refer to individual values in specific data structures using their position.

NOTE: Python (and many other programming languages) are **zero-indexed**, which means counting for index positions begins at `0`.

Let's use the example of a list of strings:

```Python
# list of string objects
fruits = ["apple", "banana", "blueberry", "cherry"]

# check data type
type(fruits)
```

We can determine the number of elements in the list using the `len()` function.

```Python
len(fruits)
```

Remember Python starts at `0` and counts left-to-right. We can access specific values using their position.

```Python
# access first value 
fruits[0]

# access second value
fruits[1]

# access third value
fruits[2]
```

Python lists also support negative indexing- we can use negative index values to count right-to-left. 
- NOTE: Negative indexing starts counting at `-1`

```Python
# access last value
fruits[-1]

# access next to last value
fruits[-2]
```

We can also use the `.index()` method to output the position for specific values (if they are present in the structure).

```Python
# return index for cherry
print("The index for cherry is ", fruits.index("cherry"))

# return index for pear
print("The index for pear is ", fruits.index("pear"))
```

The last line of the program returns an `IndexError` message because `pear` is not a value in the list.

We can test for membership using the `in` and `not in` operators.

```Python
# test if apple is in list
"apple" in fruits

# test if blueberry is NOT in list
"blueberry" not in fruits
```

The `in` and `not in` operators return Boolean `True` or `False` values.

We can also use this index syntax with string objects.

```Python
# create string variable
message = "Hello world!"

# return number of characters in string
len(message)

# access first character in string
message[0]

# access last character in string
message[-1]

# test if character x is in string
'x' in message # returns false

# test if symbol % is NOT in string
'%' not in message # returns true
```

## Associative Arrays

DIAGRAM

The other primary type of array we can encounter is an **associative array**, "an abstract data type that stores a collection of (key, value) pairs, such that each possible key appears at most once in the collection" ([Wikpedia, Associative Array](https://en.wikipedia.org/wiki/Associative_array))

Python stores associate arrays using the **dictionary** data structure. Python dictionaries consist of key-value pairs, where the key is working as an identifier or index.

A preliminary example in Python:

```Python
# create dictionary
english_to_french = {
  'one': 'un',
  'two': 'deux',
  'three': 'trois',
  'four': 'quatre',
  'five': 'cinq'
}

# check data type
type(english_to_french)
```

We can use the index operator (`[]`) and key values to select specific values in the dictionary.

```Python
# access value for one key
english_to_french['one']

# access value for five key
english_to_french['five']

# access value for asdf key
english_to_french['asdf']
```

The last line will return a `KeyError` because `asdf` is not a key in this dictionary.

We can use the `.keys()` and `.values()` methods to output all of the keys or values in a dictionary.

```Python
# output keys
print(english_to_french.keys())

# output values
print(english_to_french.values())
```

## Comprehension Check

## Application

# Specific Data Structures

PYTHON DATA TYPES DIAGRAM

Before we dive into more detail on these data structures in Python, remember some properties include:
- Mutable: Can values in the structure be changed once it has been created or assigned to a variable?
- Order: Does the order of values in the structure have meaning/significance, or is order not significant?
- Indexing/Slicing: Can values in the structure be accessed using their position or index? Can we isolate values in the structure using their position?
- Duplicates: Does the structure allow duplicate values?

How these properties show up for Python's built-in data structures:

PYTHON ARRAY COMPARISON DIAGRAM

Each structure has its own specific vocabulary and syntax, but some common operations we can use with these structures:
- Getting number of values in the structure (using the `len()` function)
- For structures that are mutable, adding, modifying, and removing values
- Sorting values in the structure
- Testing for membership, if specific value(s) are present in the structure (using the `in` and `not in` operators)
- For structures that are ordered or indexed, accessing elements using their position

## Strings

"A string data type is traditionally a sequence of characters, either as a literal constant or as some kind of variable...A string is generally considered a data type and is often implemented as an array data structure of bytes (or words) that stores a sequence of elements, typically characters, using some character encoding" (Busbee and Braunschweig, "[String Data Type](https://press.rebus.community/programmingfundamentals/chapter/string-data-type/)")

"Like many other popular programming languages, strings in Python are arrays of bytes representing unicode characters. However, Python does not have a character data type, a single character is simply a string with a length of 1. Square brackets can be used to access elements of the string" ([W3Schools, Python Strings](https://www.w3schools.com/python/python_strings.asp))

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

Some Python string syntax we've seen previously:

```Python
# create string variable
message = "Hello world!"

# return number of characters in string
len(message)

# access first character in string
message[0]

# access last character in string
message[-1]

# test if character x is in string
'x' in message # returns false

# test if symbol % is NOT in string
'%' not in message # returns true
```

We can use the `in` operator in combination with `if-then-else` logic:

```Python
# create string variable
message = "Hello world!"

# if-then-else logic testing for specific characters in the string
if "!" in message:
  print("An exclamation point is present in this string")
  
else:
  print("An exclamation point is not present in this string")
```

Remember we can use concatenation to join or combine string objects.

```Python
# first and last name variables
first = "Knute"
last = "Rockne"

# use concatenation to create full name
name = first + " " + last
print(name)
```

### String Methods

Python includes a number of built-in methods we can use to interact with strings. Brief explanations and examples are provided for some common string methods.

#### Capitalization

- `.title()` (title case)
- `.upper()`(upper case)
- `.lower()` (lower case)

```Python
# create name variable
name = "Knute Rockne

# print in title case
print(name.title())

# print in lower case
print(name.lower())

# print in upper case
print(name.upper())
```

#### Searching

- `.count()` (returns number of times specific value appears in a string)
- `.startswith()` (returns Boolean True/False value if string begins with specific value
- `.endswith()` (returns Boolean True/False value if string ends with specific value)
- `.find()` (returns index for specific value in string, searching left-to-right)
- `.rfind()` (returns index for specific value in string, searching right-to-left)
- `.index()` (returns index for specific value in string)
- `.rfind()` (returns index for specific value in string, searching right-to-left)

```Python
# create color variable
color = "chartreuse"

# return number of e characters in string
print(color.count("e")

# return true/false if string begins with value
print(color.startswith("e")) # returns false

# return true/false if string ends with value
print(color.endswith("e")) # returns true

# returns position for first occurance of value in the string
print(color.find("e")) # returns 6

# returns index for first occurance of value in the string
print(color.index("e")) # returns 6

# returns position for first occurance of a value in the string searching right-to-left
print(color.rfind("e")) # returns 1

# returns index for first occurance of a value in the string searching right-to-left
print(color.rindex("e")) # returns 1
```

We can also use these methods to search for a substring within a string.

```Python
# create string variable
passage = "As there is no other school within more than a hundred miles, this college cannot fail to succeed. Before long, it will develop on a large scale. It will be one of the most powerful means for good in this country."

# return true/false if string ends with substring
print(passage.endswith("good")) # returns false

# returns position for first occurance of substring
print(passage.find("college"))
```

#### Modifying 

Strings in Python are immutable- that is values in the string cannot be modified once it has been created and assigned to a variable. But Python include string methods that facilitate modifying a string to create a new string object.

`.replace()` replaces a value in a string. Syntax: `.replace("OLD VALUE", "NEW VALUE")`

`.split()` splits a string at a specific separator and returns a list. The default separator is a space or whitespace character. Syntax: `.split("SEPARATOR")`

`.strip()` trims specific character(s) from a string. The default character `.strip()` removes is a whitespace character. Syntax: `.strip("CHARACTERS TO STRIP")`

```Python
# create string variable
passage = "As there is no other school within more than a hundred miles, this college cannot fail to succeed. Before long, it will develop on a large scale. It will be one of the most powerful means for good in this country."

# replace value in string
modified = passage.replace("cannot", "can't")
print(modified)

# split string at separator
sentences = passage.split(". ")
print(sentences)

# remove strip whitespace from string
modified = passage.strip()
print(modified)
```

For more on strings (general):
- Kenneth Leroy Busbee and Dave Braunschweig, "[String Data Type](https://press.rebus.community/programmingfundamentals/chapter/string-data-type/)" in *Programming Fundamentals*

More on strings in Python:
- [W3Schools, Python Strings](https://www.w3schools.com/python/python_strings.asp)
- [W3Schools, Python String Methods](https://www.w3schools.com/python/python_ref_string.asp)

### Comprehension Check

String properties

Creating string, converting to string

What method(s) could we use to accomplish X
- capitalization
- test for membership
- access via index/return index

### Application

Q6: Write a program that converts integer, float, or boolean values to a string, using the str() function.

Q7: Write a program that prompts the user to enter a 6-letter word, and then prints the first, third, and fifth letters of that word.

Q8: Modify the program to have it search for other characters in the string. Does it always return the index number you expect? What index is returned if you ask for the index of the letter u (i.e., what happens when the desired character appears more than once in the string)?

```Python
# program you're modifying for Q8
# assign string variable
color = "turquoise"

# get index number of q character
index_number = color.index("q")

# show index number as part of print statement
print ("The index number for the letter q within the word " + color + " is " + index_number)
```

### Comprehension Check

### Application


## Lists

"An array is a data structure consisting of a collection of elements (values or variables), each identified by at least one array index or key...In Python, the built-in array data structure is a list" (Busbee and Braunschweig, "[Arrays and Lists](https://press.rebus.community/programmingfundamentals/chapter/arrays-and-lists/)")
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

Some Python list syntax we've seen previously:

Let's use the example of a list of strings:

```Python
# list of string objects
fruits = ["apple", "banana", "blueberry", "cherry"]

# check data type
type(fruits)
```

We can determine the number of elements in the list using the `len()` function.

```Python
len(fruits)
```

Remember Python starts at `0` and counts left-to-right. We can access specific values using their position.

```Python
# access first value 
fruits[0]

# access second value
fruits[1]

# access third value
fruits[2]
```

Python lists also support negative indexing- we can use negative index values to count right-to-left. 
- NOTE: Negative indexing starts counting at `-1`

```Python
# access last value
fruits[-1]

# access next to last value
fruits[-2]
```

We can also use the `.index()` method to output the position for specific values (if they are present in the structure).

```Python
# return index for cherry
print("The index for cherry is ", fruits.index("cherry"))

# return index for pear
print("The index for pear is ", fruits.index("pear"))
```

The last line of the program returns an `IndexError` message because `pear` is not a value in the list.

We can test for membership using the `in` and `not in` operators.

```Python
# test if apple is in list
"apple" in fruits

# test if blueberry is NOT in list
"blueberry" not in fruits
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


- Structure big picture
- Examples we've seen before (composite variables)
- Creating them
- Length/access
- Modifying (growing, deleting, inserting, appending)
- Other common operations (length, sort, concatenation, copying, in operator, search, utility functions, max/min, sum)
- Nested lists, sublists (selection syntax, modifying)

- "An array is a data structure consisting of a collection of elements (values or variables), each identified by at least one array index or key...In Python, the built-in array data structure is a list" (Busbee and Braunschweig, "[Arrays and Lists](https://press.rebus.community/programmingfundamentals/chapter/arrays-and-lists/)")
- An list is a single-dimension array

### Creating Lists

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

### List Properties

We can check the number of values or elements in a list using the length function `len()`.

PYTHON EXAMPLE

We can access specific elements in a list using an index operator (`[]`) and position (numeric value).

PYTHON EXAMPLE

### List Methods

TABLE WITH LIST METHODS

### Modifying Lists

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

### Working With Lists

in operator

copying, concatenation

Sorting, reversing (INPLACE)

Summary statistics 

### Additional Resources

More on arrays/lists (general):
- Kenneth Leroy Busbee and Dave Braunschweig, "[Arrays and Lists](https://press.rebus.community/programmingfundamentals/chapter/arrays-and-lists/)" in *Programming Fundamentals*

More on lists in Python:
- [W3Schools, Python Lists](https://www.w3schools.com/python/python_lists.asp)

### Comprehension Check

### Application

## Tuples

- "Tuples are used to store multiple items in a single variable...A tuple is a collection which is ordered and unchangeable. Tuples are written with round brackets...and allow duplicate values" ([W3Schools, Python Tuples](https://www.w3schools.com/python/python_tuples.asp))

### Creating Tuples

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

### Tuple Properties

LEN FUNCTION

Tuples are indexed, so we can access individual items using an index operator and value.

```Python
# access first item in sample tuple
sample[0]
```

### Modifying Tuples

MODIFYING TUPLES

For more on tuples in Python:
- [W3Schools, Python Tuples](https://www.w3schools.com/python/python_tuples.asp)

### Comprehension Check

### Application

## Sets

### Comprehension Check

## Dictionaries

- Big picture concept
- Structure
- Creating
- Accessing
- Modifying
- More iteration/loop groundwork with keys, items, values methods

### Comprehension Check

### Application

# Putting It All Together

# Lab Notebook Questions
