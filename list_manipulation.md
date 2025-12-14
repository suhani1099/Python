## 📋 **LISTS**

Lists are **ordered, mutable** collections used to store multiple items in a single variable.

---

### **Creating Lists**

```python
numbers = [1, 2, 3, 4, 5]
mixed = [1, "a", 3.5, True]
empty = []
```

---

### **Accessing Elements**

```python
numbers[0]
numbers[-1]
```

---

### **Slicing Lists**

```python
numbers[1:4]
numbers[:3]
numbers[::2]
numbers[::-1]
```

---

### **List Length**

```python
len(numbers)
```

---

### **Modifying Lists**

```python
numbers[0] = 10
numbers[1:3] = [20, 30]
```

---

### **Adding Elements**

```python
numbers.append(6)
numbers.extend([7, 8])
numbers.insert(1, 15)
```

---

### **Removing Elements**

```python
numbers.remove(20)
numbers.pop()
numbers.pop(0)
numbers.clear()
```

---

### **Searching & Counting**

```python
numbers.index(30)
numbers.count(10)
```

---

### **Sorting & Reversing**

```python
numbers.sort()
numbers.sort(reverse=True)

numbers.reverse()
```

---

### **Copying Lists**

```python
copy1 = numbers.copy()
copy2 = numbers[:]
copy3 = list(numbers)
```

---

### **List Concatenation & Repetition**

```python
[1, 2] + [3, 4]
[0] * 5
```

---

### **Membership Operators**

```python
3 in numbers
9 not in numbers
```

---

### **Iterating Over Lists**

```python
for item in numbers:
    pass
```

---

### **Enumerate with Lists**

```python
for index, value in enumerate(numbers):
    pass
```

---

### **List Comprehensions**

```python
squares = [x ** 2 for x in range(5)]
```

```python
evens = [x for x in numbers if x % 2 == 0]
```

---

### **Nested Lists**

```python
matrix = [
    [1, 2, 3],
    [4, 5, 6]
]

matrix[0][1]
```

---

### **Built-in List Functions**

```python
min(numbers)
max(numbers)
sum(numbers)
sorted(numbers)
```

---

### **Notes**

* Lists are **mutable**
* Indexing starts at **0**
* Lists can store **mixed data types**
* List comprehensions are **faster and cleaner**

---
