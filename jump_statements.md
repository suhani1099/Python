## ⏭️ **JUMP STATEMENTS**

Jump statements alter the normal flow of execution in loops or functions.

---

### **`break` Statement**

Immediately exits the loop.

```python
for i in range(10):
    if i == 5:
        break
```

---

### **`continue` Statement**

Skips the current iteration and moves to the next one.

```python
for i in range(5):
    if i == 2:
        continue
```

---

### **`pass` Statement**

Acts as a placeholder where a statement is syntactically required.

```python
for i in range(3):
    pass
```

---

### **`return` Statement**

Exits a function and optionally returns a value.

```python
def add(a, b):
    return a + b
```

---

### **`yield` Statement**

Pauses a function and returns a value, turning it into a generator.

```python
def count_up(n):
    for i in range(n):
        yield i
```

---

### **`raise` Statement**

Forces an exception to occur.

```python
if x < 0:
    raise ValueError("Negative value not allowed")
```

---

### **Notes**

* `break` and `continue` are used **only inside loops**
* `pass` does nothing but prevents syntax errors
* `return` ends function execution
* `yield` produces values one at a time (memory efficient)
* `raise` is used for custom error handling

---

Just say 👍
