# **Comprehensive Guide to Data Structures in Python**

## Introduction

Understanding data structures is crucial for efficient problem-solving in programming. Data structures help us organize and manage data efficiently, allowing for optimized storage, access, and modification. Below is a guide to commonly used data structures in Python, complete with explanations, examples, time and space complexities, and practical use cases.

---

## 1. **Array (List in Python)**

### **Introduction:**
An array is a collection of elements, each identified by an index or a key. In Python, arrays are implemented as lists. Lists allow for fast indexing, making them ideal for random access.

### **Time and Space Complexity:**

| Operation        | Time Complexity | Space Complexity |
|------------------|-----------------|------------------|
| Access           | O(1)            | O(1)             |
| Append           | O(1)            | O(1)             |
| Insert/Delete    | O(n)            | O(n)             |
| Search           | O(n)            | O(1)             |

### **Usage Example:**
```python
arr = [1, 2, 3, 4]
arr.append(5)         # Adds 5 to the end
arr.insert(1, 10)     # Inserts 10 at index 1
arr.pop()             # Removes and returns the last item
arr.remove(2)         # Removes the first occurrence of 2
print(arr[0])         # Access first element

**### Use Case:**
Arrays are ideal for storing ordered data, like a list of students’ grades, or when you need fast random access and iteration over data.
