## 🔁 **LOOPING STATEMENTS**

Looping statements allow a program to execute a block of code repeatedly.

---

### **`for` Loop**

Used to iterate over a sequence (list, tuple, string, range).

```python
for i in range(5):
    pass
```

---

### **`for` Loop with `range()`**

```python
for i in range(1, 10, 2):
    pass
```

---

### **Looping Through a List**

```python
items = ["apple", "banana", "cherry"]

for item in items:
    pass
```

---

### **Looping Through a String**

```python
for char in "python":
    pass
```

---

### **`while` Loop**

Runs as long as the condition is `True`.

```python
count = 0

while count < 5:
    count += 1
```

---

### **`break` Statement**

Stops the loop immediately.

```python
for i in range(10):
    if i == 5:
        break
```

---

### **`continue` Statement**

Skips the current iteration and continues with the next.

```python
for i in range(5):
    if i == 2:
        continue
```

---

### **`pass` Statement**

Acts as a placeholder where a statement is required.

```python
for i in range(3):
    pass
```

---

### **`else` with Loops**

Executed when the loop finishes normally (not terminated by `break`).

```python
for i in range(3):
    pass
else:
    completed = True
```

```python
while False:
    pass
else:
    completed = True
```

---

### **Nested Loops**

```python
for i in range(3):
    for j in range(2):
        pass
```

---

### **Enumerate**

Returns both index and value.

```python
colors = ["red", "green", "blue"]

for index, color in enumerate(colors):
    pass
```

---

### **Zip**

Iterates over multiple sequences in parallel.

```python
names = ["Alice", "Bob"]
scores = [90, 85]

for name, score in zip(names, scores):
    pass
```

---

### **List Comprehension (Loop Shortcut)**

```python
squares = [x ** 2 for x in range(5)]
```

---

### **Notes**

* Use **`for`** when the number of iterations is known
* Use **`while`** when looping depends on a condition
* Avoid infinite loops unless intentional
* Prefer **list comprehensions** for simple transformations

---
