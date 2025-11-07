---
## 1.Looping Statements
A looping statement in Python is a programming structure that allows you to repeat a block of code multiple times —
either a fixed number of times or until a specific condition becomes False.

### Types
**1. `for` loop**

**2. `while` loop**

**3. Nested loop**

#### 1.`for` loop (the most Pythonic loop)
for iterates over any iterable (list, tuple, string, dict, set, file, generator, etc.).

#### Syntax
<p style="center">
<img width="351" height="98" alt="image" src="https://github.com/user-attachments/assets/b5eadfaf-e7e8-4eba-aa50-b8b20e8579da" />
</p>

#### Examples
```
# Example-1
# Write a program to print numbers from 1 to 20 using a for loop.
for i in range(1,20+1):
    print(i)
```

```
# Example-2
# Print all even numbers between 1 and 50.
for i in range(1,50+1):
    if i%2==0:
        print(i)
```

```
# Example-3
# Print all odd numbers between 1 and 30.
for i in range(1,30+1):
    if i%2==1:
        print(i)
```
```
# Example-4
# Find the sum of numbers from 1 to 10.
total=0
for i in range(10+1):
    total=total+i
    
print(total)
```

```
# Example-5
# Print the multiplication table of 5 using a for loop.
# Method-1
table=5
for i in range(10+1):
    product=i*table
    print(f"{i}*{table}={product}")

# Method-2

# Method-3
table=int(input("Enter the table"))
for i in range(10+1):
    print(f"{i}*{table}={i*table}")

```

```
# Example-6
# Print the square of each number from 1 to 10.
for i in range(1,10+1):
    square=i ** 2
    print(f"the square of {i} is {square}")
```

```
# Example-7
# Take a string (e.g., "Python") and print each character on a new line.
text="python"
for i in text:
    print(i)
```

```
# Example-8
# Given a list fruits = ["apple", "banana", "cherry"], print each fruit.
fruits = ["apple", "banana", "cherry"]
for i in fruits:
    print(i)
```

```
# Example-9
# Print numbers from 10 down to 1.
num=10
for i in range(num,0,-1):
    print(i)
```

```
# Example-10
# Count how many vowels are in the string "hello world" using a for loop.
count=0
word="hello world"
vowels="aeiou"
#vowels=['a','e','i','o','u']
for i in word:
    if i in vowels:
        count=count+1

print(count)

```

```














