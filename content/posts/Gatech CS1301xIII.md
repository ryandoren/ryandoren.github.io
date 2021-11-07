---
title: Gatech CS1301xIII.md
author: "Ryan"              # 文章作者
description : "Intro to Computing in Python by David Joyner"    # 文章描述信息
date: 2021-10-30            # 文章编写日期
draft: false
---
# Unit 4
## Chapter 4.1: Data Structures
Data structures are approaches to organizing abstract data types, such that the data can be accessed efficiently.

- **List-Like Structures:** Also referred to as sequences and collections, a data structure that holds multiple individual values gathered together under one variable name, accessed via indices. This includes structures like **lists, arrays, and tuples**. Lists are simultaneously a general type of data structure and a specific data type in some languages.

- **Index:** A number used to access a particular element from a list-like data structure. Traditionally, most programming languages assign the first item of a list-like data structure the index 0.

- **String:** A data structure that holds a list, or a string, of characters.

- **Lists:** A data structure that holds multiple individual values gathered together under one variable name, accessed via indices. Similar to arrays and tuples.

- **File Input and Output:** The complementary processes of saving data to a file and loading data from a file, generally such that the state of the memory of the program is the same after saving and loading have occurred.

- **Dictionaries:** A data structure comprised of key-value pairs, where a key is entered into the dictionary to get out a value. Similar to or synonymous with Maps, Associative Arrays, HashMaps, and Hashtables.

### Passing by Value vs. Passing by Reference
- **Passing by value**: Values themselves being passed back and forth. The functino never knows your variables and you never know the function's variables. When passing by value, you're simply handing off the value and the function can't actually change your variable.

- **Passing by reference**: The function has access to your actual variables and could modify them. You and the function are accessing the same variables.  When passing by reference, you're handing the variable itself to the function and the function can modify the variable if it wants.

The difference between passing by value and passing by reference comes down to whether or not you want the function to be able to change the values of the variables directly, or if you simply want it to receive the values themselves without being able to access the variables. (whether the function has the direct access to your original files📕)

In some languages like C++, you can choose whether to pass a variable by value or by reference. However, Python deals with passing-by-value and passing-by-reference a little strangely. **In reality, everything is passed by reference**, but *some primitive data types like integers often appear to be passing by value*. This is due to mutability.
![enter description here](./images/1636285446036.png)

### Variable Assignments
When we type down an assignment statement `b = a`, did we assign `a` only to the current value of `b` or does `b` follow `a` around and copy its value whenever it changes? In other words, did we tell `b` you now equal the **current value** of `a` or did we tell `b` you should always equal `a`?
```python
>>> a = 5
>>> b = a
>>> a = 7
a = 7, b = 5
```
```python
>>> a = ["One", "Two", "Three"]
>>> b = a
>>> a.append("Four")
a = ["One", "Two", "Three", "Four"], b = ["One", "Two", "Three", "Four"]
```
There are two important takeaways here: 
1. We can refer to the same data by different names-- we can have multiple variables that point to the same data and if you access and modify the data via one variable name, it also modifies the data for any other variable names that point to the same data.

2. As with our function calls, we see that integers and lists behave differently. An integer will not keep its data up to date if the variable to which it is set changes, but that's not the case for a list. Again, this comes down to mutability.

Python has something called immutable data types, data types whose values cannot be changed.

