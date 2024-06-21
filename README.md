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
var1 = "Aarya"
print("Hi my name is: ", var1)
print(f"Hi my name is {var1}") #using f string method
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
#similar to int and float we also have char, str etc
```
## Python Data Types
### Numeric Types
- **int**: Integer numbers.
  ```python
  x = 5
  ```

- **float**: Floating-point numbers (decimals).
  ```python
  y = 5.5
  ```

- **complex**: Complex numbers.
  ```python
  z = 1 + 2j
  ```

### Sequence Types

- **str**: String of characters.
  ```python
  name = "Alice"
  ```

- **list**: Ordered, mutable collection.
  ```python
  fruits = ["apple", "banana", "cherry"]
  ```

- **tuple**: Ordered, immutable collection.
  ```python
  point = (10, 20)
  ```

### Mapping Type

- **dict**: Key-value pairs, unordered.
  ```python
  person = {"name": "Alice", "age": 25}
  ```

### Set Types

- **set**: Unordered collection of unique elements.
  ```python
  unique_numbers = {1, 2, 3}
  ```

- **frozenset**: Immutable version of set.
  ```python
  frozen_numbers = frozenset([1, 2, 3])
  ```

### Boolean Type

- **bool**: True or False.
  ```python
  is_active = True
  ```

### None Type

- **NoneType**: Represents the absence of value.
  ```python
  unknown = None
  ```

## range Function
The `range` function returns a sequence of numbers, e.g., numbers starting from 0 to n-1 for `range(0, n)`.

```python
range(int_start_value, int_stop_value, int_step_value)
```

Here the start value and step value are by default 1 if not mentioned by the programmer, but `int_stop_value` is a compulsory parameter in the range function.
also note that `int_start_value`  is inclusive whereas `int_stop_value`  is exclusive

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

**Newline Character**:
using newline character we can jump to next line, i.e. the code \n will execute in new line

```python
print("\n")
```

**Backslash**:
It adds a backslash
```python
print("\\")
```

**Single Quote**:
It adds a single quotation mark
```python
print("\'")
```

**Tab**:
It gives a tab space
```python
print("\t")
```

**Backspace**:
It adds a backspace
```python
print("\b")
```

**Octal value**:
It represents the value of an octal number
```python
print("\ooo")
```

**Hex value**:
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
You can create Strings by enclosing text in both forms of quotes - single quotes or double quotes.

```python
variable_name = "String Data"
```

Example:

```python
str = "Aarya"
print("String is ", str)
```

## Indexing
The position of every character placed in the string starts from 0th position and step by step it ends at length-1 position.
![Python List Indexing](python-list-index.png)

## Python Slicing

Slicing is a technique in Python used to extract a portion of a sequence (like a string, list, or tuple) by specifying a start index, an end index (exclusive), and an optional step size.

### Syntax:

```python
sequence[start:end:step]
```

- **start**: The index where the slice begins (inclusive).
- **end**: The index where the slice ends (exclusive).
- **step** (optional): The increment between characters or elements in the slice.

### Examples:

```python
text = "Hello, World!"

# Extract substring from index 0 to 5 (exclusive).
substring1 = text[0:5]
print(substring1)  # Output: "Hello"

# Omit start index (starts from beginning).
substring2 = text[:5]
print(substring2)  # Output: "Hello"

# Extract substring from index 7 to end of string.
substring3 = text[7:]
print(substring3)  # Output: "World!"

# Negative index to count from end of string.
substring4 = text[-6:]
print(substring4)  # Output: "World!"

# Extract every other character.
substring5 = text[::2]
print(substring5)  # Output: "Hlo ol!"

# Reverse the string.
substring6 = text[::-1]
print(substring6)  # Output: "!dlroW ,olleH"
```

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

The position of every element placed in the list starts from 0th position and step by step it ends at length-1 position.

List is ordered, indexed, mutable and the most flexible and dynamic collection of elements in Python.

### List Methods

-**Empty list**: This method allows you to create an empty list.
```python
my_list = []
```

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

The position of every element placed in the tuple starts from 0th position and step by step it ends at length-1 position.

Tuples are ordered, indexed, immutable, and the most secured collection of elements.

### Tuple Methods

Tuples in Python are immutable, meaning their contents cannot be changed after creation. While methods that modify data (like `append()`, `insert()`, `remove()`, `pop()`, `sort()`, `reverse()`) are exclusive to lists, you can safely use other methods with tuples:

- **Querying Methods:**
  - `count(value)`: Returns the number of occurrences of `value`.
  - `index(value)`: Returns the index of the first occurrence of `value`.

- **Utility Methods:**
  - `len()`: Returns the number of items in the tuple.
  - `min()`: Returns the smallest item in the tuple.
  - `max()`: Returns the largest item in the tuple.

- **Iteration and Membership Checking:**
  - Use `for` loops to iterate over tuple elements.
  - Check membership with `in` and `not in`.

### Example:

```python
my_tuple = (1, 2, 3, 2, 4)

# Querying methods
count_twos = my_tuple.count(2)  # Output: 2
index_two = my_tuple.index(2)   # Output: 1

# Utility methods
tuple_length = len(my_tuple)    # Output: 5
min_value = min(my_tuple)       # Output: 1
max_value = max(my_tuple)       # Output: 4

# Iteration and membership checking
for item in my_tuple:
    print(item)

if 3 in my_tuple:
    print("3 is present in the tuple")
else:
    print("3 is not present in the tuple")
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

### Dictionary Methods
- **Empty Dictionary**:By using this method you can create an empty dictionary.

```python
my_dict = {}
```

- **Adding Key/Value Pair**:This method adds the key-value pair to the dictionary.

```python
my_dict[key] = value
```

- **Accessing Dictionary Items**:To access the elements from a dictionary we use the key name.

```python
dictionary[keyname]
```

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
The for loop of  Python is designed to process the items of any sequence, such as a list or a string, one by one.
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
A while loop is a conditional loop that will repeat the instructions within itself as long as a conditional remains true.
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

## Break Statement

The break statement enables a program to skip over a part of the code. A break statement terminates the very loop it lies within.

```python
for <var> in <sequence>:
    statement1
    if <condition>:
        break #therefore every line of code after this break statement will not get execute.
    statement2
statement_after_loop
```

## Continue Statement

The continue statement skips the rest of the loop statements and causes the next iteration to occur.

```python
for <var> in <sequence>:
    statement1
    if <condition>:
        continue #therefore here statements after continue will get execute
    statement2
    statement3
    statement4
```

### Functions

A function is a block of code that performs a specific task. You can pass parameters into a function. It helps us to make our code more organized and manageable.

### Defining a Function

Functions are defined using the `def` keyword followed by the function name and optional parameters:

```python
def greet(name):
    return f"Hello, {name}!"
```

### Calling a Function

To use a function, call it by its name and provide necessary arguments:

```python
message = greet("Charlie")
print(message)  # Output: "Hello, Charlie!"
```

### Return Values

Functions can return values using the `return` statement:

```python
def multiply(a, b):
    return a * b

product = multiply(4, 6)
print(product)  # Output: 24
```

### Parameters vs Arguments

- **Parameters**: Variables defined in the function's declaration to receive values and they act as placeholders for values that 
the function expects to receive when it is called (i.e. argument).
- **Arguments**: Actual values passed to a function when it is called.

```python
def greet(name):  # 'name' is a parameter
    print(f"Hello, {name}!")

greet("Alice")  # "Alice" is an argument
```

```python
def add(x, y):  # 'x' and 'y' are parameters
    return x + y

result = add(3, 5)  # 3 and 5 are arguments
print(result)  # Output: 8
```

Therefore Parameters define what kind of data a function can accept, while arguments are the actual data passed to the function when called. This distinction allows functions to be versatile and reusable in Python programming.

### File Handling

File handling refers to reading or writing data from files. Python provides some functions that allow us to manipulate data in the files.

**Open Function:**

```python
var_name = open("file name", " mode")
```

**Modes:**
- `r`: to read the content from file
- `w`: to write the content into file
- `a`: to append the existing content into file
- `r+`: To read and write data into the file. The previous data in the file will be overridden.
- `w+`: To write and read data. It will override existing data.
- `a+`: To append and read data from the file. It won’t override existing data.

**Close Function:**

```python
var_name.close()
```

**Read Functions:**

- `read()`: returns one big string
- `readlines()`: returns a list
- `readline()`: returns one line at a time

**Write Function:**

```python
write()  # Used to write a fixed sequence of characters to a file
```

**Example:**

In Python, we have two ways to handle files. In the first way, we do not need to close the file we opened, but in the second way, we have to close the file we opened.

```python
#1st way:
with open('file.txt', 'w') as f:
    f.write("Hello, World!")
#2nd way:
var_name = open("file name", " mode")
var_name.write("hello")
var_name.close()
```

## Exception Handling

Exception handling in Python allows you to manage and respond to errors that may occur during program execution.

Syntax:

```python
try:
    # Code that might raise an exception
except ExceptionType1:
    # Handle ExceptionType1
except ExceptionType2:
    # Handle ExceptionType2
except ExceptionType3:
    # Handle ExceptionType3
else:
    # Optional else block
    # Executes if no exceptions were raised in the try block
finally:
    # Optional finally block
    # Executes whether an exception occurred or not
    # Useful for cleanup actions like closing files or releasing resources
```

Types of Exception handling: 

```python
try:
    # Code that might raise different exceptions
except ZeroDivisionError:
    # Handle division by zero error
except IndexError:
    # Handle index out of range error
except FileNotFoundError:
    # Handle file not found error
except KeyError:
    # Handel Key errors
```

## Local and Global Variables in Python

In Python, variables can have different scopes, primarily categorized into two main types: local and global.

### 1. Local Variables:

- **Definition**:
  - Local variables are defined within a function and are only accessible within that function.
  - They have a limited scope and are not visible or usable outside the function.
  - Local variables are created when the function is called and destroyed when the function exits.

**Example:**
```python
def my_function():
    # This is a local variable
    x = 10
    print("Inside the function: x =", x)

my_function()
```

In this example, `x` is a local variable within the `my_function` function. It can only be accessed and used within the function.

### 2. Global Variables:

- **Definition**:
  - Global variables are defined outside of any function and are accessible from any part of the code, both inside and outside functions.
  - They have a broader scope and can be used throughout the entire program.

**Example:**
```python
# This is a global variable
y = 20

def my_function():
    # Accessing the global variable within the function
    print("Inside the function: y =", y)

my_function()

# We can also access y outside the function
print("Outside the function: y =", y)
```

In this example, `y` is a global variable defined outside the function `my_function`. It can be accessed both inside and outside the function without any issues.

### Modifying Global Variables:

- **Usage of `global` Keyword**:
  - To modify the value of a global variable from within a function, use the `global` keyword to indicate that you are working with the global variable.

**Example:**
```python
z = 30

def modify_global_variable():
    global z  # Use the 'global' keyword to modify the global variable
    z = 40

modify_global_variable()
print("Modified global variable z =", z)
```

In this example, the `global` keyword is used inside the `modify_global_variable` function to modify the global variable `z`. As a result, the value of `z` is changed to 40.


## Object Oriented Programming (OOPS)

It is a programming approach that primarily focuses on using objects and classes. The objects can be any real-world entities.

**Class:**

```python
class class_name:
    pass  # statements
```

**Creating an Object:**

```python
object-name = Class_name
Object-name.(whatev u wan do) 
```

**Self Parameter:**

The `self` parameter is the first parameter of any function present in the class. It can be of a different name, but this parameter is a must while defining any function into a class as it is used to access other data members of the class.

**Class with a Constructor:**

Constructor is a special function of the class which is used to initialize the objects.

```python
class Person:
  def __init__(self, name, age):
    self.name = name
    self.age = age

  def myfunc(self): #here we have created a function inside a class person/method for that specific class
    print("Hello my name is " + self.name)

p1 = Person("John", 36)
p1.myfunc() #we used a method of particular class on its object
```

### Inheritance in Python

By using inheritance, we can create a class which uses all the properties and behavior of another class. The new class is known as a derived class or child class, and the one whose properties are acquired is known as a base class or parent class.

It provides the re-usability of the code.

**Base Class:**

```python
class Base_class:
    pass
```

**Derived Class:**

```python
class derived_class(Base_class):
    pass
```

### Types of Inheritance

- Single inheritance
- Multiple inheritance
- Multilevel inheritance
- Hierarchical inheritance

### Filter Function

The `filter()` function allows you to process an iterable and extract those items that satisfy a given condition.

```python
filter(function, iterable)
```

### issubclass Function

Used to find whether a class is a subclass of a given class or not.

```python
issubclass(obj, classinfo)  # returns True if obj is a subclass of classinfo
```

### Iterators and Generators

Here are some advanced topics of the Python programming language like iterators and generators.

**Iterator:**

Used to create an iterator over an iterable.

```python
iter_list = iter(['Harry', 'Aakash', 'Rohan'])
print(next(iter_list))
print(next(iter_list))
print(next(iter_list))
```

**Generator:**

Used to generate values on the fly.

```python
# A simple generator function
def my_gen():
    n = 1
    print('This is printed first')
    # Generator function contains yield statements
    yield n
    n += 1
    print('This is printed second')
    yield n
    n += 1
    print('This is printed at last')
    yield n
```

### Decorators

Decorators are used to modifying the behavior of a function or a class. They are usually called before the definition of a function you want to decorate.

**Property Decorator (getter):**

```python
@property
def name(self):
    return self.__name
```

**Setter Decorator:**

It is used to set the property 'name'.

```python
@name.setter
def name(self, value):
    self.__name = value
```

**Deleter Decorator:**

It is used to delete the property 'name'.

```python
@name.deleter  # property-name.deleter decorator
def name(self):
    print('Deleting..')
    del self.__name
```
###For more detailed explanations and examples, refer to [W3Schools Python Tutorial](https://www.w3schools.com/python/default.asp)

