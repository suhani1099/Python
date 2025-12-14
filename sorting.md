# **Sorting Algorithms in Python**

Sorting is the process of arranging elements in a **specific order** (ascending or descending). Python provides **built-in functions** as well as support for classic **sorting algorithms**.

---

## **1. Bubble Sort**

**Definition:**
Bubble Sort repeatedly swaps adjacent elements if they are in the wrong order.

**Key Points:**

* Simple to implement
* In-place sorting algorithm
* Stable (preserves relative order of equal elements)
* Time Complexity: O(n²)
* Not efficient for large lists

**Python Code:**

```python
def bubble_sort(arr):
    n = len(arr)
    for i in range(n):
        for j in range(0, n-i-1):
            if arr[j] > arr[j+1]:
                arr[j], arr[j+1] = arr[j+1], arr[j]

arr = [5, 2, 9, 1, 5]
bubble_sort(arr)
# arr -> [1, 2, 5, 5, 9]
```

---

## **2. Selection Sort**

**Definition:**
Selection Sort repeatedly selects the minimum (or maximum) element and places it in the correct position.

**Key Points:**

* In-place sorting algorithm
* Not stable
* Time Complexity: O(n²)
* Performs fewer swaps than Bubble Sort

**Python Code:**

```python
def selection_sort(arr):
    n = len(arr)
    for i in range(n):
        min_idx = i
        for j in range(i+1, n):
            if arr[j] < arr[min_idx]:
                min_idx = j
        arr[i], arr[min_idx] = arr[min_idx], arr[i]

arr = [64, 25, 12, 22, 11]
selection_sort(arr)
# arr -> [11, 12, 22, 25, 64]
```

---

## **3. Insertion Sort**

**Definition:**
Insertion Sort builds the sorted list one element at a time by inserting elements into their correct position.

**Key Points:**

* Efficient for small or nearly sorted lists
* Stable sorting algorithm
* In-place sort
* Time Complexity: O(n²)

**Python Code:**

```python
def insertion_sort(arr):
    for i in range(1, len(arr)):
        key = arr[i]
        j = i-1
        while j >=0 and key < arr[j]:
            arr[j+1] = arr[j]
            j -= 1
        arr[j+1] = key

arr = [12, 11, 13, 5, 6]
insertion_sort(arr)
# arr -> [5, 6, 11, 12, 13]
```

---

## **4. Merge Sort**

**Definition:**
Merge Sort is a divide-and-conquer algorithm that splits the list into halves, sorts them recursively, and merges the sorted halves.

**Key Points:**

* Stable sorting algorithm
* Not in-place (requires extra memory)
* Efficient for large lists
* Time Complexity: O(n log n)

**Python Code:**

```python
def merge_sort(arr):
    if len(arr) > 1:
        mid = len(arr)//2
        L = arr[:mid]
        R = arr[mid:]

        merge_sort(L)
        merge_sort(R)

        i = j = k = 0

        while i < len(L) and j < len(R):
            if L[i] < R[j]:
                arr[k] = L[i]
                i += 1
            else:
                arr[k] = R[j]
                j += 1
            k += 1

        while i < len(L):
            arr[k] = L[i]
            i += 1
            k += 1

        while j < len(R):
            arr[k] = R[j]
            j += 1
            k += 1

arr = [38, 27, 43, 3, 9, 82, 10]
merge_sort(arr)
# arr -> [3, 9, 10, 27, 38, 43, 82]
```

---

## **5. Quick Sort**

**Definition:**
Quick Sort is a divide-and-conquer algorithm that partitions the list around a pivot and recursively sorts the sublists.

**Key Points:**

* Usually faster than Merge Sort for average cases
* Can be implemented in-place
* Not stable
* Time Complexity: O(n log n) average, O(n²) worst-case

**Python Code:**

```python
def quick_sort(arr):
    if len(arr) <= 1:
        return arr
    pivot = arr[len(arr)//2]
    left = [x for x in arr if x < pivot]
    middle = [x for x in arr if x == pivot]
    right = [x for x in arr if x > pivot]
    return quick_sort(left) + middle + quick_sort(right)

arr = [10, 7, 8, 9, 1, 5]
arr = quick_sort(arr)
# arr -> [1, 5, 7, 8, 9, 10]
```

---

## **6. Python Built-in Sorting**

**Definition:**
Python provides built-in sorting using `sorted()` (returns new list) and `list.sort()` (in-place).

**Key Points:**

* Stable sort implemented using **Timsort**
* Accepts `reverse=True` for descending order
* Accepts `key` for custom sorting

**Python Code:**

```python
arr = [3, 1, 4, 1, 5, 9, 2]

# Using sorted() - returns a new sorted list
sorted_arr = sorted(arr)

# Using list.sort() - modifies the original list
arr.sort()

# Descending order
arr.sort(reverse=True)

# Custom key example
words = ["apple", "banana", "cherry"]
sorted_words = sorted(words, key=len)
```

---

## **7. Comparison Table of Sorting Algorithms**

| Algorithm       | Time Complexity (Best) | Time Complexity (Average) | Time Complexity (Worst) | Space Complexity | Stable | In-Place |
| --------------- | ---------------------- | ------------------------- | ----------------------- | ---------------- | ------ | -------- |
| Bubble Sort     | O(n)                   | O(n²)                     | O(n²)                   | O(1)             | Yes    | Yes      |
| Selection Sort  | O(n²)                  | O(n²)                     | O(n²)                   | O(1)             | No     | Yes      |
| Insertion Sort  | O(n)                   | O(n²)                     | O(n²)                   | O(1)             | Yes    | Yes      |
| Merge Sort      | O(n log n)             | O(n log n)                | O(n log n)              | O(n)             | Yes    | No       |
| Quick Sort      | O(n log n)             | O(n log n)                | O(n²)                   | O(log n)         | No     | Can be   |
| Python Built-in | O(n)                   | O(n log n)                | O(n log n)              | O(n)             | Yes    | Yes      |

---

## **Notes**

* Use **built-in `sorted()` or `list.sort()`** for most cases — efficient and stable.
* Classic algorithms are useful for **learning and interviews**.
* **Stable sorting** maintains the relative order of equal elements.
* **In-place sorting** saves memory but modifies the original list.

---
