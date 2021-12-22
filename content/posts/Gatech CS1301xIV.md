---
title: Gatech CS1301xIV
author: "Ryan"              # 文章作者
description : "Intro to Computing in Python by David Joyner"    # 文章描述信息
date: 2021-11-5            # 文章编写日期
draft: false
---
# Unit 5
## Chapter 5.1: Objects
### Basic Concepts
- **Object-oriented programming:** A programming paradigm where programmers define custom data types that have custom methods embedded within them.

- **Object:** An object is a custom data structure that organizes and encapsulates variables and methods into a single data type. It is used near-interchangeably with “instance.” It's like the general 'prototype' or 'template'.

- **Class:** A custom data type comprised of multiple variables and/or methods. Instances or objects are created based on the template provided by the class. A class is a generic structure for a certain kind of data. An instance, on the other hand, is a specific example.

### Classes and Instances in Python
```python
#Define the class Name
class Name:
    def __init__(self):
        self.firstname = "[no first name]"
        self.lastname = "[no last name]"

#Define the class Person
class Person:
    #Create a new instance of Person
    def __init__(self):
        #Person's default values
        self.name = Name()
        self.eyecolor = "[no eye color]"
        self.age = -1
		
#Create a new Person and assign it to myPerson
myPerson = Person()  # with default values
#Print myPerson's name's firstname
print(myPerson.name.firstname)
#Change myPerson's name's firstname to David
myPerson.name.firstname = "David"
#Print myPerson's name's firstname
print(myPerson.name.firstname)
```
`__init__` is called whenever we create a new instance of a class. It initializes an instance of that class.

`self` is a keyword that tells Python to define variables for the instance as a whole. Any other code inside this class would be able to see those variables, as long as it accessed them with `self` as well. Besides, because it starts with `self`, the variable age exists, as long as this class or this instance exists. But if we left off `self`, then the variable would cease to exist at the end of this method. 

**Every method defined inside a class should have self as the first parameter.** We'll never have to pass in an argument for it though. Self by default just sees all the variables associated with this instance of the class.

When we call the class name to create an instance, the color of the class name that was called is the same as `__init__`. The reason is that when we call the class, it actually calls our init function. This creates a new instance of this class and then returns that instance to be set equal to the variable name on the left.

Benefits of using objects instead of dictionaries:
1. With a dictionary, we might not have created a certain key. But with classes, we guarantee that every variable created in that initializer actually exists.

2. Classes can have methods as well as variables. Dictionaries were purely ways of organizing data, but that data couldn't do anything on its own. Dictionaries only store data, whereas classes can themselves act on data.

### Encapsulating Methods in Classes
Encapsulation: The ability to combine variables and methods into class definitions in object-oriented programming. It helps avoid modification or misuse of data by other functions or programs.

Methods are what make encapsulation truly powerful in classes. A method is a function defined inside of a class. The method scope is defined as the normal scope of a function for that language plus any variables that are visible in the instance of the class as a whole.

In practice, the four common method types we'll discuss below -- constructors, destructors, getters, and setters -- are more important to other languages than to Python. Constructors are present, but you'll rarely use destructors in Python; and getters and setters are antithetical to "Pythonic" thinking.

### Common Method Types
**Constructor:** A common type of method in writing classes that specifies some code to automatically run whenever a new instance of the class is created. The constructor often has parameters that provide values to initialize the variables defined by the class.

**Destructor:** A common type of method in writing classes that specifies how the instance of a class is to be destroyed/deleted, such as releasing its memory back to the computer. Destructors can be useful if you're dealing with massive quantities of data and find yourself running out of computer memory.

