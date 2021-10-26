# Gatech CS1301xII



> "Always code as if whoever ends up maintaining your code will be a violent psychopath who knows where you live." -Martin Golding

😂😂😂😂😂😂😂😂😂😂😂😂
Fine.
# Unit 3
## Chapter 3.1: Basics of Control Structures
- **Control Structures:** Statements that control the flow of execution of the program. Or, more simply, lines of code that control when other lines of code run. They allow us to loop over certain lines of code multiple times, changing the data that they act on each time.
  - **Conditional Statements:** Programming statements that control what code is executed based on certain conditions; usually of the form “if”, “else if”, and “else”.
  - **Loop:** A programming control structure that executes a segment of code multiple times.
  - **Function:** A segment of code that performs a specific task, sometimes taking some input and sometimes returning some output. (Eg. purchasing something is a common behavior regardless of what you're buying. The steps are always the same: get the total, swipe or insert your card, enter your PIN, sign your name, and remove the card. So, we can imagine grouping those actions together into a common function to use.)
  - **Exception:** An error that a program might want to anticipate and catch instead of outright avoiding.
  - **Exception Handling:** A control structure that catches certain anticipated errors and reacts to them accordingly.

> **Condition vs. Exception**: Conditionals are most often decisions when the computer has access to all the necessary information. The condition is intentionally checked. Exception handling also feels like a decision, but typically exception handling occurs when we didn't check some piece of information beforehand. (Eg. we don't usually check for an insufficient balance, but it could occur.)

- **Indentation:** Spaces at the beginning of a line that are used to group together blocks of code. All consecutive lines of code at the same level of indentation are in a single code block.
- **Scope:** The portion of a program’s execution during which a variable can be seen and accessed. Similar to a computer's short-term memory. 
  - A single variable usually **lives within the control structures definition**. And once the computer leaves that control structure, the variable is lost. So the code that runs after the conditional can't see any variables that were created inside of it. The reason is that the computer can't guarantee that the contents of a conditional statement actually ran.
   > 🧐 Note that in Python, a variable created in a control structure lives since the line it is created (and run) to the end of the code, which is a bit wierd though. 🤔 In other languages like Java, for example, if you define a variable inside a conditional, then the variable ceases to exist when the condition is done. 😓  
   > 🤓So, it's better to never create variables inside a conditional that will need to be accessed outside the conditional.
  - Functions define scope even more narrowly. A function scope is generally just a variable sent to it or created within it. Functions don't automatically see anything created before their run. They only see those things that are sent into them intentionally.
 
## Chapter 3.2: Conditionals
- **Conditional Statements:** Programming statements that control what code is executed based on certain conditions; usually of the form “if”, “else if”, and “else”.
- **If-Then Statement:** A conditional control structure that runs a block of code only if a certain condition is true. `if`
- **Else Statement:** A conditional control structure that runs a block of code if all preceding if-then and else-if statements have been false. `else`
- **Else-If Statement:** A conditional control structure that runs a block of code if all preceding if-then and else-if statements have been false and some other conditions are met. `elif`
- **Nested Conditional:** A conditional statement that is itself controlled by another conditional statement. More simply, an if-then statement within another if-then statement.

## Chapter 3.3: Loops
- **For Loop:** A loop control structure that runs a block of code a **predetermined** number of times. For loops run with some advanced knowledge about how many times the loop will run. However, this number can be a variable (eg. a user input), just make sure that it is defined before the for loop.
- **For-Each Loop:** A loop control structure that runs a block of code a predetermined number of times, where the number of times comes from the length of some list and the items in the list are automatically loaded into a variable for usage in the block of code.
- **Iterate:** To repeat code a number of times.
- **Iteration:**  A single execution of a repeated task or block of code.
- **While Loop:** A loop control structure that runs a block of code until a certain logical expression is not satisfied. They run while something remains true. 
 > **Anything we can express in a for loop can also be expressed in a while loop. But not all loops are interchangeable.** For loops must have some pre-knowledge about the number of times it should run.
 
  > Some languages also have a special kind of while loop called a do while loop. We can think of the standard while loop that we talked about before as a while do loop--while a condition is true, do something. A do while loop is identical except that it guarantees the something will be run at least once. It does it before checking the condition the first time.

### For Loops
- **Loop Control Variable**: A variable whose value is the number of times a loop has run. It is used to check if the loop should keep running (e.g. if it has run as many times as it’s supposed to). **We actually can't change the variable within the loop**. Nothing we do to that variable inside the body of this loop will be carried over to the next time that loop runs. No matter what has been done with the variable within the body of the loop, it will take the next value in the list.
  
Actually, in Python, every for loop is a for-each loop. It runs the indented code for each item in the list given. In a for loop, `range()` is used so that you know exactly how many iterations have occured, but you have to manually look up each item by its index. In a for-each loop, a pre-defined list is used, you iterate directly over the items, but you have to use other ways to get the index `(list.index(value))`.

> 📕When we're just printing, we'll sometimes just use **commas** instead, and then we don't have to worry about actually converting an integer into a string. But `input` is a different function. It's not the `print` function, and it doesn't know how to put together variables the same way as our `print` function does. So, here, if we want to use a variable that holds an integer in the prompt that we give to our user, we have to **explicitly convert it to a string**.

### While Loops
While loops are good for code where we don't know how many times we need to repeat in advance.

Infinite loop--a loop that, because of the way it's designed, never stops running. Useful for game design. For loops cannot be infinite loops (even we use 'Infinite' to create a range, because 'Infinite' is just a large constant).

Although we can't do a do-while loop in Python, we can create our initial variables and assign values to our variables such that it guarantees the while loop will run at least once.

### Advanced Loop Keywords
- `continue`: Skip the rest of the current iteration of the loop and **continue** with the next iteration of the loop (if there is a next iteration). If this for loop was actually nested-- if it was inside of another for loop-- continue will correspond to the closest for loop.
- `break`: Skip the rest of the current iteration of the loop and **break** out of the loop altogether, skipping any later iterations, too. Break forces execution to skip to the next line of code **after** this loop.
- `pass`: **Pass is just like Python's way of leaving a blank indented line**. It breaks the requirement that control structures must have code within them and **skip the body of the control structure**. 
> Pass exists because there will be certain rare times when we need to use a control structure, but we don't want to do anything inside of it. One example might be-- imagine we know we're going to want to loop somewhere, but we haven't implemented its contents yet. We want to leave the loop there for now, but we don't want to bother with the interior of it. We could use pass just to skip over the inside of that loop for now until we come back to implement it.

### Extra materials
> 🐍[Beginning Python Programming for Aspiring Web Developers](http://www.openbookproject.net/books/bpp4awd/ch04.html)
> 🐍[Hands-on Python 3 Tutorial](http://anh.cs.luc.edu/python/hands-on/3.1/handsonHtml/index.html)
## Chapter 3.4: Functions
- **Function Call**: A place where a function is actually used in some code.
- **Function Definition:** A segment of code that creates a function, including its name, parameters, and code, to be used by other portions of a program.
- **Function Header:** The name and list of parameters a function expects, provided as reference to the rest of the program to use when calling the function.
- **Function Body:** The code that a function runs when called.
- **Return Statement:** The line of code that defines what output will be sent back at the end of a function.
  > Not all functions and all languages have return statements. Some might not need to return in the output of the main program. Similarly, not all functions require any input.
- **Parameter:** A variable for which a function expects to receive a value when called, whose scope is the function’s own execution.
- **Arguments:** Values passed into parameters during a function call. Essentially, these are the values assigned to the function’s dedicated variables (i.e., parameters).
  > Parameters are like variables, and arguments are like values.

Note that when Python runs the code, it doesn't initially run the function body. **The header of the function definition loads into the computer's memory the knowledge that there exists a function defined on that line.** The body of the function isn't run until it's called from somewhere else in the code. And at that time execution will jump to the begining line of the function body.

> 🤖Define a function: Hey, there exists a function called ××××. Just keep that in mind for now.
> 🤖Call a function: Hey, remember the function that I told you about earlier? Go ahead and run it now.

The scope of a function is from the line where it's defined to the end of the code. If we tried to call it before it was defined, it's out of scope and we'd receive an error because it hasn't yet been defined. This is a little bit different from compiled languages.

## Appendix 1. Python Translation Guide
<style>
table th:first-of-type {
    width: 10%;
}
table th:nth-of-type(2) {
    width: 45%;
}
table th:nth-of-type(3) {
    width: 45%;
}
</style>

### Indicating Control Structures
Python is actually considered somewhat odd in its formal use of indentation to indicate control structures. Most language indent by convention, but have more formal mechanisms to indicate the scope of a control structure.

Most languages use brackets `{ }` to indicate the scope of a control structure. The lines inside the control structure are typically indented for readability, but it would be possible to remove all indentation and still have working code in these languages.

| **Language** | **Syntax** | **Notes** |
| --- | --- | --- |
| Python | if True:<br>    #Some code would go here!<br>#The control structure is over when the indentation ends. |  |
| Java, C, C++, C#, JavaScript, Swift | if (true) { /* An open bracket starts the control structure. \*/<br>    /* Some code would go here! \*/<br>} /* A close bracket ends the control structure. \*/ | You will find [vicious arguments](http://i.imgur.com/NQ6jItG.jpg) online over whether the open bracket should go alongside the control structure or on the next line. Personally, I prefer the same-line structure. |
| VB.NET | If True Then<br>    'Some code would go here!<br>End If 'The VB.NET keyword End If ends the control structure | VB.NET does not require an additional character or keyword to start a control structure, but does require one to end a structure. It infers the control structure starts when it sees a control structure keyword like `If`, and then it formally declares the control structure over with something like `End If`. |
| Matlab | if true<br>    %Some code would go here!<br>end %The keyword end ends the control structure. | Like VB.NET, Matlab has a formal keyword reserved for ending control structures: `end`. |
| Ruby | if true<br>    #Some code would go here!<br>end #The keyword end ends the control structure. | Like VB.NET, Ruby has a formal keyword reserved for ending control structures: `end`. |

### If, Else If, and Else
Every major language offers the basic functionality of an if, else-if, and else. Some languages even offer a single operator that lets you do these all on one line, called a ternary operator, but we'll focus on the more general structure.

| **Language** | **Syntax** | **Notes** |
| --- | --- | --- |
| Python | if some_bool:<br>    #Some code would go here!<br>elif some_other_bool:<br>    #Some other code would go here!<br>else:<br>    #Some other code would go here! |  |
| Java, C, C++, C#, JavaScript | if (some_bool) {<br>    /* Some code would go here! \*/<br>} else if (some_other_bool) {<br>    /* Some other code would go here! \*/<br>} else {<br>    /* Some other code would go here! \*/<br>} | You'll also find lots of arguments online about whether the closing bracket should go on the same line as the else if and the else. I prefer to keep the brackets on the same line; we can always add extra blank lines if we want to for readability. Note that in these languages, the condition itself must go inside parentheses. |
| VB.NET | If some_bool Then<br>    'Some code would go here!<br>ElseIf some_other_bool Then<br>    'Some other code would go here!<br>Else<br>    'Some other code would go here!<br>End If | VB.NET capitalizes its conditional keywords (`If`, `ElseIf`, `Else`, and `End If`), and it also has an optional keyword `Then` that makes the code read a little more like natural language. It reads quite nicely if we use boolean names like `today_is_monday`. It also ends a conditional with the dedicated keyword `End` If instead of a close bracket. |
| Matlab | if some_bool<br>    %Some code would go here!<br>elseif some_other_bool<br>    %Some other code would go here!<br>else<br>    %Some other code would go here!<br>end | Like VB.NET, Matlab has a dedicated keyword to end a conditional structure: `end`. |
| Swift | if some_bool {<br>    /* Some code would go here! \*/<br>} else if some_other_bool {<br>    /* Some other code would go here! \*/<br>} else {<br>    /* Some other code would go here! \*/<br>} | Swift is identical to Java and C except that it does not require parentheses around the conditional expression. |
| Ruby | if some_bool<br>    #Some code would go here!<br>elseif some_other_bool<br>    #Some other code would go here!<br>else<br>    #Some other code would go here!<br>end | Ruby is identical to Matlab, which is weird. |
