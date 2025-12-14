# **FILE HANDLING IN PYTHON**

File handling allows a program to **create, read, write, and manipulate files** on the disk. Python provides built-in functions and modules for working with **text files, binary files, and CSV files**.

---

## **1. Introduction**

* Files are used to **store data permanently**.
* Python supports **reading and writing** text and binary files.
* Using the **`with` statement** ensures files are closed automatically.
* Common file types: **.txt, .csv, .json, .bin**.

---

## **2. Data Files**

* **Text Files**: Store data as plain text (`.txt`).
* **Binary Files**: Store data in bytes (`.bin`, `.jpg`, `.png`).
* **CSV Files**: Comma-separated values, commonly used for tabular data.
* **JSON Files**: Store structured data.
* **Log Files**: Store logs for applications.

---

## **3. Opening and Closing Files**

### **Open a File**

```python
file = open("example.txt", "r")  # modes: r, w, a, r+, x, b, t
```

### **File Modes**

| Mode | Description            |
| ---- | ---------------------- |
| `r`  | Read (default)         |
| `w`  | Write (overwrite file) |
| `a`  | Append                 |
| `x`  | Create new file        |
| `r+` | Read and write         |
| `b`  | Binary mode            |
| `t`  | Text mode (default)    |

### **Close a File**

```python
file.close()
```

### **Using `with` Statement**

```python
with open("example.txt", "r") as file:
    content = file.read()
# file is automatically closed
```

---

## **4. Working with Text Files**

### **Reading Text Files**

```python
# Read entire file
with open("example.txt", "r") as file:
    content = file.read()

# Read line by line
with open("example.txt", "r") as file:
    line = file.readline()

# Read all lines into a list
with open("example.txt", "r") as file:
    lines = file.readlines()
```

### **Writing Text Files**

```python
# Write text (overwrites)
with open("example.txt", "w") as file:
    file.write("Hello World\n")

# Append text
with open("example.txt", "a") as file:
    file.write("New Line\n")

# Write multiple lines
lines = ["Line 1\n", "Line 2\n"]
with open("example.txt", "w") as file:
    file.writelines(lines)
```

### **File Cursor Control**

```python
with open("example.txt", "r") as file:
    file.seek(0)      # move cursor to start
    position = file.tell()  # get current cursor position
```

---

## **5. Standard Input, Output, and Error Streams**

* **`sys.stdin`** → Standard input
* **`sys.stdout`** → Standard output
* **`sys.stderr`** → Standard error

```python
import sys

sys.stdout.write("Hello World\n")
sys.stderr.write("An error occurred\n")
input_text = sys.stdin.readline()
```

---

## **6. Working with Binary Files**

```python
# Reading binary files
with open("image.png", "rb") as file:
    data = file.read()

# Writing binary files
with open("copy.png", "wb") as file:
    file.write(data)
```

* Use `rb` for reading binary
* Use `wb` for writing binary

---

## **7. Working with CSV Files**

```python
import csv

# Writing CSV
with open("data.csv", "w", newline="") as file:
    writer = csv.writer(file)
    writer.writerow(["Name", "Age"])
    writer.writerow(["Alice", 25])

# Reading CSV
with open("data.csv", "r") as file:
    reader = csv.reader(file)
    for row in reader:
        pass
```

* Use **`csv.DictReader`** and **`csv.DictWriter`** for dictionary-based operations.

```python
# DictReader
with open("data.csv", "r") as file:
    reader = csv.DictReader(file)
    for row in reader:
        name = row["Name"]

# DictWriter
with open("data.csv", "w", newline="") as file:
    fieldnames = ["Name", "Age"]
    writer = csv.DictWriter(file, fieldnames=fieldnames)
    writer.writeheader()
    writer.writerow({"Name": "Bob", "Age": 30})
```

---

## **8. File Attributes**

```python
with open("example.txt", "r") as file:
    file.name
    file.mode
    file.closed
```

---

## **9. File Methods**

* `read()`, `readline()`, `readlines()`
* `write()`, `writelines()`
* `seek()`, `tell()`, `close()`

---

## **10. Exception Handling with Files**

```python
try:
    with open("missing.txt", "r") as file:
        content = file.read()
except FileNotFoundError:
    pass
except IOError:
    pass
```

---

## **11. Extra Tips**

* Always use **`with`** to ensure files are closed.
* Text mode is default; use binary mode for images, PDFs, etc.
* For large files, read line by line to save memory.
* Use **`os.path.exists()`** to check file existence.
* CSV files are preferred for **structured tabular data**.

---
