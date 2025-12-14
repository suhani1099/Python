## 📦 **TUPLES**

Tuples are **ordered, immutable** collections used to store multiple items in a single variable.

---

### **Creating Tuples**

```python
t1 = (1, 2, 3)
t2 = "a", "b", "c"      # tuple packing
single = (5,)           # single-element tuple
empty = ()
```

---

### **Accessing Elements**

```python
t1[0]
t1[-1]
```

---

### **Slicing Tuples**

```python
t1[1:3]
t1[:2]
t1[::2]
t1[::-1]
```

---

### **Tuple Length**

```python
len(t1)
```

---

### **Tuple Immutability**

```python
# This will raise an error
t1[0] = 10
```

---

### **Tuple Concatenation & Repetition**

```python
(1, 2) + (3, 4)
(0,) * 5
```

---

### **Membership Operators**

```python
2 in t1
5 not in t1
```

---

### **Iterating Over Tuples**

```python
for item in t1:
    pass
```

---

### **Enumerate with Tuples**

```python
for index, value in enumerate(t1):
    pass
```

---

### **Tuple Packing & Unpacking**

```python
point = (3, 4)

x, y = point
```

```python
a, b, *rest = (1, 2, 3, 4, 5)
```

---

### **Nested Tuples**

```python
nested = ((1, 2), (3, 4))

nested[1][0]
```

---

### **Tuple Methods**

```python
t1.count(2)
t1.index(3)
```

---

### **Built-in Functions with Tuples**

```python
min(t1)
max(t1)
sum(t1)
sorted(t1)
```

---

### **Tuple vs List**

| Feature     | Tuple      | List         |
| ----------- | ---------- | ------------ |
| Mutable     | ❌ No       | ✅ Yes        |
| Syntax      | `()`       | `[]`         |
| Performance | Faster     | Slower       |
| Use Case    | Fixed data | Dynamic data |

---

### **Notes**

* Tuples are **immutable**
* Faster than lists
* Can be used as **dictionary keys**
* Parentheses are optional (except for single-element tuples)

---

