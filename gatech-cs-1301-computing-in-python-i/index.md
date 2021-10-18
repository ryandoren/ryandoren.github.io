# Gatech CS 1301



----------


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
- **Run/Excution**: Running some code and having it actually perform its operations.
> Compiling just makes sure what we told the program to do makes sense; running checks whether the program actually do what we want it to do.

Compilation could potentially be skipped.
- Languages that require compilation are called **static/compiled**  languages.
- Languages that do not require compilation are called **dynamic/interpreted**  languages.

*Nonetheless though, even with dynamic languages, we often mimic the workflow of static languages.*

### Programming Language
Categorization of languages: 
- **Static & Dynamic**: whether compilation is required
- **Hight-level languages** involve a great deal of abstraction from the low-level details of the computer like memory, whereas **low-level languages** require these details to be addressed manually.

[Popularity of different languages](https://www.tiobe.com/tiobe-index/)

> C++ and C# are two successors to the programming language C, which is a low-level language used a lot in developing operating systems, video games, and other highly complex programs. C++ adds a few more features to C, while C# is more of a high-level version. Java, C, C++, and C# are static, compiled languages; Python is the top dynamic, scripting language on this list.

### Console vs. GUI
- Graphical user interfaces (GUIs): An output medium that uses more than just text, like forms, buttons, tabs, and more. Eg. a web brower, a word processor like Microsoft Word, a smartphone app, a modern operating system like Windows or Mac OS.
- Console: An output medium for a program to show exclusively text-based output. Eg. command line interfaces like the terminal on a Mac or the command window on a PC.

### Fundations, language, and domain 
- **Foundations** are the *core principles of computing* that transcend specific programming languages.
- These foundational principles are then *implemented* in specific **programming languages**.
- You then *apply* them to a particular **domain**.

### Python
- Python is a **high-level, platform independent** programming language. Python abstracts further away from the inner workings of the computer than lower-level languages (like memory management), thus is easier to use.
- Python is **dynamic & interpreted**, which means that Python will *run our code line by line* when we ask it to without trying to compile it first. That opens up the possibility of using Python in a command line interface where we write and run lines of code one at a time. Whereas in the **scripting mode**, we write a bunch of code, then *run it all at once*.
- The main takeaway of Python being an interpreted language is that we might not be aware of errors until we actually try to run those lines.

## Chapter 1.2: Programing
