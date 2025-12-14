# **Recursion in Python**

Recursion is a **programming technique** where a function **calls itself** to solve a smaller instance of a problem until a **base condition** is met.

---

## **1. Definition**

* Recursion is a method of solving problems by **breaking them down into smaller, simpler subproblems**.
* Each recursive call moves closer to a **base case**, which stops further recursion.

---

## **2. Key Points**

* Every recursive function must have a **base case** to avoid infinite recursion.
* Recursive functions can be **direct** (function calls itself) or **indirect** (function calls another function that calls the original function).
* Recursion can be used to solve problems like **factorials, Fibonacci series, tree traversal, and more**.
* Recursive calls use the **call stack**, so too many calls can cause a **stack overflow**.

---

## **3. Basic Example**

**Factorial of a number using recursion**

```python
def factorial(n):
    if n == 0 or n == 1:  # base case
        return 1
    else:
        return n * factorial(n - 1)  # recursive call

print(factorial(5))  # Output: 120
```

---

## **4. Fibonacci Series using Recursion**

```python
def fibonacci(n):
    if n <= 0:
        return 0
    elif n == 1:
        return 1
    else:
        return fibonacci(n-1) + fibonacci(n-2)

# Print first 10 Fibonacci numbers
for i in range(10):
    print(fibonacci(i), end=" ")  # Output: 0 1 1 2 3 5 8 13 21 34
```

---

## **5. Sum of N Numbers**

```python
def sum_n(n):
    if n == 0:
        return 0
    else:
        return n + sum_n(n-1)

print(sum_n(10))  # Output: 55
```

---

## **6. Reverse a String using Recursion**

```python
def reverse_string(s):
    if len(s) == 0:
        return s
    else:
        return reverse_string(s[1:]) + s[0]

print(reverse_string("Python"))  # Output: nohtyP
```

---

## **7. Tower of Hanoi**

```python
def tower_of_hanoi(n, source, auxiliary, target):
    if n == 1:
        print(f"Move disk 1 from {source} to {target}")
        return
    tower_of_hanoi(n-1, source, target, auxiliary)
    print(f"Move disk {n} from {source} to {target}")
    tower_of_hanoi(n-1, auxiliary, source, target)

tower_of_hanoi(3, 'A', 'B', 'C')
```

---

## **8. Advantages of Recursion**

* Simplifies **code readability** for complex problems.
* Suitable for problems that can be **divided into similar subproblems**.
* Essential for working with **trees, graphs, and backtracking algorithms**.

---

## **9. Disadvantages of Recursion**

* Can lead to **stack overflow** if recursion is too deep.
* Usually **slower** than iterative solutions due to function call overhead.
* Uses more **memory** because of the call stack.

---

## **10. Notes / Tips**

* Always define a **base case**.
* Ensure each recursive call **reduces the problem size**.
* Consider **memoization** to optimize recursion (like in Fibonacci).
* Use recursion only when it **simplifies the problem**, otherwise iterative solutions may be faster.
