# Lambda Function (Anonymous Function)

A lambda function in Python is a small, anonymous (nameless) function defined using the lambda keyword.
It is typically used for short, simple operations when defining a full function using def is unnecessary.

## Syntax

<p align="center">
  <img width="323" height="42" alt="image" src="https://github.com/user-attachments/assets/46294fc8-42d8-4d49-b998-b039811307c2" />

</p>

It can have any number of arguments.

It can have only one expression (no multiple statements).

The expression is evaluated and returned automatically.


### Normal Function
```
def add(a, b):
    return a + b
```

### Lambda Version

```
add = lambda a, b: a + b
```

### Usage

```
print(add(5, 3))  # Output: 8
```

## When to Use Lambda Functions

**1. map()**

**2. filter()**

**3. sorted()**

## Example

### Square of a number

```
square = lambda x: x * x
print(square(5))
```
### Add two numbers

```
add = lambda a, b: a + b
print(add(10, 20)) 
```
### Using lambda with `map()`

```
nums = [1, 2, 3, 4]
squares = list(map(lambda x: x*x, nums))
print(squares)  # Output: [1, 4, 9, 16]
```

### Using lambda with `filter()`

```
nums = [1, 2, 3, 4, 5, 6]
even = list(filter(lambda x: x % 2 == 0, nums))
print(even)  # Output: [2, 4, 6]
```






















