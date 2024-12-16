<!--
  <<< Author notes: Step 1 >>>
  Choose 3-5 steps for your course.
  The first step is always the hardest, so pick something easy!
  Link to docs.github.com for further explanations.
  Encourage users to open new tabs for steps!
  TBD-step-1-notes.
-->

# Week 1: Errors in Python

Before we start with the debugging, we need to understand what are the most common errors in Python and how to read Python traceback.
This will be the subject of the first part of the course.

## 1 :book: Errors and Exception in Python

- **Syntax errors** 

  Syntax errors are the most common type of error. 
It is caused by not following the proper structure (syntax) of the language.
These errors are detected during the parsing phase before the code is executed. 
They are often caused by typos, missing parentheses, or incorrect keyword usage.
An example of a syntax error is:
  - missing parentheses:
```python
print("Hello, World!"
```
  - missing colon:
```python
if True
    print("Hello, World!")
```
  - missing quotation marks:
```python
print(Hello, World!)
```
  - missing indentation:
```python
if True:
print("Hello, World!")
```

- **Runtime errors**

  Runtime errors occur during the execution of the program.
They are also called **exceptions** because they usually indicate that something exceptional (and bad) has happened.
Examples of runtime errors are:
  - `ZeroDivisionError`:
```python
print(1/0)
```
  - `TypeError`:
```python
print("Hello, World!" + 1)
```
  - `ValueError`:
```python
print(int("Hello, World!"))
```

  - `NameError`:
```python
print(a)
```

  - `IndexError`:
```python
a = [1, 2, 3]
print(a[3])
```

  - `KeyError`:
```python
a = {"name": "John"}
print(a["age"])
```

  - `FileNotFoundError`:
```python
with open("file.txt", "r") as f:
    print(f.read())
```

  - `ImportError`:
```python
import unknown_module
```

  - `AssertionError`:
```python
assert 1 + 1 == 3, "This is an assertion error"
```

You can find a list of all built-in exceptions in Python [here](https://docs.python.org/3/library/exceptions.html).

- **Semantic errors**

  Semantic errors are the hardest to find and fix.
They occur when the code is logically correct but does not produce the expected result.
These errors are often caused by incorrect assumptions or misunderstandings of the problem.
An example of a semantic error is:
```python
def add(a, b):
    return a - b
```

In this part of the course, we will focus on the syntax and runtime errors (exceptions).

> Questions:
> - Do you know what is the main difference between syntax and runtime errors?


## 2 :book: Reading Python traceback

When an error occurs in Python, the interpreter generates an error message called a **traceback**.
The traceback provides information about the error, including the type of error, the line number where the error occurred, 
and the sequence of function calls that led to the error.
An example of a traceback is:
```
Traceback (most recent call last):
  File "/Users/dorota/teaching/pycon_debug/part2/standard_deviation.py", line 41, in <module>
    main(filename)
  File "/Users/dorota/teaching/pycon_debug/part2/standard_deviation.py", line 35, in main
    std = standard_deviation_list(data)
  File "/Users/dorota/teaching/pycon_debug/part2/standard_deviation.py", line 24, in standard_deviation_list
    mean = mean_value_list(data_list)
  File "/Users/dorota/teaching/pycon_debug/part2/standard_deviation.py", line 6, in mean_value_list
    return sum(data_list) / len(data_list)
ZeroDivisionError: division by zero
```

In this traceback, the error occurred in the `mean_value_list` function on line 6 of the `standard_deviation.py` file.
The error is a `ZeroDivisionError` caused by dividing by zero.

When reading a traceback, it is important to look for the following information:
- The type of error (e.g., `ZeroDivisionError`)
- The line number where the error occurred (e.g., line 6)
- The function or module where the error occurred (e.g., `mean_value_list` function)
- The sequence of function calls that led to the error (e.g., `mean_value_list` -> `standard_deviation_list` -> `main`)
- The file where the error occurred (e.g., `standard_deviation.py`)
- The full path to the file where the error occurred (e.g., `/Users/dorota/teaching/pycon_debug/part2/standard_deviation.py`)
- The traceback message (e.g., `division by zero`)

## 3 :eyes: :keyboard: Reading Python traceback
Now it is time for you to practice reading Python traceback.
In the directory `week1/ex1` you will find a Python script `traceback.py` that contains a deliberate errors.
Your task is to run the script and read the traceback to identify the type of error, the line number, and the function where the error occurred.
Do you know how to fix the error?


