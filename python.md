# ROOM: PYTHON CONCEPTS
**TryHackMe Link** : [PYTHON:CORE CONCEPTS](https://tryhackme.com/room/pythoncoreconcepts?utm_campaign=social_share&utm_medium=social&utm_content=share-completed-room&utm_source=copy&sharerId=6a5ba5be99ab54f7c1dacca7)<BR>
**Category** : Python introduction <br>
# What I Learned 
### Python: Overview
Python is a high-level, general-purpose programming language. It is designed to be easy to read and simple to write.<br>

**Key Features**<br>
Readable Syntax: Uses clean language that looks like English.<br>
Interpreted Language: Runs code line-by-line, making debugging faster.<br>
Cross-Platform: Works on Windows, macOS, and Linux.<br>
Versatile: Supports multiple programming styles (procedural, object-oriented).<br>

**Common Uses**<br>
Automation: Writing scripts to handle repetitive tasks.<br>
Cybersecurity: Developing tools for penetration testing and scanning.<br>
Data Science: Analyzing data and building machine learning models.<br>
Web Development: Creating backend systems for websites.<br>
## Learning Objectives & Explanations

* **Variables:** Containers that hold data values so they can be referenced or changed later.<br>
* **Conditional Statements (`if`, `elif`, `else`):** Logic blocks that run specific code only when certain conditions are true.<br>
* **Loops (`while`):** Code blocks that repeat continuously as long as a specified condition remains true.<br>
## 2. Data Types & Conversions
**Data Types:** Python automatically categorises data (e.g., Integers for whole numbers, Floats for decimals, Strings for text).<br>
**Type Conversions:** Functions like `int()`, `str()`, and `float()` that change data from one type to another.<br>
## 3. Strings & Assignment

**f-strings (`f"..."`):** A clean way to embed variables directly inside text strings by wrapping them in curly braces `{}`.<br>
**Augmented Assignment:** Shorthand operators (like `+=` or `-=`) that update a variable's value based on its current value.<br>
## 4. String Manipulation
**Built-in Methods:** Functions built into Python (like `.lower()`, `.upper()`, or `.split()`) used to modify or inspect text data.<br>
## 5. Data Structures
* **Lists `[]`:** Ordered collections used to store multiple items in a single variable, accessed by their position (index).<br>
* **Dictionaries `{}`:** Unordered collections that store data in key-value pairs, letting you look up data by its label.<br>
## 6. Operators
* **Arithmetic:** Math symbols used to calculate values (`+`, `-`, `*`, `/`).<br>
* **Comparison:** Symbols used to evaluate relationships between values (`==`, `!=`, `<`, `>`).<br>
* **Logical:** Words used to combine multiple conditions (`and`, `or`, `not`).<br>
* **Membership:** The `in` and `not in` keywords used to check if an item exists inside a list, string, or dictionary.<br>
## 7. Iteration & Advanced Loops
* **`for` loops:** Loops designed to step through a specific sequence, like items in a list or characters in a string.<br>
* **`range()`:** A function that generates a sequence of numbers, perfect for controlling how many times a loop runs.<br>
## 8. Loop Control Flow
* **`break`:** Instantly terminates the loop completely, jumping to the next lines of code outside the loop.<br>
* **`continue`:** Skips the rest of the current loop iteration and moves straight to the next cycle.<br>
## Machine Setup
Click the **Start Machine** button to launch your Target VM.

* **IDE:** Visual Studio Code (opens automatically).
* **Code Location:** `/home/ubuntu/Core-Concepts/`
* **Action Item:** Activate your virtual environment on the Lab Machine before starting. We strongly encourage you to run and modify all code snippets as you progress.
## Python Basics 
A concise reference guide covering foundational Python concepts, data types, conditional logic, and modern syntax.
## 1. The Basics & Variables
* `print()` outputs text to the screen. 
* Strings must be enclosed in single (`'`) or double (`"`) quotes.
* `#` denotes comments, which are ignored by the computer.
* Use `=` to assign and update variable values.

```python
# Print hello world
print("Hello World")

# Variable assignment & manipulation
age = 30
age += 1 # Augmented assignment (same as age = age + 1)
print(f"Age: {age}") # Outputs 31
```
## 2. Core Data Types
Check any data type using `type(variable_name)`.
| Type | Name | Example | Description |
| :--- | :--- | :--- | :--- |
| `str` | String | `"hello"` | Text and symbols |
| `int` | Integer | `42` | Whole numbers |
| `float`| Float | `3.14` | Decimal numbers |
| `bool` | Boolean | `True` / `False` | Logical on/off |
| `list` | List | `[1, 2, 3]` | Ordered collection |
## 3. Conditionals & Operators
* **`=` vs `==`**: `=` assigns data; `==` compares data.
* Code blocks under `if`, `elif`, and `else` must be indented.
### Comparison Operators
* `==` (Equal), `!=` (Not equal)
* `<`, `>` (Less/Greater than)
* `<=`, `>=` (Less/Greater than or equal)
### Logical Operators
* `and`: True if **both** sides are true.
* `or`: True if **at least one** side is true.
* `not`: Inverts the boolean value.

```python
name = "bob"
hungry = True

if name == "bob" and hungry:
    print("Bob is hungry")
elif name == "bob" and not hungry:
    print("Bob is not hungry")
else:
    print("Unknown person status")
```
## 4. Type Conversion
Functions like `input()` always return data as a string (`str`). Use conversion functions to change types before performing math.

| Function | Converts To | Example |
| :--- | :--- | :--- |
| `int()` | Integer | `int("42")` → `42` |
| `float()`| Float | `float("3.14")` → `3.14` |
| `str()` | String | `str(42)` → `"42"` |
| `bool()` | Boolean | `bool(0)` → `False` |

```python
text_input = input("Enter port: ") # "443" (str)
port_num = int(text_input)         # 443 (int)
```
## 5. Modern Formatting (f-strings)
Prefix a string with `f` to embed variables directly inside curly braces `{}`.
```python
username = "admin"
port = 443
# Modern f-string approach
print(f"User {username} is on port {port}")
# Output: User admin is on port 443
```
## Python Strings
A condensed reference for string manipulation, indexing, slicing, and built-in methods.
### 1. Length & Indexing
* `len()` returns the total character count.
* Indexing starts at `0`. Negative indices count backward from the end (`-1` is the last item).
| Index | 0 | 1 | 2 | 3 | 4 | 5 |
| :--- | :-: | :-: | :-: | :-: | :-: | :-: |
| **Character** | P | y | t | h | o | n |
```python
word = "Python"
print(len(word))   # 6
print(word[0])     # P
print(word[-1])    # n
```
### 2. Slicing
Syntax: `string[start:end]` (Includes `start`, excludes `end`).
```python
word = "Python"
print(word[0:3])   # "Pyt" (Indices 0, 1, 2)
print(word[2:])    # "thon" (Index 2 to end)
print(word[:4])    # "Pyth" (Start to index 3)
```
### 3. Essential String Methods
Methods return modified copies; they do not alter the original string.

| Method | Purpose | Example | Result |
| :--- | :--- | :--- | :--- |
| `.upper()` | Uppercase | `"hi".upper()` | `"HI"` |
| `.lower()` | Lowercase | `"HI".lower()` | `"hi"` |
| `.strip()` | Remove outer spacing | `" hi ".strip()` | `"hi"` |
| `.replace(a, b)` | Replace text | `"cat".replace("c", "b")` | `"bat"` |
| `.split(sep)` | Convert to list | `"a,b".split(",")` | `["a", "b"]` |
| `.startswith(x)`| Check starting text | `"http".startswith("ht")`| `True` |
| `.endswith(x)` | Check ending text | `"a.txt".endswith(".txt")`| `True` |
| `.count(x)` | Count occurrences | `"banana".count("a")` | `3` |
### 4. Character Checks & Existence
These methods scan characters or substrings and return Booleans (`True`/`False`).
```python
# Type Verification
char = "A"
print(char.isupper())    # True
print(char.isdigit())    # False
print(char.isalpha())    # True (Is it a letter?)
print(char.isalnum())    # True (Is it alphanumeric?)
# The 'in' Operator (Substring Check)
url = "https://tryhackme.com"
print("tryhackme" in url) # True
```
## Python Collections 
A concise reference for working with lists (ordered arrays) and dictionaries (key-value maps).
### 1. Lists
Ordered, mutable collections of data defined with square brackets `[]`. 
* **Indexing & Slicing**: Works exactly like strings. Index `0` is the first item; `-1` is the last item.
* **Mutating**: Update elements directly using `list[index] = new_value`.
* **Existence**: Use `item in list` to check for membership.
```python
ports = [22, 80, 443, 8080]
# Access & Slice
print(ports[0])      # 22
print(ports[1:3])    # [80, 443]

# Modify & Check
ports[0] = 2222      # [2222, 80, 443, 8080]
is_web = 80 in ports # True
```
#### Essential List Methods
| Method | Purpose | Example / Shorthand |
| :--- | :--- | :--- |
| `.append(x)` | Adds item to the very end | `ports.append(3306)` |
| `.remove(x)` | Deletes first occurrence of value `x` | `ports.remove(80)` |
| `.pop(i)` | Deletes and returns item at index `i` | `ports.pop(0)` |
| `.sort()` | Sorts items in ascending order | `ports.sort()` |
| `.reverse()` | Flips the order of the list items | `ports.reverse()` |
| `len(list)` | Global function returning item count | `len(ports)` |
### 2. Dictionaries
Unordered, mutable collections of key-value pairs defined with curly braces `{}`.
* **Access**: Retrieve values using `dict[key]`.
* **Safety**: Accessing a non-existent key via `dict[key]` crashes the program. Use `.get()` instead.
```python
# Initialization
services = {22: "SSH", 80: "HTTP", 443: "HTTPS"}

# Read, Add, and Update
print(services[22])       # "SSH"
services[8080] = "Web"    # Adds new pair
services[22] = "OpenSSH"  # Updates existing key

# Delete
del services[80]          # Removes port 80

# Key Checking
has_ssl = 443 in services # True (Checks keys only)
```
#### Essential Dictionary Methods
| Method | Returns / Purpose | Example Output |
| :--- | :--- | :--- |
| `.keys()` | All dictionary keys | `dict_keys([22, 443, 8080])` |
| `.values()` | All dictionary values | `dict_values(['OpenSSH', 'HTTPS', 'Web'])` |
| `.items()` | All key-value pairs as tuples | `dict_items([(22, 'OpenSSH'), ...])` |
| `.get(k, d)` | Value for key `k`; returns `d` if missing | `services.get(99, "Unknown")` |
## Python Operators 
A concise reference for advanced arithmetic operators, membership conditions, and practical logic evaluation.
### 1. Advanced Arithmetic Operators
Standard operators (`+`, `-`, `*`, `/`) apply normally. Regular division (`/`) always returns a floating-point number.
| Operator | Name | Example | Result | Purpose / Security Use Case |
| :--- | :--- | :--- | :--- | :--- |
| `**` | Exponent | `2 ** 8` | `256` | Calculating key space combinations (e.g., `2 ** 128`) |
| `//` | Floor Division | `7 // 2` | `3` | Dividing numbers and rounding down to the nearest integer |
| `%` | Modulus | `7 % 2` | `1` | Checking remainders. Useful for parity checks (`num % 2 == 0`) |
```python
print(7 / 2)   # 3.5 (Float)
print(7 // 2)  # 3   (Integer, rounded down)
print(7 % 2)   # 1   (Remainder)
print(2 ** 8)  # 256 (2 to the power of 8)
```
### 2. The Membership Operator (`in` / `not in`)
Evaluates containment across collection types like strings, lists, and dictionaries.
```python
common = ["123456", "password", "qwerty"]
user_pass = "qwerty"

# Check presence
if user_pass in common:
    print("Password is too common.")

# Check absence
if "secure_pass" not in common:
    print("Password is not in the blocklist.")
```
### 3. Practical Logic Evaluation
Combining length checks, membership testing, and logical operators (`and`, `or`, `not`) for validation workflows.
```python
password = "Tr0ubador"
# Simple security validation logic
if len(password) >= 8 and any(c.isdigit() for c in password):
    print("Moderate strength")
elif len(password) >= 8 or any(c.isdigit() for c in password):
    print("Weak, but has some merit")
else:
    print("Very weak")
```
## Python Loops Cheat Sheet
A concise reference for repeating code blocks using `while` and `for` loops, handling sequences, and managing loop control.
### 1. Loop Types: `while` vs `for`
* Use **`while`** loops when execution depends on a changing condition (e.g., tracking retry attempts).
* Use **`for`** loops when iterating over a known sequence (lists, strings, ranges, or dictionaries).
```python
# while loop: Runs as long as condition stays True
attempts = 0
while attempts < 3:
    attempts += 1
    print(f"Attempt {attempts} of 3")

# for loop: Iterates through an explicit collection
targets = ["192.168.1.1", "192.168.1.2"]
for ip in targets:
    print(f"Scanning {ip}...")
```
### 2. Iteration Targets & Techniques
You can loop through strings (character-by-character) or dictionaries using specific methods.
```python
# String Iteration
for char in "S3cure!":
    if char.isdigit():
        print(f"Found digit: {char}")

# Dictionary Iteration (Keys & Values)
services = {22: "SSH", 80: "HTTP"}
for port, name in services.items():
    print(f"Port {port} runs {name}")
```
### 3. The `range()` Function
Generates custom number sequences. The `stop` integer is always excluded.
| Syntax | Description | Example | Numbers Generated |
| :--- | :--- | :--- | :--- |
| `range(stop)` | `0` to `stop - 1` | `range(5)` | `0, 1, 2, 3, 4` |
| `range(start, stop)` | `start` to `stop - 1` | `range(1, 6)` | `1, 2, 3, 4, 5` |
| `range(start, stop, step)`| Increments sequence by `step` | `range(0, 20, 5)` | `0, 5, 10, 15` |
### 4. Loop Control: `break` & `continue`
* **`break`**: Immediately exits the loop entirely.
* **`continue`**: Skips the remaining code in the *current* iteration and jumps to the next cycle.
```python
# break: Stop immediately upon matching a condition
for port in:
    if port == 443:
        break
    print(f"Checked {port}") # Checks 22 and 80, then stops entirely

# continue: Skip invalid entries and move forward
lines = ["admin", "", "root"]
for line in lines:
    if line == "":
        continue
    print(f"User: {line}") # Processes "admin" and "root", skips ""
```