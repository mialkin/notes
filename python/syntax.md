# Python syntax

- [Python syntax](#python-syntax)
  - [Comments](#comments)
  - [Division](#division)
  - [Comparison](#comparison)
  - [Exponentiation](#exponentiation)
  - [`is` vs `==`](#is-vs-)
  - [Booleans](#booleans)
  - [Strings](#strings)
  - [Environment variables](#environment-variables)
  - [None](#none)
  - [Print](#print)
  - [User input](#user-input)
  - [Ternary operator](#ternary-operator)
  - [Lists](#lists)
  - [Tuples](#tuples)
  - [Dictionaries](#dictionaries)
  - [Sets](#sets)
  - [Control flow](#control-flow)
  - [Exceptions handling](#exceptions-handling)
  - [Files](#files)

## Comments

```py
# Single line comments

""" Multiline strings
    comment
"""
```

## Division

The result of division is always a floating-point number:

```py
10.0 / 3  # => 3.3333333333333335
1 / 1     # => 1.0
```

Integer division `//` rounds down for both positive and negative numbers:

```py
5 // 3       # => 1
-5 // 3      # => -2
5.0 // 3.0   # => 1.0 # works on floats too
-5.0 // 3.0  # => -2.0
```

## Comparison

Chaining makes this look nicer:

```py
1 < 2 < 3  # => True
2 < 3 < 2  # => False
```

## Exponentiation

```py
2**3  # => 8
```

## `is` vs `==`

`is` checks if two variables refer to the same object, whereas `==` checks
if the pointed objects have the same values:

```py
a = [1, 2, 3, 4]  # Point a at a new list, [1, 2, 3, 4]
b = a             # Point b at what a is pointing to
b is a            # => True, a and b refer to the same object
b == a            # => True, a's and b's objects are equal
b = [1, 2, 3, 4]  # Point b at a new list, [1, 2, 3, 4]
b is a            # => False, a and b do not refer to the same object
b == a            # => True, a's and b's objects are equal
```

## Booleans

```py
True   # => True
False  # => False
```

Negation is done with `not`:

```py
not True        # => False
not False       # => True
True and False  # => False
False or True   # => True
```

`True` and `False` are actually `1` and `0`:

```py
True + True # => 2
True * 8    # => 8
False - 5   # => -5
```

Comparison operators examine numerical values of `True` and `False`:

```py
0 == False  # => True
1 == True   # => True
2 == True   # => False
-5 != False # => True
```

`None`, `0`, and empty strings/lists/dicts/tuples all evaluate to `False`. All other values are `True`

```py
bool(0)   # => False
bool("")  # => False
bool([])  # => False
bool({})  # => False
bool(())  # => False
```

## Strings

```py
"This is a string"
'This is a string too'
```

Length:

```py
len("summer")   # => 6
```

Concatenation:

```py
"Hello " + "world!"  # => "Hello world!"
"Hello " "world!"    # => "Hello world!"
```

Interpolation:

```py
name = "Aleksei"
f"My name is {name}"                       # => "My name is Aleksei"
f"{name} is {len(name)} characters long"   # => "Aleksei is 7 characters long"
```

A string can be treated like a list of characters:

```py
"Hello world!"[0]  # => 'H'
```

## Environment variables

```py
import os
    print(os.environ['HOME'])
```

## None

`None` is an object:

```py
None  # => None
```

Don't use the equality `==` symbol to compare objects to None
Use `is` instead. This checks for equality of object identity.

```py
"etc" is None  # => False
None is None   # => True
```

## Print

Python has a `print` function:

```py
print("I'm Python. Nice to meet you!")  # => I'm Python. Nice to meet you!
```

By default the `print` function also prints out a newline at the end. Use the optional argument end to change the end string:

```py
print("Hello, World", end="!")  # => Hello, World!
```

## User input

Get input data from console:

```py
input_string_var = input("Enter some data: ") # Returns the data as a string
```

## Ternary operator

```py
result = "yay!" if 0 > 1 else "nay!"
print (result)  # => "nay!"
```

## Lists

```py
my_list = [4, 5, 6] # Quick list initialization

li = []
li.append(1)    # Append new element

li[0]           # Get element by index
li[-1]          # Get last element
li.pop()        # Remove last element
del li[2]       # Remove element at index
li.remove(2)    # Remove first occurence of element 2
li.insert(1, 2) # Insert 2 at index 1
li.index(2)     # Get index of the first element 2
li + li2        # Concatenate li with li2 => [1, 2, 3, 4, 5, 6]
li.extend(li2)  # Concatenate li with li2
1 in li         # Check if element exists in list => True
len(li)         # Get length of list
```

Ranges:

```py
li[1:3]   # Return list from index 1 to 3
li[2:]    # Return list starting from index 2
li[:3]    # Return list from beginning until index 3
li[::2]   # Return list selecting every second entry
li[::-1]  # Return list in reverse order => [3, 4, 2, 1]
```

## Tuples

Tuples are immutable:

```py
tup = (1, 2, 3)
tup[0]            # => 1
tup[0] = 3        # Raises a TypeError
```

Note, that a tuple made of a single element has to have a comma after that element, but tuples of other lengths, including zero, don't:

```py
type((1))   # => <class 'int'>
type((1,))  # => <class 'tuple'>
type(())    # => <class 'tuple'>
```

You can do most of the list operations on tuples too:

```py
len(tup)         # => 3
tup + (4, 5, 6)  # => (1, 2, 3, 4, 5, 6)
tup[:2]          # => (1, 2)
2 in tup         # => True
```

You can unpack tuples (or lists) into variables:

```py
a, b, c = (1, 2, 3)  # a is now 1, b is now 2 and c is now 3
```

You can also do extended unpacking:

```py
a, *b, c = (1, 2, 3, 4)  # a is now 1, b is now [2, 3] and c is now 4
```

Tuples are created by default if you leave out the parentheses:

```py
d, e, f = 4, 5, 6  # tuple 4, 5, 6 is unpacked into variables d, e and f
```

Respectively such that d = 4, e = 5 and f = 6. Now look how easy it is to swap two values:

```py
e, d = d, e  # d is now 5 and e is now 4
```

## Dictionaries

```py
empty_dict = {}
```

Here is a prefilled dictionary:

```py
filled_dict = {"one": 1, "two": 2, "three": 3}
```

Note keys for dictionaries have to be immutable types. This is to ensure that the key can be converted to a constant hash value for quick look-ups.

Immutable types include ints, floats, strings, tuples:

```py
invalid_dict = {[1,2,3]: "123"}  # => Raises a TypeError: unhashable type: 'list'
valid_dict = {(1,2,3):[1,2,3]}   # Values can be of any type, however.
```

Look up values with `[]`:

```py
filled_dict["one"]  # => 1
```

Get all keys as an iterable with `keys()`. We need to wrap the call in `list()` to turn it into a list. We'll talk about those later. Note - for Python versions <3.7, dictionary key ordering is not guaranteed. Your results might not match the example below exactly. However, as of Python 3.7, dictionary items maintain the order at which they are inserted into the dictionary:

```py
list(filled_dict.keys())  # => ["three", "two", "one"] in Python <3.7
list(filled_dict.keys())  # => ["one", "two", "three"] in Python 3.7+
```

Get all values as an iterable with `values()`. Once again we need to wrap it in `list()` to get it out of the iterable. Note - Same as above regarding key ordering:

```py
list(filled_dict.values())  # => [3, 2, 1]  in Python <3.7
list(filled_dict.values())  # => [1, 2, 3] in Python 3.7+
```

Check for existence of keys in a dictionary with `in`:

```py
"one" in filled_dict  # => True
1 in filled_dict      # => False
```

Looking up a non-existing key is a `KeyError`:

```py
filled_dict["four"]  # KeyError
```

Use `get()` method to avoid the `KeyError`:

```py
filled_dict.get("one")      # => 1
filled_dict.get("four")     # => None
```

The get method supports a default argument when the value is missing:

```py
filled_dict.get("one", 4)   # => 1
filled_dict.get("four", 4)  # => 4
```

`setdefault()` inserts into a dictionary only if the given key isn't present:

```py
filled_dict.setdefault("five", 5)  # filled_dict["five"] is set to 5
filled_dict.setdefault("five", 6)  # filled_dict["five"] is still 5
```

Adding to a dictionary:

```py
filled_dict.update({"four":4})  # => {"one": 1, "two": 2, "three": 3, "four": 4}
filled_dict["four"] = 4         # another way to add to dict
```

Remove keys from a dictionary with `del`:

```py
del filled_dict["one"]  # Removes the key "one" from filled dict
```

From Python 3.5 you can also use the additional unpacking options:

```py
{'a': 1, **{'b': 2}}  # => {'a': 1, 'b': 2}
{'a': 1, **{'a': 2}}  # => {'a': 2}
```

## Sets

```py
empty_set = set()
```

Initialize a set with a bunch of values:

```py
some_set = {1, 1, 2, 2, 3, 4}
```

Similar to keys of a dictionary, elements of a set have to be immutable:

```py
invalid_set = {[1], 1}  # => Raises a TypeError: unhashable type: 'list'
valid_set = {(1,), 1}
```

Add element to the set:

```py
filled_set = some_set
filled_set.add(5)  # Filled_set is now {1, 2, 3, 4, 5}
# Sets don't have duplicate elements,
filled_set.add(5)  # so it remains as before {1, 2, 3, 4, 5}
```

Intersection is done with `&`:

```py
other_set = {3, 4, 5, 6}
filled_set & other_set  # => {3, 4, 5}
```

Union is done with `|`:

```py
filled_set | other_set  # => {1, 2, 3, 4, 5, 6}
```

Difference is done with `-`:

```py
{1, 2, 3, 4} - {2, 3, 5}  # => {1, 4}
```

Symmetric difference is done with `^`:

```py
{1, 2, 3, 4} ^ {2, 3, 5}  # => {1, 4, 5}
```

Check if the set on the left is a superset of the set on the right:

```py
{1, 2} >= {1, 2, 3} # => False
```

 Check if the set on the left is a subset of the set on the right:

 ```py
 {1, 2} <= {1, 2, 3} # => True
 ```

Check if element is in the set:

```py
2 in filled_set   # => True
10 in filled_set  # => False
```

Create a deep copy of a set:

```py
filled_set = some_set.copy()  # filled_set is {1, 2, 3, 4, 5}
filled_set is some_set        # => False
```

## Control flow

Let's just make a variable:

```py
some_var = 5
```

Here is an if statement. Indentation is significant in Python! Convention is to use four spaces, not tabs.

```py
if some_var > 10:
    print("some_var is totally bigger than 10.")
elif some_var < 10:    # This elif clause is optional.
    print("some_var is smaller than 10.")
else:                  # This is optional too.
    print("some_var is indeed 10.")

"""
For loops iterate over lists
prints:
    dog is a mammal
    cat is a mammal
    mouse is a mammal
"""
for animal in ["dog", "cat", "mouse"]:
    # You can use format() to interpolate formatted strings
    print("{} is a mammal".format(animal))

"""
"range(number)" returns an iterable of numbers
from zero to the given number
prints:
    0
    1
    2
    3
"""
for i in range(4):
    print(i)

"""
"range(lower, upper)" returns an iterable of numbers
from the lower number to the upper number
prints:
    4
    5
    6
    7
"""
for i in range(4, 8):
    print(i)

"""
"range(lower, upper, step)" returns an iterable of numbers
from the lower number to the upper number, while incrementing
by step. If step is not indicated, the default value is 1.
prints:
    4
    6
"""
for i in range(4, 8, 2):
    print(i)

"""
To loop over a list, and retrieve both the index and the value of each item in the list
prints:
    0 dog
    1 cat
    2 mouse
"""
animals = ["dog", "cat", "mouse"]
for i, value in enumerate(animals):
    print(i, value)

"""
While loops go until a condition is no longer met.
prints:
    0
    1
    2
    3
"""
x = 0
while x < 4:
    print(x)
    x += 1  # Shorthand for x = x + 1
```

## Exceptions handling

Handle exceptions with a `try/except` block:

```py
try:
    # Use "raise" to raise an error
    raise IndexError("This is an index error")
except IndexError as e:
    pass                 # Pass is just a no-op. Usually you would do recovery here.
except (TypeError, NameError):
    pass                 # Multiple exceptions can be handled together, if required.
else:                    # Optional clause to the try/except block. Must follow all except blocks
    print("All good!")   # Runs only if the code in try raises no exceptions
finally:                 # Execute under all circumstances
    print("We can clean up resources here")
```

## Files

Instead of try/finally to cleanup resources you can use a with statement

```py
with open("myfile.txt") as f:
    for line in f:
        print(line)
```

Writing to a file:

```py
contents = {"aa": 12, "bb": 21}
with open("myfile1.txt", "w+") as file:
    file.write(str(contents))        # Writes a string to a file

with open("myfile2.txt", "w+") as file:
    file.write(json.dumps(contents)) # Writes an object to a file
```

Reading from a file:

```py
with open('myfile1.txt', "r+") as file:
    contents = file.read()           # Reads a string from a file
print(contents)
# print: {"aa": 12, "bb": 21}

with open('myfile2.txt', "r+") as file:
    contents = json.load(file)       # Reads a json object from a file
print(contents)
# print: {"aa": 12, "bb": 21}
```