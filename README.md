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

2. Set
Introduction:
A set is an unordered collection of unique elements. It’s optimized for fast membership tests and prevents duplicate entries.

Time and Space Complexity:
Operation	Time Complexity	Space Complexity
Add/Remove	O(1)	O(1)
Search	O(1)	O(1)
Union/Intersect	O(n)	O(n)

Usage Example:
python
Copy
Edit
s = {1, 2, 3}
s.add(4)
s.remove(2)
print(3 in s)        # True
s1 = {1, 2, 3}
s2 = {2, 3, 4}
print(s1.union(s2))  # {1, 2, 3, 4}
Use Case:
Sets are useful when you need to ensure no duplicates and need fast membership checks, like tracking unique visitors or finding common elements between two collections.

3. Hash Map (Dictionary)
Introduction:
A hash map (or dictionary) stores key-value pairs and allows for efficient access to values based on their associated key.

Time and Space Complexity:
Operation	Time Complexity	Space Complexity
Insert	O(1)	O(1)
Access	O(1)	O(1)
Delete	O(1)	O(1)

Usage Example:
python
Copy
Edit
d = {'a': 1, 'b': 2}
d['c'] = 3
print(d['a'])            # 1
d.pop('b')
print('a' in d)          # True
Use Case:
Hash maps are great for fast lookups, such as counting word frequencies or implementing simple databases where each key is unique.

4. Queue (FIFO)
Introduction:
A queue follows the First-In, First-Out (FIFO) principle, making it ideal for situations where tasks need to be processed in the order they arrive.

Time and Space Complexity:
Operation	Time Complexity	Space Complexity
Enqueue	O(1)	O(1)
Dequeue	O(1)	O(1)

Usage Example:
python
Copy
Edit
from collections import deque
q = deque()
q.append(1)        # Enqueue
q.append(2)
print(q.popleft())  # Dequeue: 1
Use Case:
Queues are commonly used in job scheduling, breadth-first search (BFS) for graphs, or any situation where items need to be processed in order.

5. Stack (LIFO)
Introduction:
A stack operates on the Last-In, First-Out (LIFO) principle. The last element added is the first to be removed, which is useful for backtracking operations.

Time and Space Complexity:
Operation	Time Complexity	Space Complexity
Push	O(1)	O(1)
Pop	O(1)	O(1)

Usage Example:
python
Copy
Edit
stack = []
stack.append(10)     # Push
stack.append(20)
print(stack.pop())    # Pop: 20
Use Case:
Stacks are ideal for problems like expression evaluation (e.g., converting infix to postfix), backtracking algorithms, or maintaining function call stacks.

6. Linked List
Introduction:
A linked list is a collection of nodes where each node contains data and a reference to the next node. It's used when the size of the collection can change dynamically, and frequent insertions/deletions are required.

Time and Space Complexity:
Operation	Time Complexity	Space Complexity
Insert Front	O(1)	O(1)
Insert End	O(n)	O(1)
Search/Delete	O(n)	O(1)

Usage Example:
python
Copy
Edit
class Node:
    def __init__(self, data):
        self.data = data
        self.next = None

class LinkedList:
    def __init__(self):
        self.head = None

    def insert_front(self, data):
        new_node = Node(data)
        new_node.next = self.head
        self.head = new_node
Use Case:
Linked lists are used in applications where data frequently changes, such as real-time editing systems, or for implementing other data structures like stacks and queues.

7. Heap (Min-Heap)
Introduction:
A heap is a binary tree that satisfies the heap property. In a min-heap, the smallest element is at the root, making it useful for efficient priority-based operations.

Time and Space Complexity:
Operation	Time Complexity	Space Complexity
Insert	O(log n)	O(n)
Pop min	O(log n)	O(n)
Peek min	O(1)	O(1)

Usage Example:
python
Copy
Edit
import heapq
heap = []
heapq.heappush(heap, 3)
heapq.heappush(heap, 1)
print(heapq.heappop(heap))  # 1
Use Case:
Heaps are used in algorithms like Dijkstra’s shortest path, for scheduling tasks, or maintaining a running list of the smallest/largest elements.

8. Priority Queue
Introduction:
A priority queue allows elements to be processed based on their priority, not their insertion order. It’s often implemented using a heap.

Time and Space Complexity:
Operation	Time Complexity	Space Complexity
Insert	O(log n)	O(n)
Remove Highest	O(log n)	O(n)

Usage Example:
python
Copy
Edit
import heapq
pq = []
heapq.heappush(pq, (2, "Task A"))
heapq.heappush(pq, (1, "Task B"))
print(heapq.heappop(pq))  # (1, 'Task B')
Use Case:
Priority queues are ideal for algorithms like Dijkstra's shortest path, job scheduling with priorities, and handling tasks in order of their urgency.

9. Deque (Double-Ended Queue)
Introduction:
A deque (double-ended queue) allows fast additions and removals from both ends. It’s more versatile than a regular queue or stack.

Time and Space Complexity:
Operation	Time Complexity	Space Complexity
Append/Pop	O(1)	O(1)
Appendleft/PopLeft	O(1)	O(1)

Usage Example:
python
Copy
Edit
from collections import deque
d = deque()
d.append(1)
d.appendleft(2)
print(d.pop())       # 1
print(d.popleft())   # 2
Use Case:
Deques are perfect for problems where you need access from both ends, such as sliding window problems, palindrome checks, and undo-redo functionality.

