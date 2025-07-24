# 🐍 Basic Python Interview Questions & Answers for Freshers

---

## ✅ 1. What is Python?
Python is a high-level, interpreted, general-purpose programming language known for its readability and simplicity.

## ✅ 2. What are the key features of Python?
- Easy to learn and use  
- Interpreted language  
- Dynamically typed  
- Object-oriented  
- Extensive standard libraries

## ✅ 3. What is PEP 8?
PEP 8 is the Python Enhancement Proposal that provides coding style guidelines for writing readable and consistent Python code.

## ✅ 4. What are Python’s key data types?
- `int`, `float`, `str`, `bool`, `list`, `tuple`, `dict`, `set`, `NoneType`

## ✅ 5. What is the difference between list and tuple?
- List: mutable  
- Tuple: immutable

## ✅ 6. What is a dictionary in Python?
A dictionary is an unordered collection of key-value pairs.

## ✅ 7. What is the difference between `==` and `is`?
- `==`: compares values  
- `is`: compares object identities

## ✅ 8. What are local and global variables?
- Local: declared inside a function  
- Global: declared outside any function

## ✅ 9. What is a function in Python?
A reusable block of code that performs a specific task.

## ✅ 10. How do you define a function in Python?
```python
def function_name(parameters):
    # code block
````

## ✅ 11. What is the difference between \*args and \*\*kwargs?

* `*args`: variable number of positional arguments
* `**kwargs`: variable number of keyword arguments

## ✅ 12. What is indentation in Python?

Indentation defines the block of code and is mandatory in Python (usually 4 spaces).

## ✅ 13. What are Python modules?

Files containing Python code (.py) that can be imported and reused.

## ✅ 14. What is a package in Python?

A collection of Python modules organized in directories with an `__init__.py` file.

## ✅ 15. What is the use of the `pass` statement?

A null statement used as a placeholder where code will be written later.

## ✅ 16. What is the difference between `break` and `continue`?

* `break`: exits the loop
* `continue`: skips current iteration

## ✅ 17. How does the `range()` function work?

Generates a sequence of numbers, used in loops.
Example: `range(0, 5)` generates 0 to 4.

## ✅ 18. What is the purpose of `self` parameter?

Refers to the current instance of the class; used to access instance attributes.

## ✅ 19. Difference between deep copy and shallow copy?

* Shallow copy: copies object reference
* Deep copy: creates new object and copies all data

## ✅ 20. How do you handle exceptions in Python?

```python
try:
    # code
except Exception as e:
    # handle exception
```

## ✅ 21. What is the purpose of the `finally` block?

It runs regardless of whether an exception occurs or not.

## ✅ 22. What is a lambda function?

An anonymous function written as:

```python
lambda args: expression
```

## ✅ 23. What is list comprehension?

A concise way to create lists:

```python
[x for x in range(5)]
```

## ✅ 24. What is a generator?

A function that yields values one at a time using `yield`.

## ✅ 25. How to open a file in Python?

```python
with open('file.txt', 'r') as f:
    data = f.read()
```

## ✅ 26. What are Python decorators?

Functions that modify the behavior of other functions or methods.

## ✅ 27. What is recursion in Python?

A function calling itself to solve smaller problems.

## ✅ 28. What are \*args and \*\*kwargs?

* `*args`: collects extra positional arguments
* `**kwargs`: collects extra keyword arguments

## ✅ 29. What is the use of `__init__` method?

Used to initialize object attributes during class instantiation.

## ✅ 30. What is a class and object in Python?

* Class: blueprint for creating objects
* Object: instance of a class

## ✅ 31. What is inheritance?

Allows a class to inherit methods and attributes from another class.

## ✅ 32. What is multiple inheritance?

A class inheriting from more than one base class.

## ✅ 33. Difference between `@staticmethod` and `@classmethod`?

* `@staticmethod`: no self or cls
* `@classmethod`: takes `cls` as the first argument

## ✅ 34. What is the `__str__()` method?

Defines the string representation of an object.

## ✅ 35. What are built-in data structures in Python?

List, Tuple, Set, Dictionary

## ✅ 36. What is slicing in Python?

Extracting a part of a sequence:

```python
s[1:5:2]
```

## ✅ 37. What is a lambda function?

A short anonymous function:

```python
lambda x: x * 2
```

## ✅ 38. Difference between mutable and immutable objects?

* Mutable: can change (list, dict)
* Immutable: can’t change (tuple, str, int)

## ✅ 39. How do you convert string to int in Python?

```python
int("123")
```

## ✅ 40. What is the purpose of `isinstance()`?

Checks if an object is an instance of a class.

## ✅ 41. Difference between `append()` and `extend()`?

* `append()`: adds one element
* `extend()`: adds elements from an iterable

## ✅ 42. What is a docstring?

A string literal used to document code.

## ✅ 43. What is pickling in Python?

Serializing an object using the `pickle` module.

## ✅ 44. What is the use of `dir()` function?

Returns list of attributes and methods of an object.

## ✅ 45. Difference between `input()` and `raw_input()`?

* Python 3: only `input()` exists
* Python 2: `raw_input()` used to read string input

## ✅ 46. How do you install packages in Python?

```bash
pip install package_name
```

## ✅ 47. What is a virtual environment?

An isolated environment for managing dependencies per project.

## ✅ 48. What is `if __name__ == "__main__"` used for?

Ensures code runs only when script is executed directly.

## ✅ 49. What is the use of `map()`, `filter()`, and `reduce()`?

* `map()`: applies function to each item
* `filter()`: filters items based on condition
* `reduce()`: reduces a list to a single value

## ✅ 50. What is a Python iterator?

An object with `__iter__()` and `__next__()` methods.

## ✅ 51. What is a Python generator?

A function that yields values one by one using `yield`.

## ✅ 52. Difference between `=`, `==`, and `===` in Python?

* `=`: assignment
* `==`: equality check
* `===`: not used in Python

---
📘 **Tips for Freshers**:

* Practice writing clean Python scripts
* Use list comprehension and functions regularly
* Work on basic projects (To-do App, Calculator, etc.)
* Practice on platforms like HackerRank, LeetCode, or Replit
