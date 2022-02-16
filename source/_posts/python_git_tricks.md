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

# Software Design Principle and Code Smell

## Least Surprise
- Function and variable name make sense. 
- No unexpected side effects. 
> "You have to call A before B, othersie the program will crash. " (Bad example)

## Don't Repeat Yourself
- The same constant or piece of codes should only appear once. 
- Why repeat is a bad thing in programming?
- How could we avoid repeating ourselves?
  - If the same piece of codes needed more than once, wrap it into a function. 
  - If the constant is needed more than once, give it a name. 


## SOLID
### Single Resonsiblity
- One function should do only "ONE THING"
- Uncle Bob: Gather the things that change for the same reasons. Separate those things that change for different reasons. 
- If your description of a function has multiple "and", then it probably needs to be separated into several functions. 

### Open / Close
> Adding a new feature could destroy the whole program?
- Software entities should be open to extension but closed to modification. 
- If else could be the big enermy. 
- Function approach to follow open / close 
- Easier to do unit testing
> Different Coverage Level
> - Statement Coverage
> - Branch Coverage (satisties our assignments and final project)
> - Condition coverage


> The following three principles are useful in large project. 
### Liskov Substitution Principle
- Functions that use pointers or references to base classes must be able to use objects of derived classes without knowing it. 


### Interface Segregation Principle
- Many client-specific interfaces are better than on a general-purpose interface. 

### Dependency Inversion Principle
- High level modules should not import anything from low level modules. 
- Abstractions should not depend on details. 

## Code Smell
> Code is hard to read and use. 

- Too many parameters
> combine them into list, dict, or strings.
- Too long variable name
- Too short variable name
- Too many return of data
- Too long function 
- Excessive comments 
- Excessively long line of code (PEP8)


# Git 

[What if I made some change on the wrong branch?](https://stackoverflow.com/questions/8085838/how-to-move-the-changes-from-one-branch-to-another-branch-git)
> Main branch is for deployment in the industry. 
> Git conflicts.
