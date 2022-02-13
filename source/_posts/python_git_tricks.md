---
title: Tricks on Python and Git
date: 2022-02-09 15:39:50
tags:
- python
---
# Errors in Python program
- Every function should have docstring. 
- Two types of python error: Syntax error and exception error
> A syntax error occurs when a programmer writes an incorrect line of code. Most syntax errors involve missing punctuation or a misspelled name. If there is a syntax error in a compiled or interpreted programming language, then the code won't work.<br>
> An exception is an event, which occurs during the execution of a program, that disrupts the normal flow of the program's instructions.

- try and except function to handle errors
```
try:
    from my_cal import sqrt
except ModuleNotFoundError:
    from math import sqrt
    print("My_cal not found")
```

## How to raise an error 
> I don't want people to use my function incorrectly.
```
sqrt(-4)
```
Raise error instead of user interface to deal with negative input. 
```
if n < 0:
    raise ValueError("{} is a negative number".format(n))

if type(a) == str:
    raise TypeError("Cannot handle a string.")
```


