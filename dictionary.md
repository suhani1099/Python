##  **DICTIONARIES**

Dictionaries store data as **key–value pairs**. They are **unordered (insertion-ordered since Python 3.7)**, **mutable**, and keys must be **unique and immutable**.

---

##  **Creating Dictionaries**

```python
d1 = {"name": "Alice", "age": 25}
d2 = dict(city="London", country="UK")
empty = {}
```

---

##  **Accessing Values**

```python
d1["name"]
d1.get("age")
d1.get("salary", 0)     # default value
```

---

##  **Adding & Updating Items**

```python
d1["age"] = 26
d1["job"] = "Engineer"
```

---

##  **Removing Items**

```python
d1.pop("job")
d1.popitem()            # removes last item
del d1["age"]
d1.clear()
```

---

##  **Iterating Over Dictionaries**

```python
for key in d1:
    pass

for value in d1.values():
    pass

for key, value in d1.items():
    pass
```

---

##  **Dictionary Methods (ALL)**

### **`dict.keys()`**

Returns all keys.

```python
d1.keys()
```

### **`dict.values()`**

Returns all values.

```python
d1.values()
```

### **`dict.items()`**

Returns key–value pairs.

```python
d1.items()
```

---

### **`dict.get(key, default)`**

Safely gets a value.

```python
d1.get("name")
```

---

### **`dict.update()`**

Updates dictionary with another mapping.

```python
d1.update({"age": 30, "city": "Paris"})
```

---

### **`dict.pop(key)`**

Removes and returns value.

```python
d1.pop("age")
```

---

### **`dict.popitem()`**

Removes last inserted item.

```python
d1.popitem()
```

---

### **`dict.clear()`**

Removes all items.

```python
d1.clear()
```

---

### **`dict.copy()`**

Shallow copy.

```python
new_dict = d1.copy()
```

---

### **`dict.setdefault(key, default)`**

Returns value; inserts if missing.

```python
d1.setdefault("country", "USA")
```

---

### **`dict.fromkeys(iterable, value)`**

Creates new dictionary.

```python
dict.fromkeys(["a", "b", "c"], 0)
```

---

##  **Dictionary Membership**

```python
"name" in d1
"salary" not in d1
```

---

##  **Built-in Functions with Dictionaries**

```python
len(d1)
min(d1)
max(d1)
sorted(d1)
```

---

##  **Dictionary Comprehension**

```python
squares = {x: x**2 for x in range(5)}
```

---

##  **Nested Dictionaries**

```python
user = {
    "name": "Alice",
    "address": {
        "city": "London",
        "zip": 12345
    }
}

user["address"]["city"]
```

---

##  **Merging Dictionaries (Python 3.9+)**

```python
d3 = d1 | d2
```

---

##  **Dictionary Immutability Rules**

```python
# valid key
{(1, 2): "tuple key"}

# invalid key
# {[1, 2]: "list key"}  # error
```

---

##  **Dictionary vs List vs Tuple**

| Feature     | Dictionary  | List   | Tuple  |
| ----------- | ----------- | ------ | ------ |
| Mutable     | ✅ Yes       | ✅ Yes  | ❌ No   |
| Ordered     | ✅ Yes       | ✅ Yes  | ✅ Yes  |
| Key-Value   | ✅ Yes       | ❌ No   | ❌ No   |
| Fast Lookup | ✅ Very Fast | ❌ Slow | ❌ Slow |

---

##  **Notes**

* Keys must be **immutable**
* Values can be **any data type**
* Dictionary lookup is **O(1)**
* Ideal for structured data

---

