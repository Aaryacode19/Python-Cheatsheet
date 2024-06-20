# Python-Cheatsheet

## Basics
Basic syntax from the Python programming language

### Showing Output To User
The `print` function is used to display or print output as follows:

```python
print("Content that you wanna print on screen")
```

We can display the content present in an object using the `print` function as follows:

```python
var1 = "Shruti"
print("Hi my name is: ", var1)
```

### Taking Input From the User
The `input` function is used to take input as a string or character from the user as follows:

```python
var1 = input("Enter your name: ")
print("My name is: ", var1)
```

To take input in the form of other data types we need to typecast them as follows:

To take input as an integer:

```python
var1 = int(input("Enter the integer value: "))
print(var1)
```

To take input as a float:

```python
var1 = float(input("Enter the float value: "))
print(var1)
```

### range Function
The `range` function returns a sequence of numbers, e.g., numbers starting from 0 to n-1 for `range(0, n)`.

```python
range(int_start_value, int_stop_value, int_step_value)
```

Here the start value and step value are by default 1 if not mentioned by the programmer, but `int_stop_value` is a compulsory parameter in the range function.

Example - Display all even numbers between 1 to 100:

```python
for i in range(0, 101, 2):
    print(i)
```

### Comments
Comments are used to make the code more understandable for programmers, and they are not executed by the compiler or interpreter.

**Single line comment**

```python
# This is a single line comment
```

**Multi-line comment**

```python
'''This is a
multi-line
comment'''
```

### Escape Sequence
An escape sequence is a sequence of characters; it doesn't represent itself (but is translated into another character) when used inside a string literal or character. Some of the escape sequence characters are as follows:

**Newline Character**

```python
print("\n")
```

**Backslash**
It adds a backslash
```python
print("\\")
```

**Single Quote**
It adds a single quotation mark
```python
print("\'")
```

**Tab**
It gives a tab space
```python
print("\t")
```

**Backspace**
It adds a backspace
```python
print("\b")
```

**Octal value**
It represents the value of an octal number
```python
print("\ooo")
```

**Hex value**
It represents the value of a hex number
```python
print("\xhh")
```

**Carriage Return**

Carriage return or `\r` will just work as you have shifted your cursor to the beginning of the string or line.

```python
print("\r")
```

## Strings
Python string is a sequence of characters, and each character can be individually accessed using its index.

### String
You can create Strings by enclosing text in both forms of quotes - single quotes or double quotes.

```python
variable_name = "String Data"
```

Example:

```python
str = "Shruti"
print("String is ", str)
```

### Indexing
The position of every character placed in the string starts from 0th position and step by step it ends at length-1 position.

### Slicing
Slicing refers to obtaining a sub-string from the given string. The following code will include index 1, 2, 3, and 4 for the variable named `var_name`.

Slicing of the string can be obtained by the following syntax:

```python
string_var[int_start_value:int_stop_value:int_step_value]
var_name[1 : 5]
```

Here start and step value are considered 0 and 1 respectively if not mentioned by the programmer.

### String Methods
- **isalnum()**: Returns `True` if all the characters in the string are alphanumeric, else `False`.

```python
string_variable.isalnum()
```

- **isalpha()**: Returns `True` if all the characters in the string are alphabets.

```python
string_variable.isalpha()
```

- **isdecimal()**: Returns `True` if all the characters in the string are decimals.

```python
string_variable.isdecimal()
```

- **isdigit()**: Returns `True` if all the characters in the string are digits.

```python
string_variable.isdigit()
```

- **islower()**: Returns `True` if all characters in the string are lower case.

```python
string_variable.islower()
```

- **isspace()**: Returns `True` if all characters in the string are whitespaces.

```python
string_variable.isspace()
```

- **isupper()**: Returns `True` if all characters in the string are upper case.

```python
string_variable.isupper()
```

- **lower()**: Converts a string into lower case equivalent.

```python
string_variable.lower()
```

- **upper()**: Converts a string into upper case equivalent.

```python
string_variable.upper()
```

- **strip()**: It removes leading and trailing spaces in the string.

```python
string_variable.strip()
```

## List
A List in Python represents a list of comma-separated values of any data type between square brackets.

```python
var_name = [element1, element2, ...]
```

These elements can be of different data types.

### Indexing
The position of every element placed in the list starts from 0th position and step by step it ends at length-1 position.

List is ordered, indexed, mutable and the most flexible and dynamic collection of elements in Python.

### Empty List
This method allows you to create an empty list.

```python
my_list = []
```

### List Methods
- **index**: Returns the index of the first element with the specified value.

```python
list.index(element)
```

- **append**: Adds an element at the end of the list.

```python
list.append(element)
```

- **extend**: Add the elements of a given list (or any iterable) to the end of the current list.

```python
list.extend(iterable)
```

- **insert**: Adds an element at the specified position.

```python
list.insert(position, element)
```

- **pop**: Removes the element at the specified position and returns it.

```python
list.pop(position)
```

- **remove**: Removes the first occurrence of a given item from the list.

```python
list.remove(element)
```

- **clear**: Removes all the elements from the list.

```python
list.clear()
```

- **count**: Returns the number of elements with the specified value.

```python
list.count(value)
```

- **reverse**: Reverses the order of the list.

```python
list.reverse()
```

- **sort**: Sorts the list.

```python
list.sort(reverse=True|False)
```

## Tuples
Tuples are represented as comma-separated values of any data type within parentheses.

### Tuple Creation
```python
variable_name = (element1, element2, ...)
```

These elements can be of different data types.

### Indexing
The position of every element placed in the tuple starts from 0th position and step by step it ends at length-1 position.

Tuples are ordered, indexed, immutable, and the most secured collection of elements.

### Tuple Methods
- **count**: Returns the number of times a specified value occurs in a tuple.

```python
tuple.count(value)
```

- **index**: Searches the tuple for a specified value and returns the position.

```python
tuple.index(value)
```

## Sets
A set is a collection of multiple values which is both unordered and unindexed. It is written in curly brackets.

### Set Creation
Way 1:

```python
var_name = {element1, element2, ...}
```

Way 2:

```python
var_name = set([element1, element2, ...])
```

Set is unordered, immutable, and non-indexed type of collection. Duplicate elements are not allowed in sets.

### Set Methods
- **add**: Adds an element to a set.

```python
set.add(element)
```

- **clear**: Removes all elements from a set.

```python
set.clear()
```

- **discard**: Removes the specified item from the set.

```python
set.discard(value)
```

- **intersection**: Returns intersection of two or more sets.

```python
set.intersection(set1, set2 ... etc)
```

- **issubset**: Checks if a set is a subset of another set.

```python
set.issubset(set)
```

- **pop**: Removes an element from the set.

```python
set.pop()
```

- **remove**: Removes the specified element from the set.

```python
set.remove(item)
```

- **union**: Returns the union of two or more sets.

```python
set.union(set1, set2...)
```

## Dictionaries
The dictionary is an unordered set of comma-separated key:value pairs, within `{}`, with the requirement that within a dictionary, no two keys can be the same.

### Dictionary Creation
```python
<dictionary-name> = {<key>: value, <key>: value ...}
```

Dictionary is an ordered and mutable collection of elements. Dictionary allows duplicate values but not duplicate keys.

### Empty Dictionary
By using this method you can create an empty dictionary.

```python
my_dict = {}
```

### Accessing Dictionary Items
To access the elements from a dictionary we use the key name.

```python
dictionary[keyname]
```

### Adding Key/Value Pair
This method adds the key-value pair to the dictionary.

```python
my_dict[key] = value
```

### Dictionary Methods
- **clear**: Removes all elements from the dictionary.

```python
dict.clear()
```

- **copy**: Returns a copy of the dictionary.

```python
dict.copy()
```

- **fromkeys**: Returns a dictionary with the specified keys and value.

```python
dict.fromkeys(keys, value)
```

- **get**: Returns the value of the specified key.

```python
dict.get(key, default=None)
```

- **items**: Returns a list containing a tuple for each key-value pair.

```python
dict.items()
```

- **keys**: Returns a list containing the dictionary's keys.

```python
dict.keys()
```

- **pop**: Removes the element with the specified key.

```python
dict.pop(key)
```

- **popitem**: Removes the last inserted key-value pair.

```python
dict.popitem()
```

- **setdefault**: Returns the value of the specified key. If the key does not exist, insert the key, with the specified value.

```python
dict.setdefault(key, default=None)
```

- **update**: Updates the dictionary with the specified key-value pairs.

```python
dict.update([other])
```

- **values**: Returns a list of all the values in the dictionary.

```python
dict.values()
```

## Conditional Statements
Conditional statements help us to execute some particular block of statements if the specified condition is `True`.

### if Statement
```python
if <condition>:
    <statement>
```

Example:

```python
if 5 > 2:
    print("5 is greater than 2")
```

### if-else Statement
```python
if <condition>:
    <statement>
else:
    <statement>
```

Example:

```python
if 5 > 2:
    print("5 is greater than 2")
else:
    print("5 is not greater than 2")
```

### if-elif-else Statement
```python
if <condition>:
    <statement>
elif <condition>:
    <statement>
else:
    <statement>
```

Example:

```python
x = 3
if x > 2:
    print("x is greater than 2")
elif x == 2:
    print("x is equal to 2")
else:
    print("x is less than 2")
```

### Nested if-else Statement
```python
if (conditional expression):
    if (conditional expression):
        statements
    else:
        statements
else:
    statements
```

### Example
```python
a = 15
b = 20
c = 12
if (a > b and a > c):
    print(a, "is greatest")
elif (b > c and b > a):
    print(b, "is greatest")
else:
    print(c, "is greatest")
```

## Loops
Loops are used to repeat a block of code multiple times.

### for Loop
```python
for <variable> in <sequence>:
    <statement>
```

Example:

```python
for i in range(5):
    print(i)
```

### while Loop
```python
while <condition>:
    <statement>
```

Example:

```python
i = 0
while i < 5:
    print(i)
    i += 1
```

## Functions
Functions are blocks of code that perform a specific task.

### Function Definition
```python
def function_name(parameters):
    <statement>
```

Example:

```python
def greet(name):
    print("Hello, " + name)

greet("Shruti")
```

### Return Statement
The `return` statement is used to exit a function and return a value.

```python
def sum(a, b):
    return a + b

print(sum(3, 5))
```

## Exception Handling
Exceptions are errors that occur during the execution of the program. We can handle exceptions using `try` and `except` blocks.

### try-except Block
```python
try:
    <statement>
except:
    <statement>
```

Example:

```python
try:
    print(10 / 0)
except ZeroDivisionError:
    print("Cannot divide by zero")
```

### finally Block
The `finally` block is executed no matter if the try block raises an error or not.

```python
try:
    <statement>
except:
    <statement>
finally:
    <statement>
```

Example:

```python
try:
    print(10 / 0)
except ZeroDivisionError:
    print("Cannot divide by zero")
finally:
    print("Execution complete")
```
