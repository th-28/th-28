# <div align='center'> WWWH Protocol: My Coding Learning Journey </div>

## Introduction

Welcome to my documentation of the WWWH - What, Why, When, How protocol! It is a record of my coding journey, a catch-all for the main ideas of each concept that I meet and learn.

### What is WWWH?

WWWH is a very simple but strong framework to really understand and document a coding concept in these areas:

* **What**: Define it
* **Why**: What is its purpose?
* **When**: Describe when to use
* **How**: Describe how to implement and how the concept work 

With this protocol repeated routinely, I build up a comprehensive knowledge base that helps in remembering and also serves for quick references later on in projects.

# Intro:

## The Python Zen:
> Beautiful is better than ugly.
> Explicit is better than implicit.
> Simple is better than complex.
> Complex is better than complicated.
> Flat is better than nested.
> Sparse is better than dense.
> Readability counts.
> Special cases aren't special enough to break the rules.
> Although practicality beats purity.
> Errors should never pass silently.
> Unless explicitly silenced.
> In the face of ambiguity, refuse the temptation to guess.
> There should be one-- and preferably only one --obvious way to do it.
> Although that way may not be obvious at first unless you're Dutch.
> Now is better than never.
> Although never is often better than *right* now.
> If the implementation is hard to explain, it's a bad idea.
> If the implementation is easy to explain, it may be a good idea.
> Namespaces are one honking great idea -- let's do more of those!
> *By Tim Peters*

## Python Programing Language

### What:
Python is a **high-level**, **interpreted**, and **general-purpose** programming language. Created by Guido van Rossum in 1991, it is known for its simple, readable syntax, which emphasizes code readability and reduces the cost of program maintenance. Python supports multiple programming paradigms, including procedural, object-oriented, and functional programming (These paradigms will be discussed later).

### Why:
Python is widely used because of its:
+ **Ease of Use:** Its simple syntax makes it beginner-friendly.
+ **Versatility:** It is used in web development, data science, machine learning, automation, scientific computing, and more.
+ **Large Community and Libraries:** Python boasts a vast ecosystem of frameworks and libraries that speed up development and solve complex problems efficiently.
+ **Portability:** It is cross-platform and can run on various operating systems without modification.

### When:
Python is ideal to use:
+ When you want to prototype or develop software quickly.
+ For applications involving data analysis, machine learning, or artificial intelligence.
+ When automating repetitive tasks or managing system operations.
+ In web development with frameworks like Django or Flask.
+ For educational purposes, as it is one of the most taught languages in programming courses.

## How:
For this section will see how the language works in the following concept [How section](#how-1).

## Python Interpreter:

### What:
The Python Interpreter is a program that reads and executes Python code. It converts the code you write into machine-understandable instructions line by line. Python is an interpreted language, meaning the interpreter processes the code at runtime rather than compiling it beforehand.

### Why:
The Python Interpreter is essential because:
+ It provides an interactive environment (REPL: Read-Eval-Print Loop) for testing and debugging code.
+ It translates high-level Python code into machine code efficiently, without the need for manual compilation.
+ It supports dynamic typing and runtime flexibility, enabling Python's simplicity and versatility.

### When:
You use the Python Interpreter:
+ **To run Python scripts:** Execute ```.py``` files from the command line or an IDE.
+ **For quick testing:** Use the interactive shell to try out small code snippets.
+ **During debugging:** Explore variables and function outputs interactively to troubleshoot issues.
+ **For embedded systems:** Use it in environments that embed Python for scripting and automation.

### How:
**Example 1: Running Python Interactively**
```bash
# In the terminal, type:
python
# This launches the Python interpreter in interactive mode.
>>> print("Hello from the Python Interpreter!")
Hello from the Python Interpreter!
# The '>>>' is the interpreter prompt, where you can type Python commands directly.
```

**Example 2: Executing a Python Script**
```python
# Create a file named `example.py` with the following content:
print("This is a Python script!")
```
```bash
# Run the file in the terminal:
python example.py
# Output: This is a Python script!
# The interpreter reads the script and executes the code sequentially.
```

**Example 3: Using Python as a Calculator in REPL**
```bash
# Launch the interpreter:
python

>>> 5 + 7  # Performs arithmetic
12

>>> "Hello" * 3  # Demonstrates string repetition
'HelloHelloHello'
# The Python Interpreter evaluates the expressions immediately and displays the result.
```

# Basics:
+ **Note on print() and f-strings:**
    The ```print()``` function is used to output information to the console. It's a way to display values or messages while the program runs.
    f-strings (formatted string literals) allow you to embed expressions inside string literals, making it easy to format strings dynamically. You can use curly braces ```{}``` to insert variables or expressions directly into a string, like ```f"Hello, {name}"```.
    We'll dive deeper into functions later in the document.

## Basic Data Types:
### What:
Basic data types in Python are the foundational building blocks for storing and manipulating data. These types include:
+ **Integers (```int```):** Whole numbers, e.g., ```1```, ```-100```.
+ **Floating-point numbers (```float```):** Numbers with decimals, e.g., ```3.14```, ```-0.5```.
+ **Strings (```str```):** Text data, e.g., ```"hello"```, ```'Python'```.
+ **Booleans (```bool```):** Logical values, either ```True``` or ```False```.

### Why:
Basic data types are critical because:
+ They define **how data is stored and processed** in memory.
+ They provide the foundation for more complex data structures (e.g., lists, dictionaries).
+ They allow you to represent and manipulate different kinds of data + efficiently, such as numbers for calculations, text for communication, and logic for decisions.

### When:
Use basic data types:
+ **Integers and floats:** When working with numerical computations or storing counts, measurements, or calculations.
+ **Strings:** For handling and manipulating text, such as user inputs, messages, or file contents.
+ **Booleans:** For controlling logic in programs, such as conditions in ```if``` statements.(More about booleans in the conditional logic concept)

### How:
**Example 1: Using Basic Data Types**
```python
# Integer, float, string, and boolean examples
age = 16       # Integer
height = 183.5 # Float
name = "Alice" # String
is_student = True  # Boolean

print(f"{name} is {age} years old and {height} cm tall. Student: {is_student}")
# Outputs: Alice is 16 years old and 183.5 cm tall. Student: True
```
**Example 2: Performing Operations with Basic Data Types**
```python
# Basic operations
x = 10
y = 3

# Arithmetic with integers and floats
sum_ = x + y         # Addition
division = x / y     # Division (float result)
boolean_check = x > y  # Boolean result from comparison

print(f"Sum: {sum_}, Division: {division:.2f}, Is x greater than y? {boolean_check}")
# Outputs: Sum: 13, Division: 3.33, Is x greater than y? True
# :.2f rounds the value of division to two decimal places and displays it as a floating-point number.
```

**Example 3: Type Conversion and String Manipulation**
```python
# Mixing and converting data types
num_str = "50"
num = int(num_str)  # Converting string to integer

new_num = num + 10
message = f"The result is {new_num}"  # String formatting with a converted value

print(message)  # Converts the string to uppercase
# Outputs: The Result is 60
```
+ **Note:**
    While converting between data types, the original value should be compatible with the intended data type.
    For example:
    Using ```int("1 Incompatible conversion")``` this will **raise an error** because ```"1 Incompatible conversion"```contains non-numeric characters, making it impossible to convert to an integer. The Python interpreter expects the string to be a valid representation of an integer (e.g., "1"), but it encounters additional text that it cannot process.


## Variables:
### What:
Variables in Python are containers for storing data values. They act as named references to objects in memory, allowing you to manipulate and reuse data throughout your program. Python variables are dynamically typed, meaning you don’t need to declare their type explicitly.
+ **Note:**
    In Python, **an object is any data or value stored in memory**. Everything in Python, including numbers, strings... is an object.

### Why:
Variables are essential because:
+ They make code **more readable and reusable** by assigning meaningful names to data.
+ They **reduce redundancy** by storing values that can be used multiple times.
+ They allow you to perform **dynamic operations** and manage data efficiently during program execution.
    + **Note:**
    **Dynamic operations** refer to actions that can change or adapt during the program's execution. In simple terms, it means that the values or types of variables can change on the fly, depending on the conditions or inputs at runtime. Python, being dynamically typed, allows these changes without the need to explicitly define variable types in advance.

### When:
Use variables:
+ To store data for calculations or manipulations.
+ When reusing data across multiple parts of your program is needed.
+ To enhance the clarity of your code by replacing hardcoded values with descriptive names.

### How:
**Example 1: Declaring and Using Variables**
```python
# Declaring variables
name = "John"   # String variable
age = 25        # Integer variable
height = 180.5  # Float variable

# Using variables
print(f"{name} is {age} years old and {height} cm tall.")
# Outputs: John is 25 years old and 180.5 cm tall.
```
+ **Note:**
    We can declare multiple variables in one expression:
    ```python
    name, age, hight = "John", 25, 180.5 # Each variable will get assigned a value respectively 
    ``` 
**Example 2: Updating and Manipulating Variables**
```python
# Updating variables
x = 10
x = x + 5  # Incrementing the value of x by 5
print(f"x after increment: {x}")  # Outputs: x after increment: 15

# Reassigning with a new type
x = "Now I'm a string!"
print(x)  # Outputs: Now I'm a string!

```

**Example 3: Using Variables in Expressions**
```python
# Variables in calculations
length = 20
width = 10
area = length * width  # Using variables in an expression

print(f"The area of the rectangle is: {area} square units.")
# Outputs: The area of the rectangle is: 200 square units.
```
