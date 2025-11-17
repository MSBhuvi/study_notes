# Python Data Structures
## Intoduction
Python provides a rich set of built-in and specialized data structures that allow efficient storage, retrieval, transformation, and organization of data.

## Built-in Data Structures
List

Tuples

sets

Dictionaries

## **List**:

A **list** in Python is a dynamic, mutable, ordered data structure used to store multiple items in a single variable.
It is one of the most commonly used data structures in Python because it is flexible, easy to use, and supports a wide variety of operations.

Python lists:
- Can store **mixed data types**
- Can grow or shrink dynamically
- Are implemented internally as **dynamic arrays** (resizable arrays)

Lists are ideal when you need an ordered, modifiable sequence of elements.

---

**Key Characteristics of Lists**

#### ✔ Ordered
Elements in a list maintain the order in which they are inserted.

```
x = [10, 20, 30]
# index: 0   1   2

#### ✔ Mutable (can be changed)

You can modify elements, append items, delete items, etc.

```
x[1] = 99  # allowed

#### ✔ Allows Duplicate Values

You can store different data types together.

```
x = [10, "hello", 3.14, True]
```

#### ✔ Dynamic Size

Lists grow and shrink automatically as elements are added or removed.

#### ✔ Indexing & Slicing Supported

Allows accessing individual elements or sublists.

```
x = [10, 20, 30, 40, 50]
print(x[2])    # 30
print(x[1:4])  # [20, 30, 40]
```

### Examples of List Usage
#### Creating List

```
numbers = [1, 2, 3, 4]
mixed = [10, "hello", 3.14]
empty = []
```

#### Adding Elements

```
numbers.append(5)        # Add at end
numbers.insert(1, 10)    # Insert 10 at index 1
numbers.extend([6, 7])   # Add multiple items
```

#### Removing Elements

```
numbers.pop()        # Removes last element
numbers.pop(1)       # Removes element at index 1
numbers.remove(3)    # Removes first occurrence of 3
del numbers[0]       # Delete index 0
```
#### Searching

```
if 10 in numbers:
    print("Found")

print(numbers.index(10))   # returns index of 10
```

#### Iteration

```
for n in numbers:
    print(n)
```

#### List Comprehension

```
squares = [x*x for x in range(1, 6)]
```

### Advantages of Lists

✅ 1. Highly Flexible

Can store mixed data types and support multiple operations.

✅ 2. Fast Random Access (O(1))

Indexing is very fast because lists are implemented as dynamic arrays.

✅ 3. Easy to Modify

You can:

add

remove

update

elements easily.

✅ 4. Supports Powerful Built-in Methods

append(), extend(), insert(), remove(), sort(), reverse(), etc.

✅ 5. Dynamic Resizing

The list automatically expands or shrinks as needed.

✅ 6. Great for Iteration

Works smoothly with loops, list comprehensions, and functions like map() or filter().

### Disadvantages of Lists

❌ 1. Slow for Insert/Delete in Middle (O(n))

Because elements must shift to maintain order.

❌ 2. Higher Memory Usage

Since Python lists store references, they consume more memory than arrays in other languages.

❌ 3. Not Type-Safe

Mixed data types can lead to logic errors if not handled carefully.

❌ 4. Searching is O(n)

Linear search is required unless the list is sorted.

❌ 5. Not Efficient for Queue Operations

pop(0) or insert(0, value) is slow because entire list shifts.

### Summary Table

| Feature           | Details                                   |
| ----------------- | ----------------------------------------- |
| Ordered           | Yes                                       |
| Mutable           | Yes                                       |
| Duplicate Allowed | Yes                                       |
| Heterogeneous     | Yes                                       |
| Implementation    | Dynamic Array                             |
| Best Use Cases    | Iteration, random access, general storage |

----

## **Tuple**

A tuple in Python is an immutable, ordered data structure used to store multiple items in a single variable.
Unlike lists, tuples cannot be modified after creation, making them ideal for fixed, secure, and read-only data.

Python tuples:

Cannot be changed after creation (immutable)

Can store mixed data types

Maintain order

Are stored more efficiently than lists

Are commonly used for:

Fixed collections of values

Returning multiple values from functions

Using as dictionary keys (because they are hashable)

Tuples are ideal when you want to protect data from modification and ensure stable, predictable structure.

### Key Characteristics of Tuples

### ✔ Ordered

Tuples preserve the order of elements.

```
t = (10, 20, 30)
# index: 0   1   2
```

### ✔ Immutable (cannot be changed)
You cannot modify, add, or delete elements once created.

```
t = (1, 2, 3)
# t[1] = 99  ❌ Not allowed – TypeError
```

### ✔ Allows Duplicate Values
Tuples can contain repeated values.

```
t = (1, 2, 2, 3)
```

### ✔ Supports Heterogeneous Data
Tuples can store different data types.

```
t = (10, "hello", 3.14, True)
```

### ✔ Indexing & Slicing Supported
You can access individual items or sub-tuples.

```
t = (10, 20, 30, 40, 50)
print(t[2])    # 30
print(t[1:4])  # (20, 30, 40)
```

#### ✔ Hashable (if all elements are hashable)
Tuples can be used as keys in dictionaries.

```
coords = {(10, 20): "Location A"}
```

### Examples of Tuples Usage
#### **Creating Tuples**

```
t1 = (1, 2, 3)
t2 = ("apple", 10, 3.14)
t3 = ()            # empty tuple
t4 = (5,)          # single-element tuple (comma required)
```

#### **Accessing Elements**

```
t = (10, 20, 30)
print(t[0])   # 10
print(t[-1])  # 30
```

#### **Tuple Unpaking**
Useful for returning multiple values.

```
point = (5, 10)
x, y = point
```

#### **Iteration**

```
for item in (1, 2, 3):
    print(item)
```

#### **Membership Test**






