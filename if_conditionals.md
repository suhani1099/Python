## 🔀 **IF CONDITIONALS**

**Conditional statements** allow a program to execute different blocks of code based on boolean expressions.

---

### **Basic `if` Statement**

```python
x = 10

if x > 5:
    pass
```

---

### **`if` / `else` Statement**

```python
x = 3

if x % 2 == 0:
    pass
else:
    pass
```

---

### **`if` / `elif` / `else`**

```python
score = 85

if score >= 90:
    grade = "A"
elif score >= 80:
    grade = "B"
elif score >= 70:
    grade = "C"
else:
    grade = "F"
```

---

### **Multiple Conditions**

```python
age = 20

if age >= 18 and age <= 65:
    eligible = True
```

```python
x = 5

if x < 0 or x > 10:
    pass
```

---

### **Nested `if` Statements**

```python
x = 15

if x > 10:
    if x < 20:
        pass
```

---

### **Comparison Operators**

```python
x == y   # equal
x != y   # not equal
x > y    # greater than
x < y    # less than
x >= y   # greater than or equal
x <= y   # less than or equal
```

---

### **Membership & Identity**

```python
x in [1, 2, 3]
x not in [4, 5, 6]

x is None
x is not None
```

---

### **Ternary (Conditional Expression)**

```python
result = "Even" if x % 2 == 0 else "Odd"
```

---

### **Boolean Values**

```python
True
False
```

---

### **Truthiness**

```python
if []:
    pass

if 0:
    pass

if "":
    pass

if None:
    pass
```

