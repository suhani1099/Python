## **FUNCTIONS**

Functions are reusable blocks of code designed to perform a specific task.

---

## **Defining a Function**

```python
def greet():
    pass
```

---

## **Function Parameters**

```python
def greet(name):
    pass
```

---

## **Return Statement**

```python
def add(a, b):
    return a + b
```

---

## **Calling a Function**

```python
result = add(3, 4)
```

---

## **Positional Arguments**

```python
def subtract(a, b):
    return a - b

subtract(10, 5)
```

---

## **Keyword Arguments**

```python
subtract(b=5, a=10)
```

---

## **Default Parameters**

```python
def greet(name="Guest"):
    pass
```

---

## **Variable-Length Arguments**

### **`*args` (Non-Keyword Arguments)**

```python
def total(*args):
    return sum(args)
```

---

### **`**kwargs` (Keyword Arguments)**

```python
def info(**kwargs):
    return kwargs
```

---

## **Mixing Arguments**

```python
def demo(a, b, *args, **kwargs):
    pass
```

---

## **Recursive Functions**

```python
def factorial(n):
    if n == 0:
        return 1
    return n * factorial(n - 1)
```

---

## **Lambda Functions**

```python
square = lambda x: x ** 2
```

---

## **Docstrings**

```python
def add(a, b):
    """Returns the sum of two numbers."""
    return a + b
```

---

## **Type Annotations**

```python
def add(a: int, b: int) -> int:
    return a + b
```

---

## **Nested Functions**

```python
def outer():
    def inner():
        pass
    inner()
```

---

## **Scope (LEGB Rule)**

```python
x = 10

def demo():
    x = 5
```

---

## **Global Keyword**

```python
count = 0

def increment():
    global count
    count += 1
```

---

## **Nonlocal Keyword**

```python
def outer():
    x = 10
    def inner():
        nonlocal x
        x += 5
```

---

## **Generator Functions**

```python
def count_up(n):
    for i in range(n):
        yield i
```

---

## **Functions as Arguments**

```python
def apply(func, value):
    return func(value)
```

---

## **Built-in Function Examples**

```python
len([1, 2, 3])
sum([1, 2, 3])
min([1, 2, 3])
max([1, 2, 3])
```

---

## **Functions vs Lambda**

| Feature     | Function      | Lambda             |
| ----------- | ------------- | ------------------ |
| Name        | Required      | Optional           |
| Lines       | Multiple      | Single             |
| Readability | High          | Lower              |
| Use Case    | Complex logic | Simple expressions |

---

## **Notes**

* Functions improve code reuse
* Use `return` to send values back
* Lambda functions are best for short operations
* Generators are memory efficient

---
