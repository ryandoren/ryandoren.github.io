---
title: Gatech CS1301xII
author: "Ryan"              # 文章作者
description : "Intro to Computing in Python by David Joyner"    # 文章描述信息
date: 2021-10-25            # 文章编写日期
draft: false
---


> "Always code as if whoever ends up maintaining your code will be a violent psychopath who knows where you live." -Martin Golding

😂😂😂😂😂😂😂😂😂😂😂😂
Fine.
# Unit 3
## Terminology
- **Control Structures:** Statements that control the flow of execution of the program. Or, more simply, lines of code that control when other lines of code run. They allow us to loop over certain lines of code multiple times, changing the data that they act on each time.
  - **Conditional Statements:** Programming statements that control what code is executed based on certain conditions; usually of the form “if”, “else if”, and “else”.
  - **Loop:** A programming control structure that executes a segment of code multiple times.
  - **Function:** A segment of code that performs a specific task, sometimes taking some input and sometimes returning some output. (Eg. purchasing something is a common behavior regardless of what you're buying. The steps are always the same: get the total, swipe or insert your card, enter your PIN, sign your name, and remove the card. So, we can imagine grouping those actions together into a common function to use.)
  - **Exception:** An error that a program might want to anticipate and catch instead of outright avoiding.
  - **Exception Handling:** A control structure that catches certain anticipated errors and reacts to them accordingly.

> **Condition vs. Exception**: Conditionals are most often decisions when the computer has access to all the necessary information. The condition is intentionally checked. Exception handling also feels like a decision, but typically exception handling occurs when we didn't check some piece of information beforehand. (Eg. we don't usually check for an insufficient balance, but it could occur.)

- **Indentation:** Spaces at the beginning of a line that are used to group together blocks of code. All consecutive lines of code at the same level of indentation are in a single code block.
- **Scope:** The portion of a program’s execution during which a variable can be seen and accessed. Similar to a computer's short-term memory. 
  - A single variable usually lives within the control structures definition. And once the computer leaves that control structure, the variable is lost. So the code that runs after the conditional can't see any variables that were created inside of it. The reason is that the computer can't guarantee that the contents of a conditional statement actually ran.
  - Functions define scope even more narrowly. A function scope is generally just a variable sent to it or created within it. Functions don't automatically see anything created before their run. They only see those things that are sent into them intentionally.
 
## Chapter 3.1: Control Structures