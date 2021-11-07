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
**Passing by value**: Values themselves being passed back and forth. The functino never knows your variables and you never know the function's variables.
**Passing by reference**: The function has access to your actual variables and could modify them. You and the function are accessing the same variables.