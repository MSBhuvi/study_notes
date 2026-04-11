# File Handling

File handling is the process of creating, reading, writing, and managing files using a programming language like Python.

It allows data to be stored permanently (in files) instead of temporarily (in RAM).



# 📂 1. Introduction to File Handling

File handling is used to store and retrieve data permanently from files instead of memory.

**Key operations:**

* Open file
* Read file
* Write file
* Append file
* Close file

---

# 📂 2. Opening a File

### Syntax:

```python
open("filename", "mode")
```

### Example:

```python
file = open("data.txt", "r")
```

---

# 📂 3. File Modes

| Mode | Description       |
| ---- | ----------------- |
| `r`  | Read              |
| `w`  | Write (overwrite) |
| `a`  | Append            |
| `x`  | Create new file   |
| `b`  | Binary mode       |
| `t`  | Text mode         |
| `r+` | Read + Write      |

---

# 📂 4. Closing a File

```python
file = open("data.txt", "r")
file.close()
```

👉 Important to avoid memory leaks.

---

# 📂 5. Reading Files

### 5.1 Read full content

```python
with open("data.txt", "r") as f:
    print(f.read())
```

### 5.2 Read line

```python
with open("data.txt", "r") as f:
    print(f.readline())
```

### 5.3 Read all lines

```python
with open("data.txt", "r") as f:
    print(f.readlines())
```

### 5.4 Loop through file

```python
with open("data.txt", "r") as f:
    for line in f:
        print(line.strip())
```

---

# 📂 6. Writing Files

### 6.1 Write (overwrite)

```python
with open("data.txt", "w") as f:
    f.write("Hello\n")
```

### 6.2 Write multiple lines

```python
lines = ["Line1\n", "Line2\n"]

with open("data.txt", "w") as f:
    f.writelines(lines)
```

---

# 📂 7. Appending Data

```python
with open("data.txt", "a") as f:
    f.write("New Line\n")
```

👉 Does NOT delete existing content.

---

# 📂 8. Using `with` Statement (Best Practice)

```python
with open("data.txt", "r") as f:
    data = f.read()
```

✔ Automatically closes file
✔ Cleaner and safer

---

# 📂 9. File Pointer Operations

```python
with open("data.txt", "r") as f:
    print(f.tell())   # Current position
    f.seek(0)         # Move to beginning
```

---

# 📂 10. File Attributes

```python
file = open("data.txt", "r")

print(file.name)
print(file.mode)
print(file.closed)

file.close()
```

---

# 📂 11. Binary File Handling

Used for images, videos, etc.

```python
with open("image.jpg", "rb") as f:
    data = f.read()
```

---

# 📂 12. File Existence & Deletion

```python
import os

if os.path.exists("data.txt"):
    os.remove("data.txt")
```

---

# 📂 13. Creating a File

```python
with open("newfile.txt", "x") as f:
    pass
```

---

# 📂 14. Exception Handling

```python
try:
    with open("data.txt", "r") as f:
        print(f.read())
except FileNotFoundError:
    print("File not found")
```

---

# 📂 15. Working with Paths

### Problem:

```python
open("C:\Users\file.txt")
```

### Solution:

```python
open(r"C:\Users\file.txt")
```

OR

```python
open("C:\\Users\\file.txt")
```

---

# 📂 16. Practical Example (Mini Program)

```python
import os

# Write
with open("sample.txt", "w") as f:
    f.write("Glass Count: 100\n")

# Read
with open("sample.txt", "r") as f:
    print(f.read())

# Append
with open("sample.txt", "a") as f:
    f.write("Pallet ID: P001\n")

# Delete
if os.path.exists("sample.txt"):
    os.remove("sample.txt")
```

---

# 📂 17. Best Practices

* Use `with open()` ✔
* Handle exceptions ✔
* Use correct mode ✔
* Avoid hardcoding paths ✔
* Close files properly ✔

---

# 📂 18. Interview Questions (Important)

* Difference between `read()`, `readline()`, `readlines()`
* Difference between `w` and `a`
* What is file pointer?
* Why use `with` statement?
* What is binary mode?

---

If you want next level, I can:

* Build **real project: glass count system (file + database style)**
* Or give **MCQs + test questions for practice**
