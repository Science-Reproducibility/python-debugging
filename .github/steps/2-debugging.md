<!--
  <<< Author notes: Step 2 >>>
  Start this step by acknowledging the previous step.
  Define terms and link to docs.github.com.
  TBD-step-2-notes.
-->

# Week 2: Introduction to debugging in Python

In the second week, we will review what we learned about errors, 
and we will introduce the concept of debugging. 

## 1 :book: Review of Errors and Exceptions in Python

If you want to review last week's content and read more about the topic, I recommend:
- [GeeksforGeeks: Python Errors and Exceptions](https://www.geeksforgeeks.org/python-errors-and-exceptions/)
- [Types of error on tutorialsteacher](https://www.tutorialsteacher.com/python/error-types-in-python)

## 2 :book: What is debugging?

Debugging is the process of identifying, analyzing, and resolving issues or bugs in software 
to ensure it functions as intended. 
It is a crucial part of the software development lifecycle and involves locating the root cause 
of errors in code, fixing those errors, and verifying that the changes do not introduce new issues.

Key steps in the debugging process include:
- Identify the problem and reproduce it consistently.
- Identifying the root cause of the issue.
- Fixing the issue
- Testing the fix to ensure it resolves the problem without introducing new issues.
- Improving the code to prevent similar issues in the future.

Common debugging techniques include:
- **Print statement**
  
  Using print statements to output the values of variables and the flow of the program.

- **Debuggers**

  Using an interactive debugger to step through the code and inspect the state of variables at different points.

- **Logging**

  Implementing logging to track the state and flow of a program over time.

- **Unit tests**

  Writing unit tests to verify the behavior of individual components of the code.


## 3 :book: Python debugger `pdb`

Python provides a built-in debugger called `pdb` that allows you to interactively debug your code.
You can set breakpoints, step through code, inspect variables, and evaluate expressions to identify issues in your code.
```python
import pdb

def add(a, b):
    pdb.set_trace()
    return a + b
```
Alternatively:
```python
def add(a, b):
    breakpoint()
    return a + b
```

Once you are in the debugger, you can use commands like:

- `n` - next line
- `c` - continue execution
- `q` - quit the debugger
- `p <variable>` - print the value of a variable
- `l` - list the code around the current line
- `s` - step into a function call
- `r` - return from the current function
- `h` - get help on the available commands
- `!` - run a Python command
- `u` - move up the call stack
- `d` - move down the call stack
- `b <line>` - set a breakpoint at a specific line number
