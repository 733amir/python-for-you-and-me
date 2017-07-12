# Introduction

## What is Python?

[Python](https://www.python.org/) is an interpreted, general purposed language that is designed in 1991. Python can be used for object oriented and functional programming. The language usage areas are tremendous. Some of them are, system programming, graphical user interfaces, game development, developing back-end, machine learning, visualizing data, media processing, scientific programming and many many more.

Python have very readable and simple syntax to write code. Nowadays python frameworks and libraries are every where.

There is only one drawback with python. That's runtime speed. But even this problem is almost solved by [PyPy](https://pypy.org/) project.

## What is PyCharm?

As a developer we need an environment to code in it. The best environment that I found is [PyCharm](https://www.jetbrains.com/pycharm/), it has many features like auto-completion, debugging, version controller support, ... .

## What is Jupyter?

An integrated development environment like pycharm isn't exactly what need for most of this course. We are dealing with watching effects of each line of code we write. [Jupyter](https://jupyter.org/) is what we use here.

Python is a scripting language. This is an advantage that we will get familiar through the course.

## Hello Python

There is a tradition in learning programming languages, called _Hello World_ program. We are going to respect the traditions and do it.

```python
print('Hello World!')
```

# PIP

Python have libraries. `pip` is a program that can install and remove your packages. This a fast and safe way to get a python library for our projects.

## Virtualenv

Consider situations like 2 projects with same dependencies of different versions. Like `pip`, `virtualenv`  helps you manage your packages but in different way.

```bash
$ virtualenv .venv           # Creating python virtual environment
$ source .venv/bin/activate  # Activating virtual environment
$ deactivate                 # Deactivating virtual environment
```

# Comments

Sharp \# and strings are your comments.

# PEP8

Python enhancement proposal documents are about everything. New features, community input on an issue, ... . Probably the most famous and useful one for us, is PEP8.

Development is not a single handed anymore. It's a social effort. Groups of many people try to write a code for a same software. PEP8 helps for readability of code.

We talk about it during the course and mention what you need to know about it.

# Numbers and Mathematics

## Integers

Python support unlimited numbers. Your number can have millions of digits.

`int()`

### Booleans

`False, True, bool()`

## Reals

### Floating Points

IEEE 754, 32-bit, 64-bit.

## Fractions

### Decimal

## Complex

## Arithmetics
`=, +, -, *, /, //, **, %`

# Variables and Naming
## Mutable Vs. Immutable
`id()`

# Strings & Bytes
## Escape Sequences
## Input from user
## Indexing and Slicing
## `in` Operator

# Functions

Functions can make coding easy. Splitting tasks and write them once. Improve readability.

## Don't Repeat Yourself (DRY)
## Parameters
* Passed by Reference (mutable) & Value (immutable)
* Positional argument
* Keyword argument
* Default values (becareful with default mutables!)
* Variable positional arguments
* Variable keyword arguments
* Keyword only arguments

## Return
## Scope

`if`, `elif`, `else`, `for`, `while` is current scope.
Function are new scope.

## Documentation

PEP257 - Docstring conventions. Sphinx is use to generate python documentation.

## global & nonlocal
## lambda
## pass

## Recursive Functions

```python
def factorial(n):
    if n == 0:
        return 1
    return factorial(n - 1) * n
```

## Useful Tips
* Functions should do one thing.
* Functions should be small.
* The fewer input parameters, the better.
* Functions should be consistent in their return values.
Functions shouldn't have side effects.

9. Decision Making
    1. if, elif, else
    2. <, <=, >, >=, ==, !=
    2. VALUE_1 if CONDITION else VALUE_2
    3. Use `is` and `is not` instead of `==` for `True` and `False` comparison.
    2. True, False, and, or, not
        1. Use `is` for readability
    3. Binary operators
10. Loops
    1. for
        1. `range`
    2. while
    3. break
    4. continue
    5. Comprehensions
    5. `__iter__()` and `__next__()` with `StopIteration` exception
    6. `zip()`
    7. `map()`
    8. `filter()`
# Lists
`append`, `del`, `len()`
## Packing & Unpacking
# Tuples

Frozen Lists.

# Dictionaries
## Comprehensions
# Set
## Comprehensions
# Files
    1. Reading
    2. Writing
    3. Appending
    4. Binary mode
    5. General Strings
10. Modules and Packages
    1. Don't Repeat Yourself (DRY)
    1. Importing other modules
    2. Creating other modules
10. Exceptions
    1. raise
    1. try
    1. except
    1. finally
    4. assert

# Object Oriented Programming

Good for easy code designing, reusability and readability.

Concepts:
* Objects
    * State
    * Behavior
* Class
    * Attributes
    * Methods
* Instances

Simplest python class:  
```python
# A Class (code blueprints) that represent an Object (real world concepts).
class simple:
    pass

# Creating an Instance of the object.
simple_var = simple()
```

## Class Attributes

```python
class Car:
    number_of_wheels = 4

# It's defined withing the structures of our class.
print(Car.number_of_wheels)  # 4

# Each instance can see it from the class.
simple_car = Car()
print(simple_car.number_of_wheels)  # 4

# Class attributes updates through all instances.
Car.number_of_wheels = 3
not_so_simple_car = Car()
print(not_so_simple_car.number_of_wheels)  # 3
print(simple_car.number_of_wheels)  # 3
```

Class attribute can have shadows for each object instances.

```python
class Car:
    number_of_wheels = 4

strange_car = Car()

# Altering class attribute through instances make specific class attribute values for them.
strange_car.number_of_wheels = 18
print(Car.number_of_wheels)  # 4
print(strange_car.number_of_wheels)  # 18

# But it will break updated through class structure.
Car.number_of_wheels = 3
print(strange_car.number_of_wheels)  # 18

# Don't panic, you can bind your instance to your class again.
del strange_car.number_of_wheels
print(strange_car.number_of_wheels)  # 3
```

## Access to Instance

Each method in a class have a default first argument that is not passed by what we code.

```python
class Person:
    name = 'Nobody'
    def print_name(self):
        print(self.name)

david = person()
david.name = 'David'
david.print_name()  # David
```

Now that we can access instances, we can define instance attributes.

```python
class Person:
    def set(self, name, age):
        self.name = name
        self.birth_year = 2017 - age

bob = Person()
bob.set(name='Bod', age=27)
```

## Special Methods

These methods have specific name and specific job. They have names that starts and ends with `__`

When we are creating an instance, `__init__` is the very first method that get called automatically.

```python
class Person:
    def set(self, name, age):
        self.name, self.age = name, age

alice = Person('Alice', 21)
```

You can find all information on special methods in [Here](http://www.diveintopython3.net/special-method-names.html).

# Inheritance & Composition

Main purpose of OOP is reusing existing codes. Inheritance (is-a relationship) and composition (has-a relationship) are
two main ways to reuse code.

```python
class Engine:  # Base class, Parent class
    def start(self):
        print('Engine started.')

    def stop(self):
        print('Engine stopped.')

# Composition
class Car:
    def __init__(self):
        self.engine = Engine()

# Inheritance
class MechanicalEngine(Engine):  # Child class, Derived Class
    def __init__(self):
        self.max_speed = 120

motorcycle_engine = MechanicalEngine()
motorcycle_engine.start()  # MechanicalEngine class inherits attributes and methods of Engine class.
```

## Private and Public

Each method or attribute of a class that starts with `__` is considered private and everything else is public. All
special methods are private.

* `super()`

# Generators

* `yield`
* `yeild from`

# Decorators

Example: Decorator to calculate up execution time.

## Decorator Factory

Homeworks:
* Describing what some codes do.

Notes to talk:
* Printing structures and customization.

Examples:

* Prime number function.
* Prime number generator.
* Fibonacci number recursive function.
* Fibonacci number generator.
* Web crawler.
