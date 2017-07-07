# Introduction

## What is Python?

[Python](https://www.python.org/) is an interpreted, general purposed language that is designed in 1991. Python can be used for object oriented and functional programming. The language usage areas are tremendous. Some of them are, system programming, graphical user interfaces, game development, developing back-end, machine learning, visualizing data, media processing, scientific programming and many many more.

Python have very readable and simple syntax to write code. Nowadays python frameworks and libraries are every where.

There is only one drawback with python. That's runtime speed. But even this problem is almost solved by [PyPy](https://pypy.org/) project.

## What is PyCharm?

As a developer we need an environment to code in it. The best environment that I found is [PyCharm](https://www.jetbrains.com/pycharm/), it has many features like auto-completion, debugging, version controller support, ... .

## What is Jupyter?

An integrated development environment like pycharm isn't exactly what need for most of this course. We are dealing with watching effects of each line of code we write. [Jupyter](https://jupyter.org/) is what we use here.

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
$ virtualenv .venv    # Creating python virtual environment
$ source .venv/bin/activate  # Activating virtual environment
$ deactivate          # Deactivating virtual environment
```

3. Comments
4. PEP8
5. Numbers and Mathematics
6. Variables and Naming
7. Strings
    1. Escape Sequences
    2. Input from user
8. Functions
    1. Parameters
        1. Passed by Reference
        2. Passed by Value
        3. Default Value
        4. Unordered Parameter Passing
    2. Return
    3. Documentation
        1. Help
    4. global
    5. lambda
    6. pass
9. Decision Making
    1. if, elif, else
    2. <, <=, >, >=, ==, !=
    2. True, False, and, or, not
        1. Use `is` for readability
    3. Binary operators
10. Loops
    1. for
        1. `range`
    2. while
    3. break
    4. continue
11. Lists
    1. `append`
    2. `del`
    3. `len()`
12. Indexing and Slicing
10. Packing & Unpacking
12. Tuples
13. Dictionaries
9. Files
    1. Reading
    2. Writing
    3. Appending
    4. Binary mode
    5. General Strings
10. Modules
    1. Importing other modules
    2. Creating other modules
10. Exceptions
    1. raise
    1. try
    1. except
    1. finally
    4. assert
11. Classes
    1. Object Oriented Programming
        1. Class
        2. Object
        3. Instance
        4. Self
        5. `__init__`
        6. Attribute
        7. Methods
        8. Decorators
        1. Inheritance (is a)
        2. Composition (has a)
11. `with`
12. Generators
    1. yield
12. Small Project using Kivy or PyGame

Homeworks:
* Describing what some codes do.

Notes to talk:
* Printing structures and customization.
