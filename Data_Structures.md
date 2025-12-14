# **Data Structures in Python**

Data structures are **ways to organize, store, and manage data** efficiently in a program. Python provides **built-in structures** and allows implementation of **classic data structures**.

---

## **1. Linear Data Structures**

### **A. List / Array**

**Definition:**
A collection of elements stored in a **sequential order**. Lists in Python are **dynamic arrays**.

**Key Points:**

* Ordered collection
* Mutable
* Allows duplicates
* Index-based access

**Example:**

```python
# Python list
arr = [1, 2, 3, 4, 5]
arr.append(6)
arr[0] = 0
print(arr)  # Output: [0, 2, 3, 4, 5, 6]
```

---

### **B. Stack**

**Definition:**
A stack is a **Last-In-First-Out (LIFO)** data structure.

**Key Points:**

* Insert (push) and remove (pop) from **top**
* Can be implemented using **list** or **`collections.deque`**

**Example:**

```python
stack = []
stack.append(1)  # push
stack.append(2)
stack.pop()      # remove top
```

---

### **C. Queue**

**Definition:**
A queue is a **First-In-First-Out (FIFO)** data structure.

**Key Points:**

* Insert (enqueue) at rear, remove (dequeue) from front
* Implementable using **`collections.deque`**

**Example:**

```python
from collections import deque

queue = deque()
queue.append(1)  # enqueue
queue.append(2)
queue.popleft()   # dequeue
```

---

### **D. Linked List**

**Definition:**
A linked list is a **linear collection of nodes**, where each node points to the next.

**Key Points:**

* Dynamic size
* Efficient insertion/deletion
* Can be singly or doubly linked

**Example:**

```python
class Node:
    def __init__(self, data):
        self.data = data
        self.next = None

class LinkedList:
    def __init__(self):
        self.head = None

    def append(self, data):
        new_node = Node(data)
        if not self.head:
            self.head = new_node
            return
        last = self.head
        while last.next:
            last = last.next
        last.next = new_node

ll = LinkedList()
ll.append(10)
ll.append(20)
```

---

## **2. Non-Linear Data Structures**

### **A. Tree**

**Definition:**
A tree is a **hierarchical data structure** with nodes connected by edges. The top node is called the **root**.

**Key Points:**

* Each node can have multiple children
* Binary Tree: max two children per node
* Useful in **hierarchies, search operations, and decision-making**

**Example: Binary Tree**

```python
class Node:
    def __init__(self, data):
        self.data = data
        self.left = None
        self.right = None

root = Node(1)
root.left = Node(2)
root.right = Node(3)
root.left.left = Node(4)
```

---

### **B. Binary Search Tree (BST)**

**Definition:**
A BST is a **binary tree** where left child < parent < right child.

**Key Points:**

* Efficient search, insert, delete
* In-order traversal gives **sorted order**

**Example:**

```python
class BSTNode:
    def __init__(self, data):
        self.data = data
        self.left = None
        self.right = None

def insert(root, key):
    if not root:
        return BSTNode(key)
    if key < root.data:
        root.left = insert(root.left, key)
    else:
        root.right = insert(root.right, key)
    return root

root = BSTNode(10)
insert(root, 5)
insert(root, 15)
```

---

### **C. Graph (Optional Advanced)**

**Definition:**
A graph is a set of **nodes (vertices) connected by edges**.

**Key Points:**

* Can be directed/undirected
* Represented using **adjacency list** or **matrix**

**Example:**

```python
graph = {
    "A": ["B", "C"],
    "B": ["A", "D"],
    "C": ["A", "D"],
    "D": ["B", "C"]
}
```

---

## **3. Notes**

* **Linear structures** store data sequentially (Lists, Stacks, Queues, Linked Lists)
* **Non-linear structures** store data hierarchically or graph-based (Trees, Graphs)
* Choose a structure based on **operation types** (search, insert, delete) and **efficiency requirements**
* Python’s **built-in structures** (list, deque, dict, set) cover most use cases, but implementing classic structures helps in **learning and interviews**

---
