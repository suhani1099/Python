##  **SETS**

Sets are **unordered**, **mutable** collections of **unique elements**. They are optimized for fast membership testing and mathematical set operations.

---

##  **Creating Sets**

```python
s1 = {1, 2, 3}
s2 = set([3, 4, 5])
empty = set()        # {} creates a dict, not a set
```

---

##  **Membership Testing**

```python
2 in s1
10 not in s1
```

---

##  **Adding Elements**

### **`add()`** – Add one element

```python
s1.add(4)
```

### **`update()`** – Add multiple elements

```python
s1.update([5, 6, 7])
```

---

##  **Removing Elements**

### **`remove()`** – Raises error if missing

```python
s1.remove(3)
```

### **`discard()`** – No error if missing

```python
s1.discard(10)
```

### **`pop()`** – Removes random element

```python
s1.pop()
```

### **`clear()`** – Removes all elements

```python
s1.clear()
```

---

##  **Set Operations (Methods)**

### **Union**

```python
s1.union(s2)
```

### **Intersection**

```python
s1.intersection(s2)
```

### **Difference**

```python
s1.difference(s2)
```

### **Symmetric Difference**

```python
s1.symmetric_difference(s2)
```

---

##  **Set Operations (Operators)**

```python
s1 | s2    # union
s1 & s2    # intersection
s1 - s2    # difference
s1 ^ s2    # symmetric difference
```

---

##  **Subset / Superset Checks**

```python
s1.issubset(s2)
s1.issuperset(s2)
s1.isdisjoint(s2)
```

---

##  **Set Methods (ALL)**

### **`copy()`**

```python
s3 = s1.copy()
```

### **`difference_update()`**

```python
s1.difference_update(s2)
```

### **`intersection_update()`**

```python
s1.intersection_update(s2)
```

### **`symmetric_difference_update()`**

```python
s1.symmetric_difference_update(s2)
```

---

##  **Built-in Functions with Sets**

```python
len(s1)
min(s1)
max(s1)
sum(s1)
sorted(s1)
```

---

##  **Set Comprehension**

```python
evens = {x for x in range(10) if x % 2 == 0}
```

---

##  **Frozen Sets (Immutable Sets)**

```python
fs = frozenset([1, 2, 3])
```

---

##  **Set vs List vs Tuple**

| Feature    | Set   | List  | Tuple |
| ---------- | ----- | ----- | ----- |
| Ordered    | ❌ No  | ✅ Yes | ✅ Yes |
| Mutable    | ✅ Yes | ✅ Yes | ❌ No  |
| Duplicates | ❌ No  | ✅ Yes | ✅ Yes |
| Indexing   | ❌ No  | ✅ Yes | ✅ Yes |

---

##  **Notes**

* Sets do **not allow duplicates**
* Elements must be **immutable**
* No indexing or slicing
* Ideal for **membership tests & uniqueness**

---
