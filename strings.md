## 🔤 **STRINGS**

Strings are sequences of characters used to store and manipulate text.

---

### **Creating Strings**

```python
s1 = "Hello"
s2 = 'World'
s3 = """Multi-line
string"""
```

---

### **Accessing Characters**

```python
text = "Python"

text[0]
text[-1]
```

---

### **Slicing Strings**

```python
text[0:4]
text[2:]
text[:3]
text[::2]
text[::-1]
```

---

### **String Length**

```python
len(text)
```

---

### **String Concatenation & Repetition**

```python
"Hello" + " World"
"Hi" * 3
```

#### **`format()` Method**

```python
"My name is {} and I am {}".format("Bob", 30)
```

---

### **Escape Characters**

```python
"Line1\nLine2"
"Tab\tSpace"
"Quote: \"Hello\""
```

---

### **Membership Operators**

```python
"Py" in "Python"
"x" not in "Python"
```

---

### **Iterating Over Strings**

```python
for char in "Python":
    pass
```

---

### **Immutability of Strings**

```python
text = "Python"
text = text.replace("P", "J")
```

---

### **Case Conversion**

```python
text.upper()
text.lower()
text.capitalize()
text.title()
text.swapcase()
text.casefold()
```

---

### **Alignment & Padding**

```python
text.center(20)
text.ljust(20)
text.rjust(20)
text.zfill(10)
```

---

### **Search & Find**

```python
text.find("a")
text.rfind("a")

text.index("a")
text.rindex("a")

text.count("a")
```

---

### **Replace & Translate**

```python
text.replace("old", "new")

table = str.maketrans("abc", "123")
text.translate(table)
```

---

### **Strip Whitespace / Characters**

```python
text.strip()
text.lstrip()
text.rstrip()
```

---

### **Split & Join**

```python
text.split()
text.split(",")
text.rsplit(",")

text.splitlines()

"-".join(["2025", "01", "01"])
```

---

### **Prefix & Suffix Checks**

```python
text.startswith("Py")
text.endswith("on")
```

---

### **Character Type Checks**

```python
text.isalpha()
text.isdigit()
text.isalnum()
text.isdecimal()
text.isnumeric()

text.islower()
text.isupper()
text.istitle()

text.isspace()
text.isprintable()
text.isascii()
```

---

### **Formatting**

```python
"Hello {}".format("World")
"{name} is {age}".format(name="Alice", age=25)

text.format_map({"name": "Bob", "age": 30})
```

---

### **Encoding & Decoding**

```python
text.encode()
```

---

### **Partitioning**

```python
text.partition(" ")
text.rpartition(" ")
```

---

### **Tabs & Spacing**

```python
text.expandtabs(4)
```

---

### **Removal (Python 3.9+)**

```python
text.removeprefix("Py")
text.removesuffix("on")
```

---

### **String Testing Examples**

```python
"123".isdigit()
"abc".isalpha()
"abc123".isalnum()
" ".isspace()
```
---

### **Notes**

* Strings are **immutable**
* All string methods return **new strings**
* Indexing starts at **0**
* Use **f-strings** for best readability

