
# 📚 Stack in Python(for quick revision) – Complete Guide

A **stack** is a linear data structure that follows the **LIFO (Last In First Out)** principle.

---

## 🧱 What is a Stack?
A stack is like a pile of plates: you add to the top and remove from the top. The last item added is the first one to be removed.

---

## ✅ Stack Implementation in Python

### 1. Using Python List (Common & Simple)
```python
stack = []

# Push
stack.append(10)

# Pop
stack.pop()

# Peek
top = stack[-1]

# Check if Empty
is_empty = len(stack) == 0
```

### 2. Using `collections.deque`
```python
from collections import deque

stack = deque()

stack.append(10)
stack.pop()
```

---

## ⚙️ Stack Operations – Time & Space Complexity

| Operation     | Python Code       | Time Complexity | Space Complexity |
|---------------|-------------------|------------------|------------------|
| Push          | `stack.append(x)` | O(1)             | O(1)             |
| Pop           | `stack.pop()`     | O(1)             | O(1)             |
| Peek / Top    | `stack[-1]`       | O(1)             | O(1)             |
| Is Empty      | `len(stack)==0`   | O(1)             | O(1)             |
| Size          | `len(stack)`      | O(1)             | O(1)             |

❗ Avoid using `insert(0, x)` or `pop(0)` – they are O(n).

---

## 🔄 Example: Basic Stack Usage
```python
stack = []
stack.append(1)
stack.append(2)
stack.append(3)

print(stack.pop())   # 3
print(stack[-1])     # 2
```

---

## 🔍 When to Use a Stack?
- Undo/Redo operations
- Expression parsing and evaluation
- Syntax parsing (e.g., balanced parentheses)
- Backtracking algorithms
- Monotonic stack problems (next greater/smaller elements)

---

## 🔚 Summary
- Use `list` or `deque` for stack in Python.
- Stack operations are all **O(1)**.
- Useful in many DSA patterns and problems.

