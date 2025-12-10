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

### **5. Punctuation (Delimiters)**

Characters used to structure code.
Examples:

```
' " # \ () {} [] : ; @ , . ` =
```

## 3. Variables in Python

A variable is a name that refers to a value stored in memory.

### **Declaring Variables**

Python does not require explicit type declaration.

```
x = 10
name = "John"
pi = 3.14
```

### **Variable Naming Rules**

* Must start with a letter or underscore
* Cannot start with a number
* Cannot contain special characters like `@`, `$`, `%`
* Case-sensitive

### **Multiple Assignment**

```
a, b, c = 1, 2, 3
```

### **Dynamic Typing**

Variables can change type during execution:

```
x = 10     # integer
x = "hi"   # string
```

### **Constant Convention**

Python does not have true constants, but uppercase names indicate constant-like behavior:

```
PI = 3.14159
```


