# 🔁 Python Loops – Complete Guide for DSA

This guide covers both **fundamental** and **advanced** Python looping techniques used in solving Data Structures & Algorithms (DSA) problems efficiently.

---

## 🧱 Basic Loop Types

### 🔹 1. For Loop
```python
for i in range(5):
    print(i)
### 2. **While Loop**
i = 0
while i < 5:
    print(i)
    i += 1

### 3. Nested Loop
for i in range(2):
    for j in range(3):
        print(i, j)

### 4. For/While with Else
for i in range(3):
    print(i)
else:
    print("Loop completed!")

### 🔹 5. Break and Continue
# Break
for i in range(5):
    if i == 3:
        break
    print(i)

# Continue
for i in range(5):
    if i == 3:
        continue
    print(i)

### 🔸 6. enumerate() – Index + Value
arr = ['a', 'b', 'c']
for index, value in enumerate(arr):
    print(index, value)

### 🔸 7. zip() – Parallel Iteration
a = [1, 2, 3]
b = ['x', 'y', 'z']
for num, char in zip(a, b):
    print(num, char)

### 🔸 8. Looping through Dictionary
d = {'a': 1, 'b': 2}
for key, value in d.items():
    print(key, value)

### 🔸 9. reversed() – Backward Loop
for i in reversed(range(5)):
    print(i)

### 🔸 10. Looping through Set
unique = set([1, 2, 3])
for val in unique:
    print(val)

### 🔸 11. List Comprehensions
squares = [x*x for x in range(5)]
evens = [x for x in range(10) if x % 2 == 0]

### 🔸 12. Reverse Index Loop
arr = [10, 20, 30]
for i in range(len(arr) - 1, -1, -1):
    print(arr[i])


