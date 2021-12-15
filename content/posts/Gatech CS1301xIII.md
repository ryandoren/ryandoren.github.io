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

### Mutability in Python
- **Mutability:** Whether or not a variable can have its value changed after being declared.

- **Mutable Variable:** A variable whose value can change after it has been declared.

- **Immutable Variable:** A variable whose value cannot change after it has been declared.
  
**Python passes all arguments by reference**. But for all practical purposes, some data types seem to be passed by value. The reason they acted this way is because they were **immutable**.

Let's talk about the way Python actually does this. We have a variable called `myInteger`, and we assign it the value `1`, we're telling it to *point to a place in memory that stores the number 1*. When we use `myInteger`, we're actually looking up its value. Now when we say `myInteger` equals `2`, what Python does is kind of weird. It *grabs a new area of memory,* puts the number 2 there, and tells `myInteger` to *point out that new location instead of the old location*. What that means is that the old value is still there in memory. The value didn't change. We didn't change the number `1`. Instead, we just created a new place in memory and told `myInteger` to point to that instead. **Changing the value of myInteger changes the spot in memory that it points to, but it doesn't actually change the value stored in the original spot of memory**. Note that a function can't change what value the variable used in the main program is pointing to. It can only change the value its own copy of that variable is pointing to. (Because the scope of variables defined in the function were until the function ended.)

 The computer has to have some way of identifying the location in memory that stores the data. Multiple names or different names can point to the same place in memory, so the place memory really needs **a fundamental unchangeable name**. This is called a **memory address**. It tells the computer where to find a particular value for a particular variable name.
```python
print(id(variable/value))  # Printing Memory Addresses
```

> - Immutable data types: integers, float, strings (Changing them changes the address where they can be found, seem like passing by value.)
> - Mutable data types: lists (Changing them **does not** change the address where they can be found. note that it's **changing/modifying** them, **not reassigning** them to a whole new value.)
> - Immutable variables pointing to the same value have the same id; however, for mutable variables, even they point to the same value, they have different ids, enless they are connected by `=`

### Functions vs. Methods 
Methods are functions accessed through dot notation; they are functions contained within data types. Just like functions, methods can return certain types of data as well.
```python 
 str.isdigit()  # a Boolean method, check to see if a string represents a number, returns either a true or a false value
 
 str.isupper()  # a Boolean method, check to see if all the letters in the string are uppercase, returns either a true or a false value
```

### External Materials
🐍[Basic Data Structures](https://runestone.academy/runestone/books/published/pythonds/BasicDS/toctree.html)
🐍[Python Data Structures](https://python.swaroopch.com/data_structures.html)

## Chapter 4.2: Strings
### Basic Concepts
- **String:** A data structure that holds a list of characters.
- **Character:** A single letter, number, symbol, or special character.
- **Unicode:** A computing industry standard that sets what hexadecimal codes correspond to what characters, so that text appears consistent across platforms. (263A should be a simple smiley emoji 😊)
- **Hexadecimal:** A short-hand expression of the ones and zeroes that comprise computer data, comprised of 16 characters, 0 through 9 and A through F.