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
- **Special Characters:** Tab, Newline characters (carriage returns & line feed)
- **Newline Character:** A Unicode character, either LF (line feed) or CR (carriage return), that is rendered as the beginning of a new line of text. (Mac uses LF to represent its newline while Windows uses both LF and CR.)

### Declare Strings
- Python won't terminate the string until it encounters the same mark that you used to start the string `'`,`'''`,`"`.
- When a string is declared with triple quotation marks or triple apostrophe's, everything inside them will be interpreted as part of the string.
```python
s = '''123
	   456'''
----------
123
456
```

### String Concatenation and Slicing
- Concatenation: use plus operator.
- Sliceing: Remember that string is a kind of list, so we can use `string[start:end]`[start, end) to slice strings (a positive number counts from the beginning, a negative number counts from the end.). Remember also, strings are an immutable type. That means we can't modify their values. **We can only use [ ] to access individual characters but not modify them**.

### String Searching
The `in` operator can be used with strings to check if a substring is part of a string.

The **find method** `string.find(text, [start], [end])` is a member of the string type, and it takes as input the substring we want to find. It returns **the first index** where that substring was found or -1 if it wasn't found anywhere. We can use **a while loop** to get all the indices that the targeted substring has appeared.
```python
myString = "ABCDEEDGHYRCDELKCDEJNCECDEGGHEDCDEPJ"
findString = "CED"
currentLocation = 0
while currentLocation >= 0:
	print(findString, "found at", currentLocation)
	currentLocation = myString.find(findString, currentLocation+len(findString))
```
If we just care about how many times the targeted substring has appeared in the given string, we can use the **count method**. The count method will count the number of times the string in parentheses occurs inside the string calling count.
`myString.count(findString, [start], [end])`

### Other Useful String Methods

> 🐍[String Methods at Python.org](https://docs.python.org/3.7/library/stdtypes.html#string-methods)
- `string.split([separator])` The split method divides the string calling it into several substrings based on the separator character and returns to a string list. The default separator is space. If we use **period** as the separator, every sentence except the first will start with an empty space. Second, there will be an empty string at the end, because **Python sees the period at the end of the string, and at that point, it closes off the previous string and starts a new one.** It doesn't know that it's not going to find anything in that new one. And so we end up with an extra empty string at the end of our list. The solution is to use **period space** `', '` as the separator.
- `string.capitalize()` capitalizes the string
- `string.lower()` all-lowercase version
- `string.upper()` all-uppercase version
- `string.title()` capitalizes any character found after a space
- `string.strip([character])` strips out any whitespace before or after the string. We could also supply an argument to strip, to strip out a different character. But if we don't, it assumes to strip out spaces.
- `string.replace(string1, string2)` replaces string1 with string2
- `string.join(list)` uses the string calling the join method to concatenate each item from the list of strings
> Split and join are basically reverses of each other.

Notice that string methods **do not** actually change the value of the string. They just return what would be the value if that operation was applied. To actually save it, we would have to define antoher string and assign the return value of the string method to that newly defined string.

### External Materials
🐍 [Strings from *How to Think Like a Computer Scientist*](https://runestone.academy/runestone/books/published/thinkcspy/Strings/toctree.html)
🐍[Python Strings from *Google for Education*](https://developers.google.com/edu/python/strings)

> - A string literal can span multiple lines, but there must be a backslash \ at the end of each line to escape the newline. String literals inside triple quotes, """ or ''', can span multiple lines of text.
> - Enclose the whole expression in an outer set of parenthesis -- then the expression is allowed to span multiple lines.

## Chapter 4.3: Lists
### Basics
- **List-like Structures:** Also referred to as sequences and collections, a data structure that holds multiple individual values gathered together under one variable name, accessed via indices. It would encompass other data structures like dictionaries and maps.
- **Homogeneity:** A property of lists determining whether they can accept multiple types of variables. A homogenous list can only accept one type of variable; a nonhomogenous or heterogenous list can accept multiple types.

Nearly every programming language has some concept of a list, but the terminology and the specific details differ significantly. **One major way different languages differ in their implementations of lists is mutability.** Mutability of a list involces: 
1) whether the values of the list can be changed
2) whether the size of the list can be changed

Some list implementations will allow us to append new items to the end, while others require you to state in advance how many items can fit in the list. Generally, the latter is more common for lower level languages like C where we manage memory more deliberately.

**Another major way list-like structures may differ is whether they accept multiple data types**. This is called **homogeneity and lists**. In some list implementations, every item in a list must be the same type. Other languages don't have this restriction.

> A **list** is a data structure that contains multiple values **accessed via an ordered numerical index**. This is in contrast to **dictionaries and hash tables and other data structures**. They can also contain multiple values, but they can be **accessed via non-numeric indices**.

List-like structures can go by various different names like *lists, arrays, tuples, vectors, tables, and more*. Oftentimes, *array* is used to refer to a more primitive structure that *only supports changing the existing values*, whereas *list* refers to more complex data structures that *support sorting and inserting and other operations*. *Tuples* are, most often, *immutable*.

### Tuples in Python
>🐍 [Documentation on tuples from Python.org.](https://docs.python.org/3/tutorial/datastructures.html#tuples-and-sequences)
- **Tuple:** An immutable form of a list-like structure in Python. Like strings, we can't add values to the end of a tuple and we can't change the current values of anything inside the tuple or sort them.
- **Lists:** A mutable form of a list-like structure in Python.

Declare a tuple: `tuple = (value1, value2, value3)`

Tuples can have multiple data types within them. This follows Python's general procedure of being what we call **loosely typed**. Python never really cares about what data types you're using until you try to do something that you can't do, like multiplying a string by a float, or printing the length of an integer.

Tuples can be accessed and sliced as other list-like data structures. However, they also have a fancy little syntax for **unpacking**: `(variable1, variable2, variable3) = tuple` What this does is it one by one assigns the values of the tuple to the different variables contained on the right side of this assignment statement.

The most usefulness of tuples may be functions. Generally functions can only return one variable or one value. But since tuples can pack multiple values into just one, they in some way let us return multiple values  out of a function: 
```python
def function(args):
	function body
	return (value1, value2, value3)  # return a tuple allows a function to return multiple values
	
(variable1, variable2, variable3) = function(args)  # assignment using tuple unpacking
```
Tuples can be nested. You can have a tuple of tuples. How to access an individual value inside of a nested tuple: use two sets of brackets. `tuple[num1][num2]` The first one specifies which tuple we want and the second one specifies which value from that tuple we want.

### Lists in Python
> 🐍[Documentation on lists from Python.org](https://docs.python.org/3.7/tutorial/datastructures.html).

Everything we've seen in the past with both strings and tuples can also be used for lists. The only real difference is that whereas we define a string with quotation marks and a tuple with parentheses, we define a list with brackets. (access, slice, unpacking, function return, nested...)

What differentiates lists is that they're **mutable**. That means we can change their values. We can add values to them, we can remove values from them, we can change the current value of certain values in the list. We can reorder them.

```python
list.sort()  # A method inside the list data type and sorts the values according to some internal logic. For integers it just sorts from the lowest to the highest (ascending). 

list.reverse()  # reverses the current order of the list, not necessarily the sorted order of the list.

list1.extend(list2)  # takes the values of list2 and puts them
at the end of list1.

list.insert(location, value)  # inserts an item at a certain place in the list.

list.remove(value)  # removes a certain value.

del list[]  # deletes items by location in the list.

list.pop([index=-1])  # removes the last item (by default) of the list and returns it, index is optional.

list.index(value)  # finds the index of a certain value.

list.count(value)  # counts how many times a certain value appears.

list.copy()  # returns a shallow copy of the list. Equivalent to a[:].

list.clear()  # removes all items from the list. Equivalent to del a[:].
```

> - It's important to note that **calling the method actually changes the value of the list**. Remember, when we called methods on strings they didn't change the value of the string. That's because lists are mutable, and strings are immutable.
> 
> - The `sorted(list)` function can also be used for sorting, but it does not change the value of the original list. It can be applied to any Iterable object, which means that it also accepts strings, sets, dictionaries when they are passed to it.
> 
> - Difference between .extend() and .append(): `extend()`, on the one hand, takes an iterable (list, set, tuple or string), and adds each element of the iterable to the list one at a time. `append()`, on the other hand, adds its argument to the end of the list as a single item, which means that when the `append()` function takes an iterable as its argument, it will treat it as a single object. **`extend()` is a more efficient version of calling `append()` multiple times.**

Lists are mutable. That means if we pass a list to a function or method and change the values of the list, those changes will persist out to our main program. So when dealing with lists, or any other mutable data type, we have to be careful to understand that all modifications we make to the list will persist.

### Lists vs. Tuples
Generally, though, there are a couple conventions we follow to decide whether to use lists or tuples:

1. We often use tuples when we're definitely dealing with a pre-determined number of items. We use lists when the ability to add or remove from the list would actually be useful and relevant.

2. We usually use lists when the individual things on the list are qualitatively similar. We use tuples if they're qualitatively different. 

3. **Lists are used for alike data types** by convention because we tend to *execute the same body of code* for each item in the list. Tuples are more often used to represent information that's unpacked into unique variables, those have qualitatively different meanings. And so you're not going to just run some code on every item in a tuple. For that same reason, it's more normal for **tuples to have different data types** within them because we're not generally expecting to be able to iterate over a tuple in the same way.

> If you’re defining a constant set of values and all you’re going to do with it is iterate through it, use a tuple instead of a list. It will be faster than working with lists and also safer, as the tuples contain “write-protect” data.

### Convert A List To...
You convert a list to a string by using `''.join()`. This operation allows you to glue together all strings in your list together and return them as a string. **Note** that if your list only contains integers, you should convert the elements to strings before performing the join on them. Read more [here](https://docs.python.org/3/library/stdtypes.html#str.join).

You can change a list to a tuple in Python by using the `tuple()` function. Pass your list to this function, and you will get a tuple back!

You can change a list into a set with the `set()` function. Just pass your list to it! But remember, a set is an unordered collection of unique items. That means not only means that any **duplicates** that you might have had in your original list **will be lost** once you convert it to a set, but **also the order** of the list elements.

A dictionary works with keys and values, so the conversion from a list to a dictionary might be less straightforward. You will need to make sure that elements are interpreted as key-value pairs. The way to do this is to select them with the slice notation and pass them to `zip(keys, values)` (keys/values=list[start:end:step]) which zips elements together. 

### Clone Or Copy A List
There are a lot of ways of cloning or copying a list:

*   You can slice your original list and store it into a new variable: `newList = oldList[:]`
*   You can use the built-in `list()` function: `newList = list(oldList)`
*   You can use the `copy` library:
    *   With the `copy()` method: `newList = copy.copy(oldList)`
    *   If your list contains objects and you want to copy those as well, you can use `copy.deepcopy()`: `copy.deepcopy(oldList)`

> **Note** that when you use the ‘simple’ copy (shallow copy) methods and has modified the copied list, if the modification is done to the first layer, then nothing would be changed to the original list; but if the modification is done to a deeper layer, the original list would also be modified. In contrast, if you use the `deepcopy()` method, nothing of the original list will be change whatever modification has been done to the copied list.
> ```python
> import copy as c
> objectList1 = ['a','b',['ab','ba']]
> objectList2 = ['a','b',['ab','ba']]
> 
> shallowCopiedList = objectList1[:]
> deepCopiedList = c.deepcopy(objectList2)
> 
> shallowCopiedList[0] = 'c'
> deepCopiedList[1] = 'd'
> shallowCopiedList[2][0] = 'cc'
> deepCopiedList[2][1] = 'dd'
> 
> print(objectList1)
> print(objectList2)
> ----------
> ['a', 'b', ['cc', 'ba']]
> ['a', 'b', ['ab', 'ba']]
> ```

### List Comprehension
List comprehension is, basically speaking, a way of elegantly constructing your lists.
```python
myList = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
[x**2 for x in range(10)]
[x**2 for x in range(10) if x%2==0]
[(lambda x: x*x)(x) for x in myList]  # anonymous function (lambda x: x*x)(x) is like f(x)
[(x, y) for x in [1,2,3] for y in [3,1,4] if x != y]
[[row[i] for row in matrix] for i in range(4)]

# Counting all items in a list with count()
list= ["a","b","b"]
[[x,list.count(x)] for x in set(list)]

# Counting all list items with Counter()
from collections import Counter
list = ["a","b","b"]
Counter(list)  #  Counter() is generally faster when you want to count all list items.
```
### Split A Python List Into Evenly Sized Chunks
To split your list up into parts of the same size, you can resort to the `zip()` function in combination with `iter()`:
```python
x = [1,2,3,4,5,6,7,8,9]
y = zip(*[iter(x)]*3)  # Split x up in chunks of 3
list(y)  # Use list() to print the result of zip()
----------
[(1, 2, 3), (4, 5, 6), (7, 8, 9)]
```


### Stacks: LIFO Structures
“Last-In-First-Out” (LIFO) paradigm.

1. We can only access the *most recently-added* (newest) item on the list;
2. We can only access it by removing it from the list.

E.g., putting dishes in the sink one on top of the other as they get dirty, then washing them when the sink gets full.
```python
stack=[value1, value2, value3]
stack.append(value4)
stack.pop()
```

### Queues: FIFO Structures
“First-In-First-Out” (FIFO) paradigm.

1. We can only access the *least recently-added* (oldest) item on the list;
2. We can only access it by removing it from the list.
```python
queue=[value1, value2, value3]
queue.append(value4)
queue.pop(0)
```

### Linked List
A list-like structure where the **location** of each item in the list is contained in the previous item in the list.

In a list, each spot tends to be a reference to a particular spot in memory that might be **completely disconnected** to the other ones. In effect, each spot in the list is more like an individual variable name that **could point to anywhere in memory**.

In a linked list, on the other hand, it only has one item that points to a place in memory. The first one. What would make it unique is that instead of the second spot pointing to the second address, it would be data contained in the first spot that point to the second address. Each value of the list contains the location of the next value of the list.

E.g., going on a scavenger hunt where each clue features a puzzle you must solve to find the next clue.

### External Materials
🐍 [Lists from *How to Think Like a Computer Scientist*](http://interactivepython.org/courselib/static/thinkcspy/Lists/toctree.html)
🐍[Python Lists from *Google for Education*](https://developers.google.com/edu/python/lists)
🐍[Python List Examples – Insert, Append, Length, Index, Remove, Pop from *The Geek Stuff*](https://www.thegeekstuff.com/2013/06/python-list/?utm_source=feedly)
🐍[18 Most Common Python List Questions](https://www.datacamp.com/community/tutorials/18-most-common-python-list-questions-learn-python#gs.=H0VpEs)

> - Note that, as you’re working with hashable items, checking membership (testing whether a certain element is part of your sequence) will go faster with sets than with lists.

| Hashable | Non-Hashable |
| --- | --- |
| Floats | Dictionaries |
| Integers | Sets |
| Tuples | Lists |
| Strings |   |
| `frozenset()` |   |

```python
# Flatten a list
sum(list, [])
print([item for sublist in listOfLists for item in sublist])

# Obtain the intersection of two lists
intersection = [list(filter(lambda x: x in list1, sublist)) for sublist in list2]
intersection = [[x for x in sublist if x in list1] for sublist in list2]

# If the order of your elements is not important and if you don’t need to worry about duplicates then you can use set intersection:
list(set(list1) & set(list2))
list(set(list1).intersection(list2))
```
## Chapter 4.4: Dictionaries
- **Dictionaries:** A data structure comprised of key-value pairs, where a key is entered into the dictionary to get out a value. Similar to or synonymous with Maps (a collection of keys mapped to values; Java, C++), Associative Arrays (PHP, JavaScript), and HashMaps/Hashtables (The term hash refers to the way in which the data structure is constructed). A dictionary would preserve the ability to give names to multiple values by way of keys.

- **Dictionary Key:** A value then, when passed into a dictionary, returns a corresponding value, like a word and its definition. Similar to a variable.

- **Dictionary Value:** A value returned in response to a key in a dictionary. Similar to a value of a variable outside a dictionary.

The major difference between a dictionary and a list is that the values of the list had to be accessed via numeric identifiers called indices or indexes. But dictionaries use keys instead of numeric indices/indexes. Besides, dictionaries aren't guaranteed to preserve order. In a list, the first item is guaranteed to be the first item unless it's changed; in a dictionary, the first key-value pair added might not be the first one accessed.

### Dictionaries in Python
We use [brackets] for lists, (parentheses) for tuples, {curly braces} for dictionaries. Each *key/value pair* in our dictionary is defined with a syntax *key colon value*. With a dictionary, we're bundling up multiple variables, but we retain the ability to give them each their own name.

Note that when we print the dictionary that we're defining, it actually prints in a *different order* than the way we defined it. Dictionaries carry no guarantee that the keys and values will be printed in the same order in which they were defined. It only guarantees that each value will stick with the correct key.

The persistence of keys, though, means that in a dictionary, **keys must be immutable values**. So we can use **strings, integers, floats, tuples** as keys, but **we couldn't use a list or a dictionary as a key** because those are mutable data types. The reason for this is that if the key changes, the dictionary wouldn't know what value was associated with it. So it must guarantee that the keys cannot change. Values, on the other hand, can change.

Editing a Dictionary:
```python
dictionary['newKey'] = newValue
del dictionary['targetKey']

if keyName in dictionary:  # check whether a key is in the dictionary

# traverse every item in the dictionary
for value in dictionary.values():  #  iterate over the values directly when not caring about keys; dictionary.values() returns a list of all the values in that dictionary

for key in dictionary.keys():  #  iterate over the keys when caring about values and their corresponding keys; dictionary.keys() returns a list of all the keys in that dictionary
	value = dictionary[key]
	
for (key, value) in dictionary.items():  # iterate over each tuple corresponding to a key and a value; dictionary.items() returns a list of (key, value) tuples in that dictionary
```
### Dictionary Applications
A dictionary of dictionaries: having names as our keys, having the value be another dictionary. And then the values for each key in that dictionary correspond to the type of data. This is getting very close to the idea of objects.
![enter description here](./images/1639824982211.png)

Word Count:
```python
myString = "This is the string whose words we would like to count. This string contains some repeated words, as well as some unique words. It contains punctuation, and it contains words that are capitalized in different ways. If the method we write runs correctly, it will count 4 instances of the word 'it', 3 instances of the word 'this', and 3 instances of the word 'count'."

myString = myString.replace(".","") #Remove periods
myString = myString.replace(",","") #Remove commas
myString = myString.replace("'","") #Remove apostrophes
myString = myString.lower() #Make all lower case
mySplitString = myString.split() #Split by spaces

wordDictionary = {} #Create empty dictionary
for word in mySplitString:  #For each word in the split string
    if word in wordDictionary:  #If it's already been found...
        wordDictionary[word] += 1   #Add one to its count
    else:   #Otherwise...
        wordDictionary[word] = 1 #Create it with value 1

print(wordDictionary)
```
Arrange seating chart for a wedding
```python
seatingChart = {"David" : 3, "Lucy" : 3, "Dana" : 2,
                "Addison" : 2, "Vrushali" : 1, "Bilbo" : 3,
                "Sara" : 1, "Lugos" : 1, "Mireia" : 1,
                "Partha" : 2, "Venijamin" : 1, "Terra" : 2, 
                "Tryphon" : 3, "Gevorg" : 1, "Raza" : 3,
                "Rein" : 3, "Sofia" : 2, "Perle" : 2}

#For each name, table pair in the seating chart
for (name, table) in seatingChart.items():  
    #Print the table for the name
    print(name, " is seated at table #", table, sep="")  

print()
#For each table number
for i in range(1, 4):   
    print("The guests at table #", i, " are: ", sep="", end="")
    #For each name, table pair
    for (name, table) in seatingChart.items():  
        #If the table numer is this number
        if i == table:  
            #Print the name
            print(name, end=" ")    
    print()
```
Classroom roster: lists as values
```python
classes = {"Math" : ["David", "Lucy", "Dana"],
           "Physics" : ["Addison", "Vrushali", "Bilbo"],
           "Chemistry" : ["Sara", "Lugos", "Mireia", "Perle"],
           "Computing" : ["Partha", "Venijamin", "Terra", "Sofia"],
           "History" : ["Tryphon", "Gevorg", "Raza", "Rein"]}

print("Students in Computing:", classes["Computing"])
#Add Francis to History
classes["History"].append("Francis")    
print("Students in History:", classes["History"])
```
Address book: lists/tuples as values (has to know the indexes of address, phone number, and email)
```python
addressBook = {"David": ("555 Home St", "4045551234", "david@david.com"),
               "Lucy" : ("555 Home St", "4045555678", "lucy@lucy.com"),
               "Dana" : ("123 There Rd", "4045559101", "dana@dana.net")}

print("David's Information:", addressBook["David"])
print("Dana's Phone Number:", addressBook["Dana"][1])  # Knowing that the phone number is at index one
```
Address book: dictionaries as values (refer to these individual values by keys instead of by indices)
```python
addressBook = {
"David": {"address" : "555 Home St", "phone" : "4045551234", "email" : "david@david.com"}, 
"Lucy" : {"address" : "555 Home St", "phone" : "4045555678", "email" : "lucy@lucy.com"}, 
"Dana" : {"address" : "123 Here Rd", "phone" : "4045559101", "email" : "dana@dana.net"}}

print("David's Information:", addressBook["David"])
print("Dana's Phone Number:", addressBook["Dana"]["phone"])
```
Grading students' answer sheets
```python
ANSWER_KEY = {"1" : "A", "2" : "B", "3" : "C", "4" : "D", "5" : "A"}

students={}
students["David"] = {"1" : "A", "2" : "B", "3" : "A", "4" : "B", "5" : "C"}
students["Terra"] = {"1" : "A", "2" : "B", "3" : "C", "4" : "D", "5" : "A"}
students["Lugos"] = {"1" : "A", "2" : "C", "3" : "C", "4" : "D", "5" : "A"}

#For each student and their answers
for (student, answers) in students.items(): 
    grade = 0   #Start grade at 0
    #For each question and answer
    for (question, answer) in answers.items():  
        #If the answer matches ANSWER_KEY's answer...
        if answer == ANSWER_KEY[question]:  
            grade +=1   #Increment their grade
    #Create a new key "grade" and assign it their grade
    students[student]["grade"] = grade  
#For each student and their answers
for (student, answers) in students.items(): 
    #Print the name and grade
    print(student, ": ", answers["grade"], sep = "", end = "; ")
```
### External Materials
🐍[Dictionaries from *How to Think Like a Computer Scientist*](http://interactivepython.org/courselib/static/thinkcspy/Dictionaries/toctree.html)
🐍[20. Dictionaries from *How to Think Like a Computer Scientist: Learning with Python 3*](http://openbookproject.net/thinkcs/python/english3e/dictionaries.html)

> ![enter description here](./images/1639828164603.png)
> ![enter description here](./images/1639828373969.png)
> ![enter description here](./images/1639828395942.png)

## Chapter 4.5: File Input and Output
**File Input and Output:** The complementary processes of saving data to a file and loading data from a file, generally such that the state of the memory of the program is the same after saving and loading have occurred.

Each file type has its own built-in, type-specific encoding. That encoding is properly unpacked by a program that knows how to read the file.  File types set up rules for how to interpret a file, and a program can only correctly interpret the file if it knows those rules.

Many languages actually require that file input and output be enclosed within a try block. Reading simply means that we're looking at the file's contents and reading it into our program. We're not changing the contents, just inputting it into our own code. Writing, on the other hand, means we're rewriting the file from scratch. When we write to a file, we, by default, erase it and rewrite it completely from scratch. With writing, we assume the file is a snapshot of the current state of our data, not a running log of the history of all of its changes. Appending also writes to the file, but it starts on the very last line of the file. Nothing is overwritten. New data is just added to the end.

### Writing Files in Python

```python
outputFile = open("OutputFile.text", 'w')  # w-write, r-read, a-append; Write will overwrite the current content of the file, append will add to the end of the file, and read will just read from the file without actually changing its contents.
outputFile.write(string)  # the write method can only write strings to files. By default write does not start a new line at the end of writing a particular line.
outputFile.writelines(list)  # takes as input a list of strings and automatically writes them to the file; doesn't append spaces or new line characters to the end of each item in the list.So, one solution would be:
outputFile.writelines('/n'.join(list))
print(content, file = outputFile)  # If we supply an argument for the keyword 'file' when calling our print function, then Python will write to that file instead of to the console.
outputFile.close()
```
### Reading Files in Python
Remember when loading from a file, the computer by default interprets everything as text. If we need to treat it as numbers or some other kind of data, we'll need to perform a type conversion.
```python
inputFile = open("OurtputFile.txt", 'r')
print(inputFile.readline())  # if we want to delete the newline character of each line, use print(inputFile.readline().strip())
myInt = int(inputFile.readline())

# loading into lists
for line in inputFile:  # starts from the line that has not been read
	myList.append(line.strip())
	
inputFile.close()
```
### Save and Load Functions
```python
#Saves inList to the file
def save(filename, inList): 
    outputFile = open(filename, "w")
    for item in inList: 
        print(item, file = outputFile)   
    outputFile.close()

#Loads from filename and returns a list of the contents
def load(filename): 
    inputFile = open(filename, "r")
    inList = []
    for line in inputFile:
        inList.append(line.strip())
    inputFile.close()
    return inList

myList = ["David", "Lucy", "Vrushali", "Ping", "Natalie", "Dana", "Addison", "Jasmine"]
save("OutputFile.txt", myList)
newList = load("OutputFile.txt")
print(newList)
```
### External Materials
🐍[Files from *How to Think Like a Computer Scientist*](http://interactivepython.org/courselib/static/thinkcspy/Files/toctree.html)