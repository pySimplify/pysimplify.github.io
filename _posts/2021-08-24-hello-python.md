---
layout: post
title: How to create a class in Python
# date: 2021-08-24
categories: python
---

# What are classes in Python

Classes are a way to group together related data and functionality.
`class` is a keyword that tells Python to create a class.

```py
class MyClass:
    ...
```

In Python classes have a special method called `__init__`. This method is called whenever a new object is created.

The `__init__` method is called automatically every time the class is being used to create a new object.

```py
class MyClass:
    def __init__(self, param1, param2):
        self.param1 = param1
        self.param2 = param2
```

Dunder methods are methods that start with double underscores. They are used to implement special functionality. For example, `__init__` is used to initialize the object. `__str__` is used to print the object.
