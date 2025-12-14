# Python Notes: Introduction, Tokens, and Variables

## 1. Introduction to Python

Python is a high-level, interpreted programming language known for its simplicity and readability. It is widely used for web development, data science, automation, artificial intelligence, and more.

### Key Features:

* Easy to learn and write
* Large standard library
* Supports multiple programming paradigms
* Cross-platform compatibility

Python Character Set

Python supports the Unicode character set, which means it can represent characters from almost every writing system in the world. Unicode provides a unique code point for every character, symbol, emoji, or script, ensuring consistency across different platforms and languages.

## 1. What Is a Character Set?

A character set is a collection of characters that a programming language recognizes.
Python uses Unicode, allowing it to handle:

English characters```A-Z , a-z```

Numbers           ```0-9```

Symbols           ```+-*/**\(){}[]//=!= == <,>.'"''',:;%!&#<=>=@ _```

Whitespaces       ```Blank space, tabs ,carriage return ,newline,formfeed```

Other characters:    Python can process all ASCII and unicode characters as part of data or libraries.

## 2. Python Tokens

Tokens are the smallest components in a Python program. They form the building blocks of Python code.

Python tokens include:

### **1. Keywords**

Reserved words with special meaning.Python contains 33 keywords, which are special reserved words that have predefined meanings in the language and cannot be used as variable names. These keywords include:
```False, None, True, and, as, assert, break, class, continue, def, del, elif, else, except, finally, for, from, global, if, import, in, is, lambda, nonlocal, not, or, pass, raise, return, try, while, with, and yield.``` 

### **2. Identifiers**

Names given to variables, functions, classes, etc.
Rules:

* The first character must be a letter; the underscore(_) counts as a letter.
* Must not start with a digit
* Cannot use keywords
* Case-sensitive and can be unlimited in length

Example:

```
name = "Alice"
```

### **3. Literals**

Fixed values such as:

* Numeric: `10`, `3.14`
* String: `'hello'`, `"world"`
* Boolean: `True`, `False`
* Special literal: `None`

### **4. Operators**

Symbols that perform operations.
Operators in Python are special symbols or keywords used to perform operations on values and variables.

### 4.1 Arithmetic Operators

```
+  Addition
-  Subtraction
*  Multiplication
/  Division
%  Modulus
** Exponent
// Floor Division
```

### 4.2 Comparison Operators

```
== Equal to
!= Not equal to
>  Greater than
<  Less than
>= Greater than or equal to
<= Less than or equal to
```

### 4.3 Logical Operators

```
and  Logical AND
or   Logical OR
not  Logical NOT
```

### 4.4 Assignment Operators

```
=   Assign
+=  Add and assign
-=  Subtract and assign
*=  Multiply and assign
/=  Divide and assign
%=  Modulus and assign
**= Exponent and assign
//= Floor divide and assign
```

### 4.5 Bitwise Operators

```
&  AND
|  OR
^  XOR
~  NOT
<< Left shift
>> Right shift
```

### 4.6 Membership Operators

```
in      True if value exists in sequence
not in  True if value does not exist
```

### 4.7 Identity Operators

```
is      True if objects are same
is not  True if objects are not same
```

Examples:

```
+, -, *, /, %, ==, !=, and, or, not
```

### 4.8. Punctuation (Delimiters)

Characters used to structure code.
Examples:

```
' " # \ () {} [] : ; @ , . ` =
```
## 3. Barebones of a Python Program

A Python program may contain various elements such as comments, expressions, statements, functions, and blocks.

### **Basic Structure**

```python
42  # expression statement

def my_function():  # function definition
    # This is a block (indented code)
    x = 1          # statement
    y = x + 1      # expression inside a statement
    return y       # statement

my_function()  # expression statement
```

---

### **Comment**

A **comment** is text ignored by the Python interpreter. It is used to explain code to humans.

Example:

```python
# This is a comment
```

---

### **Expression**

An **expression** is code that produces a value.

Examples:

```python
42
x + 1
my_function()
```

An **expression statement** is an expression used on its own line:

```python
42
my_function()
```

---

### **Statement**

A **statement** is a complete instruction that performs an action.

Examples:

```python
x = 1
return y
```

---

### **Function**

A **function** is a named, reusable block of code that can take inputs and return a value.

Example:

```python
def my_function():
    return 1
```

---

### **Block**

A **block** is a group of statements executed together. In Python, blocks are defined by indentation.

Example:

```python
def my_function():
    x = 1
    return x
```

---

### **Indentation**

**Indentation** is how Python defines blocks instead of using braces `{}`.

Example:

```python
if True:
    print("inside block")
```

---

### **Program**

A **program** is a sequence of statements executed by the Python interpreter.

Example:

```python
# The entire file is a Python program
```

---

## 4. Variables in Python

A **variable** is a name that refers to a value stored in memory.

---

### **Declaring Variables**

Python does not require explicit type declarations.

```python
x = 10
name = "John"
pi = 3.14
```

---

### **Variable Naming Rules**

* Must start with a letter or underscore (`_`)
* Cannot start with a number
* Cannot contain special characters like `@`, `$`, `%`
* Case-sensitive

---

### **Multiple Assignment**

```python
a, b, c = 1, 2, 3
```

---

### **Dynamic Typing**

Variables can change type during execution:

```python
x = 10      # integer
x = "hi"    # string
```

---

### **Constant Convention**

Python does not have true constants, but uppercase names indicate constant-like behavior:

```python
PI = 3.14159
```

---

## 5. Simple Input and Output

```python
name = input("Enter your name: ")
print(name)
```

* **Input** → `input()` reads a line of text from the user
* **Output** → `print()` writes text to the screen
* **Statement** → assignment to `name`
* **Expression** → `input(...)`, `name`
