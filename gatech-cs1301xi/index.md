# Gatech CS1301xI



----------
# Extra materials

> 1. [How to Think Like a Computer Scientist: Interactive Edition](https://runestone.academy/runestone/books/published/thinkcspy/index.html)
> 2. [How to Think Like a Computer Scientist: Learning with Python 3](http://openbookproject.net/thinkcs/python/english3e/)
> 3. [Python for Everybody (PY4E)](https://www.py4e.com/lessons)
> 4. [Hands-on Python 3 Tutorial](http://anh.cs.luc.edu/python/hands-on/3.1/handsonHtml/index.html)
> 5. [Beginning Python Programming for Aspiring Web Developers](http://www.openbookproject.net/books/bpp4awd/index.html)

# Course Outline
## Unit 1
1. **Computing:** the basic principles of working with computers.
2.  **Programming:** the general workflow of writing and running programs. Writing code, compiling it, executing it, and evaluating the results.
3.  **Debugging:** the process of finding and fixing errors in your programs.
## Unit 2
1.  **Procedural Programming:** The general idea of writing sequences of instructions for the computer to perform.
2.  **Variables:** Creating and modifying data in our programs.
3.  **Logical Operators:** Establishing the truth or falsehood of relationships among variables in our programs.
4.  **Mathematical Operators:** Using arithmetic operators (addition, multiplication, etc.) to modify the values of variables in our programs.
## Unit 3
1.  **Control Structures:** The general idea of lines of code that can control other lines of code.
2.  **Conditionals:** Lines of code (called if statements) that check logical expressions to see if certain code blocks should run.
3.  **Loops:** Lines of code that instruct the computer to repeat a block of code until some condition is met.
4.  **Functions:** Miniature programs within a larger program, each with their own input, code, and output.
5.  **Exception Handling:** Lines of code that instruct the computer how to fail gracefully when errors are encountered.
## Unit 4
1.  **Data Structures:** The general idea of data types more complex than individual letters and numbers.
2.  **Strings:** Ordered series of characters that often represent natural human language.
3.  **Lists:** Ordered series of other kinds of data, collected under one variable name and accessed via numeric indices.
4.  **File Input/Output:** Writing a program's data to a file so it can later be re-loaded after the program is closed and reopened.
5.  **Dictionaries:** Pairs of keys and values collected under one variable name, like lists with non-numeric indices.
## Unit 5
1.  **Objects:** Creating and using custom data types so our programs can reason about the world the way we do.
2.  **Algorithms:** Complex sequences of instructions that transform data or generate useful conclusions.
----------


# Unit 1
## Chapter 1.1: Computing
### Programming Vocabulary
- **Code**: Commands given to a computer in order to perform a task.
- **Line of code**: A single command.
- **Program**: A collection of lines of code that serve one or more overall functions.
- **Input** (files, user input, websites) 👉 code 👉 **output** (files, screen, sound)
- **Compile**: To translate human-readable computer code into low-level commands the computer can execute. In the programming flow, this functions as reading over code and looking for errors. (proofreading by compilers)
- **Run/Execution**: Running some code and having it actually perform its operations.
> Compiling just makes sure what we told the program to do makes sense; running checks whether the program actually do what we want it to do.

Compilation could potentially be skipped.
- Languages that require compilation are called **static/compiled**  languages.
- Languages that do not require compilation are called **dynamic/interpreted**  languages.

> Two kinds of programs process high-level languages into low-level languages: **interpreters and compilers**. An interpreter reads a high-level program and executes it. It processes the program a little at a time, alternately reading lines and performing computations. 
![Interpreter](./images/1634540777963.png)

> A compiler reads the program and translates it *completely* before the program starts running. In this case, the high-level program is called the **source code**, and the translated program is called the **object code** or the executable. Once a program is compiled, you can execute it repeatedly without further translation. 
![Compiler](./images/1634540772278.png)

> Many modern languages use both processes. They are first compiled into a lower level language, called **byte code**, and then interpreted by a program called a **virtual machine**. *Python uses both processes*, but because of the way programmers interact with it, it is usually considered an interpreted language.


### Programming Language
Categorization of languages: 
- **Static & Dynamic**: whether compilation is required
- **Hight-level languages** involve a great deal of abstraction from the low-level details of the computer like memory, whereas **low-level languages** such as machine languages or assembly languages require these details to be addressed manually.

[Popularity of different languages](https://www.tiobe.com/tiobe-index/)

> C++ and C# are two successors to the programming language C, which is a low-level language used a lot in developing operating systems, video games, and other highly complex programs. C++ adds a few more features to C, while C# is more of a high-level version. Java, C, C++, and C# are static, compiled languages; Python is the top dynamic, scripting language on this list.

### Console vs. GUI
- Graphical user interfaces (GUIs): An output medium that uses more than just text, like forms, buttons, tabs, and more. Eg. a web browser, a word processor like Microsoft Word, a smartphone app, a modern operating system like Windows or Mac OS.
- Console: An output medium for a program to show exclusively text-based output. Eg. command line interfaces like the terminal on a Mac or the command window on a PC.

### Fundations, language, and domain 
- **Foundations** are the *core principles of computing* that transcend specific programming languages.
- These foundational principles are then *implemented* in specific **programming languages**.
- You then *apply* them to a particular **domain**.

### Python
- Python is a **high-level, platform-independent** programming language. Python abstracts further away from the inner workings of the computer than lower-level languages (like memory management), thus is easier to use.
- Python is **dynamic & interpreted**, which means that Python will *run our code line by line* when we ask it to without trying to compile it first. That opens up the possibility of using Python in a command line interface where we write and run lines of code one at a time. Whereas in the **scripting mode**, we write a bunch of code, then *run it all at once*.
- The main takeaway of Python being an interpreted language is that we might not be aware of errors until we actually try to run those lines.
 ### Extra materials
1. [How to Think Like a Computer Scientist: Interactive Edition](https://runestone.academy/runestone/books/published/thinkcspy/index.html)
2. [How to Think Like a Computer Scientist: Learning with Python 3](http://openbookproject.net/thinkcs/python/english3e/)

## Chapter 1.2: Programing
- **Programming** is an iterative process of writing code, attempting to run it, and evaluating the results (write⇨run⇨evaluate cycle). Interchangeable with **coding**.
- Work in Small Chunks
- Chaining Together Instructions
- Debugging to address errors, incorrect results

## Chapter 1.3: Debugging
- **Debugging:** Resolving problems in code, whether it be errors thrown in compilation or running or mismatches between the desired and observed output.

> The terms "bug" and "debugging" are popularly attributed to Admiral Grace Hopper in the 1940s. While she was working on a Mark II Computer at Harvard University, her associates discovered a moth stuck in a relay and thereby impeding operation, whereupon she remarked that they were "debugging" the system.

![](./images/1634551637826.png)

### Types of errors
- **Compilation Errors:** Errors that occur during the computer’s read through of the code. Compilation errors in writing programs are often similar to grammatical errors in writing essays.
  - *syntax errors*: code that doesn't work with the current programming language.
  - *name errors*: code that tries to use something that doesn't exist.
  - *type errors*: code that matches different types together, which doesn't make sense. Depending on the language, some of these might turn up as runtime errors instead.
- **Runtime errors:** Errors that arise when trying to *actually execute* the code. Languages that don't have compilation will only have runtime errors. Even languages that do require compilation can have runtime errors because we can't anticipate every error just by looking at the code.
  - *Divide by zero errors*: code that divides a value by zero.
  - *Null errors*: code that refers to some variable that has no value.
  - *Memory errors*: code that surpasses your computer's memory.

### Types of errors in Python
#### NameError
An error usually occurs when you use a variable name that doesn't yet exist. When you encounter these, *check first for misspellings*; you very likely might have misspelled a variable name, causing the computer to see it as a completely different variable! If that doesn't work, try to *find where you first defined the variable*.

#### TypeError
An error occurs when we try to perform an operation on an object that doesn't make sense with the operation, like calculating the length of a number or printing an omelet.
> The function cannot deal with the object.

#### AttributeError
An error occurs when we ask for information *about* a variable that doesn't make sense, like the happiness of a potato or the GPA of a turnip.
> The object does not have the attribute.

#### SyntaxError
An error occurs when the line of code we've written can't be read by the computer because it doesn't match the computer's expectation for the programming language's grammar.

> Usually, unclosed parentheses will cause a SyntaxError on the **next** line of *code*. But depending on your code, unclosed parentheses can actually manifest as other kinds of errors. For example, if it was actually the _last_ line that had a missing close-parentheses, you would still get a syntax error, but it would read "**unexpected EOF while parsing**". EOF stands for "end of file" and "parsing" is a fancy word for "reading", so "unexpected EOF while parsing" means that Python encountered the end of the file before it expected to. So, **when you get an error on a line that looks okay, learn to quickly check for unclosed parentheses on the line of *code* before**.

#### Others
Check the [debugging guide](https://www.cc.gatech.edu/classes/AY2016/cs1301_spring/CS-1301-Debugging-Guide/index.html).

### Basic debugging
- **Print Debugging:** A form of debugging where print statements are added *throughout the code* to check how the program is flowing.
- **Scope Debugging:** A form of debugging where print statements are added to check the status of the *variables in the program at different stages* to see how they are changing. (Debugging *small sections/scopes* of a program to make sure things have run correctly so far.)
- **Rubber Duck Debugging:** A form of debugging where the programmer explains the logic, goals, and operations to an inanimate listener to methodically step through the code. The point is when faced with a hard-to-solve problem, try explaining it from scratch. Oftentimes, you'll find the solution.

> Rubber duck debugging was introduced by the 1999 book *The Pragmatic Programmer*, and it refers to a programmer who carried around a rubber duck to which to explain problems. By explaining things to the duck, the programmer often found the solution.

### Advanced debugging
- **Step by step execution**: run your code one line at a time.
- **Variable visualization**: you can view the status of every variable at any time.
- **In-line debugging**: while you're writing code, it'll show you right there if you've done something wrong; visualized very similarly to spell check. It's almost as if the computer is constantly compiling your code, just to make sure it works, while you're writing it.
 
 # Unit 2
## Chapter 2.1: Procedural Programming
### Function and Method
  - **Function**: A segment of code that performs a specific task, sometimes taking some input and sometimes returning some output.
  - **Method**: A function that is *part of a class* in object-oriented programming (but colloquially, often used interchangeably with function).
### Programming paradigms
  - **Procedural Programming:** where procedural code is the one that directly instructs a device on how to finish a task in logical steps.
  - **Object-Oriented Programming:** A programming paradigm where programmers define custom data types that have custom methods embedded within them. A concept or an abstraction is created before executing some other commands.
  - **Event-Driven Programming:** A type of programming where the program generally awaits and reacts to events rather than running code linearly.
### Operators
- **Operators:** Specific, simple functions that act on primitive data types, like integers and strings.
- **Mathematical Operators:** Operators that perform mathematical functions, like adding numbers together or assigning values to variables. (+ - \* / % \**)
- **Logical Operators:** Operators that perform logical operations, such as comparing relative values, checking equality, checking set membership, or evaluating combinations of other logical operators.
![enter description here](./images/1634711801315.png)

Typically, operators work on the most primitive types in programming languages: mathematical operators work on integers and floats, while logical operators work on booleans.

Some languages, though, allow us to use operators in creative ways. In Python, we can use the mathematical plus (+) operator to concatenate strings (put two strings together), and the multiplication (\*) operator to multiply a string by an integer to duplicate it. We can also use subtraction with dates to find the time between different dates.

### Comments and Documentation
- **Comments:** Notes from the programmer supplied in-line alongside the code itself, designated in a way that prevents the computer from reading or attempting to execute them as code. [in-line comments (pound/hash mark #) & block comments]
  
> There exist ways of writing comments that can be pulled out to generate separate, standalone documentation.

- **Documentation:** Collected and set-aside descriptions and instructions for a body of code.
- **Self-Documenting Code:** Code whose variables and functions are named in a way that makes it clear what their underlying content and operations clear to the reader.
![enter description here](./images/1634713784532.png)
> [Supplemental material](https://en.wikibooks.org/wiki/Python_Programming/Source_Documentation_and_Comments)

## Chapter 2.2: Variables
### Basic concepts
- **Variables:** Alphanumeric (letters and numbers) identifiers that hold values, like integers, strings of characters, and dates.
- **Value:** The content of some variable. The variable my_age might hold the value 21. The variable your_name might hold the value “Greymane”.
- **Null:** The “value” a variable has when it doesn’t actually have a value.
- **Naming rules:** 
  1. Variables (as well as functions, methods, classes, and other stuff we'll learn about later) cannot have spaces in them. Variable names can ==only contain letters, numbers, and underscores==.
  2. Variable names must ==start with letters==. Technically underscores are also allowed, but we generally only use those in certain situations.
  3. Variable names must not duplicate certain ==reserved words==.
  4. Names are case sensitive.
  5. A good name is ==self-documenting==.

> [See more on this website.](https://thehelloworldprogram.com/python/python-variable-assignment-statements-rules-conventions-naming/)

    Two common conventions are used if the name has more than one word: camel case and underscores. Each programming language has its own accepted style. **In Python, you should use underscores. In Java and C#, you would use camel case**. Other languages have their own conventions.
  - **Camel case** mushes the words together and capitalizes each word, like this: thisIsMyVariableName. Note that *the first letter of a variable's name is usually in lowercase, while the first letter of a function's name is often in uppercase*.
  - **Underscores** just replaces spaces with underscores, usually keeping the variable name in all-lowercase, like: this_is_my_variable_name.

### Data types
Integer, real number, character, string, boolean...self-defined types...

> [See more on this website.](https://en.wikibooks.org/wiki/Python_Programming/Data_Types)

*In **strongly-typed languages**, assigning a type to a variable is actually a separate step from assigning a value to the variable; and assigning a different type to this variable will cause crashing.*

We can multiply a sequence (string, list...) by an integer, and Python just takes that sequence and repeats it however many times we multiplied it by. But we can't multiply a sequence by a float or a string by a string. Also, when Python is asked to use a boolean like a number (such as multiplying by a boolean), it interprets True as 1 and False as 0.

Now, let's meet a weird guy in Python—the **NoneType**—which only has one value: **None**. None is Python's implementation of the programming concept of [==null==](https://en.wikipedia.org/wiki/Null_pointer) (like the null pointer in C++). This is how Python represents that a variable has no value. This is slightly different from a variable simply not existing: ==the variable name exists, it just doesn't point to any value==. Because there is no value, it also doesn't fit into any of the above types.

**Where Does None Come From?** First, the trivial way, we could just do that intentionally. The way it will happen more commonly is that you'll set it equal to some operation that doesn't result in anything, like you put on the right of an equal sign a function that has no return value (eg. the print() function)

### Type conversion
To treat a certain type of data with operations, functions, or methods of a different data type, we have to use functions for converting between the two. 

> **Implicit conversion:** In practice, you may not always need to do this manually, though. For example, when you put a value other than a string into Python's print function, it automatically tries to convert it to a string.

When we use **comma instead of plus sign**, it tells the print statement to interpret each individual thing in the parentheses as a *separate piece of data*. The print statement ==implicitly converts each thing to a string if needed and then puts them together==. **By default, it puts each thing together separated by a space**.

You'll receive a ==ValueError== whenever you try to do a type conversion, like float or integer, on a value that can't actually be converted to that type.

- ==int(variable)==: Takes as input some variable (usually a string) and attempts to convert it to an integer, returning the integer if successful or raising a ValueError if unsuccessful. This function will work if the variable is a string made up **only of digits and, optionally, the negative sign**. Note that conversion from float to int by `int()` just wiping out the decimal part. If you want to convert float to int type value in Python with a round figure. You have to use the `round()` function of Python inside the `int()` function.

- ==bool(variable)==: Takes as input some variable (usually a string) and attempts to convert it to a boolean, returning the boolean value if successful or raising a ValueError if unsuccessful. **Generally, this function returns False if the variable is 0 or an empty string, True if the variable is anything else**.

- ==float(variable)==: Takes as input some variable (usually a string/integer) and attempts to convert it to a float, returning the float if successful or raising a ValueError if unsuccessful. This function will work if the variable is a string made up **only of digits and, optionally, a negative sign and a decimal point**.

The computer interprets anything that the user enters by the ==input(variable)== function as **a string** of characters because it has no way of knowing that it's a number. So, type conversion is needed under certain circumstances. Usually, `int(input(variable))` is used if we want to use the user input as a number.

### Reserved keywords in Python

``` python 
import keyword
print(keyword.kwlist)
```
- Importing Libraries. ==import, from==. 
- Logical Operators. ==and, is, not, or, False, True, None==.
- Control Structures. ==as, break, continue, if, elif, else, for, in, while, pass, with==.
- Functions. ==def, return==.
- Object-Oriented Programming Syntax. ==class==.
- Error Handling. ==except, finally, raise, try==.
- The remaining words: ==assert, del, global, lambda, non-local, yield== are outside of the scope of the course.

If a reserved word is used as a variable name or a function name, a **SyntaxError** will be triggered. But if a function name in Python like print is used for a new variable name, assigning value to this variable will not cause any problem, but we've hidden the fact that it can also be used as a function. It can only mean one thing for a given block of code, and we're changing its meaning. When we try to use the word as a function name, a **TypeError** will arise.

## Chapter 2.3: Logical Operators
### Relational Operators
Check the relationships between multiple variables.
#### Numeric Comparison Operators
Operators that facilitate numeric comparison between values. Typically, these are 'greater than' (>), 'greater than or equal to' (>=), 'equal to' (\==), 'less than' (<), and 'less than or equal to' (<=).

These operators can sometimes be used for comparisons that are not numeric, but that nonetheless **have an underlying order**:

*   A string of characters is 'less' than another string if it **comes earlier alphabetically**. "Apple" would be *less* than "Banana". "Z" would be *less* than "a". “12” would be *less* than "3". "Quick" < "Quicker", "Quicker" < "Quickly"
*   A date is 'less' than another date if it **comes earlier in time**. January 1st, 2017 would be 'less' than January 15th, 2017.

It's also worth noting that the greater than and less than operators do work for strings as well, and they operate based on **sorting the strings alphabetically**. Besides, in Python, **all capital letters are sorted before all lowercase letters**, so a string beginning with a capital Z would be treated as less than a string beginning with a lowercase a.

#### Non-Numeric Equality Comparisons
Nearly any kind of data can compare for equality, even if it isn't numeric. We can't ask if an apple is greater than an orange, but we can ask if apples and oranges are 'equal', or the same thing.

In practice, sometimes this will compare values to see if the values of two variables are the same, and other times it will compare if two variables are pointing to the same data in memory. It could be that two variables have the same values, but those values are stored in separate places, and so the computer doesn't recognize them as equal. 

#### Set Operators
Check to see if a value is a member of a set of multiple values. Most often this comes up in strings and lists.

With strings, we can check to see if a certain smaller string occurs inside a larger string. For example, "cde" is in the string "abcdefg", but "ijk" is not.

With lists, we can check to see if a certain item is on our list. For example, if we had a list containing "grapes", "apples", and "oranges", then "apples" would be in that set, but "papaya" would not.

#### Relational Operators in Python
In many of these examples, we'll have a logical expression, and we'll set the result of it equal to a variable. Then, we can check the variable to see what the result of the expression was. We may also print the results of a logical expression directly.

Note that a single equal sign (=) is for assignment, while a double equal sign (\==) is for comparison.

The ==in== operator checks to see if something is contained within a list of other things. For one example, we can use the in operator in the context of strings to see if a certain smaller string is contained within a larger string. Note, the empty string ==""== is in all the strings.

### Boolean Operators
Operators like “and” and “or” that act on pairs of boolean (true or false) values, or that act on single boolean values, like “not”. They check the combination of multiple relational operators.

- **==And==:** An operator that acts on **two boolean** (true or false) values and evaluates to “true” **if and only if both are true**.
- **==Or==:** An operator that acts on **two boolean** (true or false) values and evaluates to “true” **if and only if at least one is true**.
- **==Not==:** An operator that acts on **one boolean** (true or false) value and **evaluates to the opposite value** (false becomes true, true becomes false).
 
Priority sequence: parentheses > mathematical operators > not > and > or
>Refer to [Operator precedence](https://docs.python.org/3/reference/expressions.html#operator-precedence)

### Truth Tables
Tables that map out the results of a statement in boolean logic (that is, using boolean operators) depending on the values of the individual variables.
![enter description here](./images/1634803606129.png)

Properties of Boolean Operators: 
- First, Boolean operators are **commutative**. What that means is it doesn't matter what order they come in. ==A and B=B and A==
- Logical expressions or logical operators are also **distributive**. ==A and (B or C)=(A and B) or (A and C)==
- ==De Morgan's Law #03A9F4==: ==not (A and B)=not A or not B==; ==not (A or B)=not A and not B==.

### Extra materials
> [Python Boolean Logic: Not As Scary As It Sounds](http://www.thehelloworldprogram.com/python/python-boolean-logic-not-as-scary-as-it-sounds/)

## Chapter 2.4: Mathematical Operators
### Basics
Operators that mimic basic mathematical functions: 
Addition `+`
Subtraction `-`
Multiplication `*`
Division `/`
Modulus `%`
Assignment Operator `=`

Note that in Python, **division in Python will automatically convert integers into a float/decimal number**. The reason for that is that whenever we do addition, subtraction, or multiplication on integers, we're guaranteed to end up with an integer. However when we do division, we might end up with a decimal number. And it's probably worth noting that this actually sets Python apart from other languages as well. Some other languages will **automatically round down** when you round integers. **But if there is a float anywhere in a mathematical expression, Python automatically converts the other type to a float, and the result will also be a float.** Eg. the result of `1.5//2` is `0.0`.

Besides, the Modulus Operation will only return the remainder having the same sign as the divisor. Eg. the result of `-8%3` is 1, the result of `8%-3` is -1, and the result of `-8%-3` is -2.

Python specifically supplies two additional operators:
- **Floor division**, represented by a double-slash (`\\`), which is division that **rounds down** to the next lowest integer (not round towards 0). For example, 5 // 2 would be 2, because 5 divided by 2 is 2.5, which is rounded down to the nearest integer, 2.
- **Exponentiation**, represented by a double-asterisk (`**`), which raises the first number to the second number. For example, 5 ** 2 would be 25, because 5 raised to the 2nd power is 25.

### Self-Assignment and Incrementing
- **Self-Assignment** means assigning a variable to a value that is in part determined by the variable itself.
- **Increment:** Repeatedly adding a constant, typically one, to a variable.
> Self-assignment reveals something very important about the assignment operator: Python (and most other programming languages) will **evaluate everything on the right side of the assignment before attempting to assign the result to the variable on the left**. That's why self-assignment works: Python initially replaces the variables with their values, so by the time we assign a new value to a variable, Python doesn't remember that the variable receiving a new value was used in the calculation.

- **Self-Assignment Shortcuts:** `+=`, `-=`, `*=`, `**=`, `/=`, `//=`, `%=`<br>Sometimes these shortcuts even work for those strange non-mathematical applications of these mathematical operators. For example, we can use the shortcut `+=` to add something to an existing string.

### Extra materials
> [Python Operators are Mathematical!](https://thehelloworldprogram.com/python/python-operators/)

## Appendix 1. Python Translation Guide
### Print Statements and Line-Ending Behaviors
<style>
table th:first-of-type {
    width: 10%;
}
table th:nth-of-type(2) {
    width: 40%;
}
table th:nth-of-type(3) {
    width: 50%;
}
</style>

| **Language** | **Syntax** | **Notes** |
| --- | ----- | --- |
| Python | print("Here's a line of code")<br>print("Here's another one!") | By default, print() adds a line break to the end of the printed text. |
| Java | System.out.println("Here's a line of code");<br>System.out.println("Here's another one!"); | Like Python's print(), Java's System.out.println() adds a line break after the printed text. In contrast, System.out.print() will print some text without creating a new line afterward. |
| C | printf("Here's a line of code");<br>printf("Here's another one!"); | In C, the printf() function does not add a line break after the printed text. To do that, you need to include "\n" inside the printed text itself, e.g. printf("New line please!\n"). |
| C++ | std::cout << "Here's a line of code";<br>std::cout << "Here's another one!"; | Like C, C++'s cout will not add a new line after the printed text. To add one, we would need to write std:cout << "New Line please!\n". |
| C# | Console.WriteLine("Here's a line of code");<br>Console.WriteLine("Here's another one!"); | C#'s Console.WriteLine() function add a line break after the printed text. Like Java, C# also has a Console.Write() function that will write without starting a new line afterward. |
| JavaScript | console.log("Here's a line of code")<br>console.log("Here's another one!") | By default, console.log() adds a line break to the end of the printed text. |
| VB.NET | Console.WriteLine("Here's a line of code")<br>Console.WriteLine("Here's another one!") | C# and VB.NET use the same underlying library, so you'll find that oftentimes syntax like Console.WriteLine is shared between them. |
| Matlab | fprintf("Here's a line of code);<br>fprintf("Here's another one!"); | Like C, Matlab's fprintf will not add a new line after the printed text. To add one, we would need to write fprintf("New Line please!\n"). |
| Swift | print("Here's a line of code")<br>print("Here's another one!") | By default, print() adds a line break to the end of the printed text. |
| Ruby |  puts "Here's a line of code"<br>puts "Here's another one!" | By default, puts adds a line break to the end of the printed text. |

*Scripting languages* (Python, JavaScript) **generally** *do not use a semi-colon to mark the ends of lines*. **Most** *compiled languages* (Java, C, C++, C#) *use semi-colons*. There are exceptions, though; Swift and VB.NET are compiled languages that do not use semi-colons, while MatLab is a scripting language that does.

### Comment Syntax
Python's comment syntax is in the minority.

| **Language** | **Syntax** | **Notes** |
| --- | --- | --- |
| Python | #This is a comment in Python<br><br>#This is a<br>#multiline comment<br>#in Python | Triple quotes can also be used in Python to create multi-line comments. |
| Java | //This is a comment in Java<br><br>/* <br> \* This is a<br> \* multi-line comment<br> \* in Java<br> */ | The asterisks at the beginning of each line inside the multi-line comment are customary, but not required. Java, C++, JavaScript, and C# use the same syntax. |
| C | /* This is a comment in C*/ <br><br> /\*  This is a<br> * multiline comment<br> * comment in C<br> */ | The asterisks at the beginning of each line inside the multi-line comment are customary, but not required. C does not have a dedicated single-line comment syntax. |
| C++ | //This is a comment in C++<br><br>/*<br> * This is a<br> * multi-line comment<br> * in C++<br> */ | The asterisks at the beginning of each line inside the multi-line comment are customary, but not required. Java, C++, JavaScript, and C# use the same syntax. |
| C# | //This is a comment in C#<br><br>/*<br> * This is a<br> * multi-line comment<br> * in C#<br> */ | The asterisks at the beginning of each line inside the multi-line comment are customary, but not required. Java, C++, JavaScript, and C# use the same syntax. |
| JavaScript | //This is a comment in JavaScript<br><br>/* <br> * This is a<br> * multi-line comment<br> * in JavaScript<br> */  | The asterisks at the beginning of each line inside the multi-line comment are customary, but not required. Java, C++, JavaScript, and C# use the same syntax. |
| VB.NET | 'This is a comment in VB.NET<br><br>'This is a<br>'multiline comment<br>'in VB.NET | VB.NET has no special way of creating multi-line comments. |
| Matlab | %This is a comment in Matlab<br><br>%{<br>This is a<br>multiline comment<br>in Matlab<br>%} |  |
| Swift | //This is a comment in Swift<br><br>/* <br> This is a<br> multi-line comment<br> in Swift<br>*/ | 
| Ruby| # This is a comment in Ruby<br><br>=begin<br>This is a<br>multiline comment<br>in Ruby<br>=end | Ruby is weird. |

### Variable Declarations and Assignments
Note that in Python, we create a variable by assigning it an initial value. In other languages, it's possible to create a variable without assigning it any value.

| **Language** | **Syntax** | **Notes** |
| --- | --- | --- |
| Python | my_int = 5<br>my_str = "Hello world!" | Python prefers snake_case for variable style. |
| Java | int myVar = 5;<br>string myStr = "Hello world!"; | The first item in the variable declaration line (`int, string`, etc.) is the data type. The variable cannot change types once declared to be a certain type. Java prefers camelCase for variable names. |
| C, C++, C# | int myVar = 5;<br>string myStr = "Hello world!"; | The first item in the variable declaration line (`int, string`, etc.) is the data type. The variable cannot change types once declared to be a certain type. C prefers camelCase for variable names. |
| JavaScript | var myVar = 5;<br>var myStr = "Hello world!"; | `var` is used whenever creating a new variable, but it does not represent a type. JavaScript prefers camelCase for variable names. |
| VB.NET | Dim MyVar As Integer = 5<br>Dim MyStr As String = "Hello world!" | types (`As Integer, As String`) are optional but recommended in VB.NET. VB.NET prefers camelCase for variable names, but **often capitalizes the first letter**, too (e.g. `MyVar` instead of `myVar`). |
| Matlab | my_var = 5<br>my_str = "Hello world!" | Matlab has few consistent variable name styles. |
| Swift | var myVar = 5<br>var myStr = "Hello world!" | Swift prefers camelCase for variable names. |
| Ruby | my_var = 5<br>my_str = "Hello world!" | Ruby prefers snake_case for variable names. |

Many languages (Java, C/C++/C#, VB.NET) are statically typed, meaning that once when you create a variable, you have to decide what its type will be. Afterward, it can never take a different type. Other languages (Python, Swift, Ruby, JavaScript) are dynamically typed, meaning that a variable's type comes from its value. If you change its value, the variable's type can change.

### Operators
The rules of logic are generally the same across all programming languages. Python's [operator precedence](http://www.mathcs.emory.edu/~valerie/courses/fall10/155/resources/op_precedence.html) is relatively universal, although there can be slight differences (for example, not all languages have slicing, subscription, or lambda expressions). The syntax used for various operators, however, can differ.

#### Relational Operators
Most relational operators are the same in all languages. These are the same in Python, Java, C, C++, C#, JavaScript, VB.NET, Matlab, Swift, and Ruby:

*   a < b: Less than
*   a <= b: Less than or equal to
*   a == b: Equal to
*   a >= b: Greater than or equal to
*   a > b: Greater than

If a and b are not the same type, JavaScript will automatically try to convert them to the same type before comparison. To avoid this conversion, you'd use `===`.

The languages differ a little bit more with the 'not equal to' operator:

| **Language** | **Syntax** | **Notes** |
| --- | --- | --- |
| Python, Java, C, C++, C# | a `!=` b  |  |
| JavaScript | a `!=` b  | If a and b are not the same type, JavaScript will automatically try to convert them to the same type before comparison. To avoid this conversion, you'd use `!==`. |
| VB.NET | a `<>` b | Technically, the `<>` operator works in most other languages as well for *not equal to*, but `!=` is more common. |
| Matlab | a `~=` b |  |

#### Boolean Operators
The three boolean operators--and, or, not--are generally represented in one of three ways: with symbols, with double-symbols, or with plaintext words. Different languages also use slightly different capitalizations for booleans, so we'll use the language-appropriate ones here, too.

| **Language** | **Syntax** | **Notes** |
| --- | --- | --- |
| Python | True `and` False  #And<br>True `or` False   #Or<br>`not` True        #Not | You can also use `&` (for and) and `|` (for or) in Python, but they technically do something slightly different. They perform **bitwise operations**. |
| Java | true `&&` false   #And<br>true `||` false     #Or<br>`!`true           #Not<br>true `^` false    #Exclusive-Or | You can also use single-operators (`&` or `|` instead of `&&` or `||`), but **it's generally better to use double operators**. Double operators only evaluate later conditions if they might change the end result. Java also offers an **exclusive-or** operator `^`, which is True if exactly *one of the two conditions is True, not both or neither*. |
| C | 1 `&&` 0   #And<br>1 `||` 0     #Or<br>`!`1       #Not | C does not natively have boolean types: it treats 0 as False and 1 (or any non-zero number) as True. |
| C++, C# | true `&&` false   #And<br>true `||` false   #Or<br>`!`true           #Not | C++ and C# are the same as C, but includes true boolean types like Java. |
| JavaScript | true `&&` false   #And<br>true `||` false   #Or<br>`!`true           #Not |  |
| VB.NET | True `And` False  #And<br>True `Or` False   #Or<br>`Not` True        #Not<br>True `Xor` False  #Exclusive-Or | Following its style, VB.NET **capitalizes** both the boolean values and the logical operators. It also offers an **exclusive-or** operator. It also includes two additional operators, **AndAlso** and **OrElse**, which function like `&&` and `||` in Java.|
| Matlab | true `&` false  #And<br>true `|` false   #Or<br>`~`true        #Not<br>true `xor` false  #Exclusive-Or | Matlab also offers an **exclusive-or** operator. |
| Swift | true `&&` false   #And<br>true `||` false   #Or<br>`!`true           #Not |  |
| Ruby | true `and` false  #And<br>true `&&` false   #Also And<br>true `or` false   #Or<br>true `||` false   #Also Or<br>`not` true        #Not<br>`!`true           #Also Not | Ruby lets you use either symbols or words. |

#### Mathematical Operators
Most languages share the same mathematical operators: it's hard to get away from plus for addition, minus for subtraction, etc. There are some unique ones, though: floor division, modulus, and exponentiation may differ by language.

| **Language** | **Syntax** | **Notes** |
| --- | --- | --- |
| Python | a // b  #Floor Division<br>a ** b  #Exponentiation, a to the b<br>a % b   #Modulus |  |
| Java | a / b   //See notes<br>a % b   //Modulus | Java has no floor division operator, but it does not automatically convert to floating point numbers either. If you divide two integers, it will round down like floor division. If either number is a decimal number, the result will be the real quotient. Java has no exponent operator: instead it would use Math.pow(a, b). |
| C, C++, C# | a / b   /* See notes \*/<br>a % b   /* Modulus \*/ | C's (and its derivatives') floor division works like Java's: if the numbers are integers, it will perform floor division, but if not, it will return a decimal number. C has no exponent operator, and instead uses separate functions. |
| JavaScript | a % b   //Modulus | JavaScript has neither a floor division operator nor an exponent operator. It uses separate functions for both. |
| VB.NET | a \ b   'Floor division<br>a ^ b   'Exponentiation, a to the b<br>a mod b 'Modulus | VB.NET's operator for modulus is just the keyword mod. |
| Matlab | a .^ b  %Exponentiation, a to the b | Matlab has no dedicated operators for floor division and modulus; it uses functions instead. |
| Swift | a % b   ///Modulus | Swift has no dedicated exponentiation or floor division operator; it uses functions instead. |
| Ruby | a / b   #See notes<br>a ** b  #Exponentiation, a to the b<br>a % b   #Modulus | Ruby's division operator works like C and Java: if the numbers are integers it performs floor division, otherwise it performs regular division. |

Most languages support self-assignment like in Python: a += 5, for example, will work in almost every language listed here. Some languages, like C++ and Java, also have a shorthand or adding or subtracting one: a++ will add one to a (same as a += 1), and a-- will subtract one from a (same as a -= 1).
