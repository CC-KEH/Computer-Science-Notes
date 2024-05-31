## Introduction
A queue is a linear data structure that follows the First In First Out (FIFO) principle. This means that the first element added to the queue will be the first one to be removed. Queues are commonly used in scenarios where order needs to be preserved, such as task scheduling, handling requests in a web server, and breadth-first search (BFS) in graphs.

## How Queues Work
Queues work by allowing two primary operations:
1. **Enqueue**: Add an element to the end of the queue.
2. **Dequeue**: Remove the element from the front of the queue.

## Important Functions in Python

In Python, queues can be implemented using lists, the `collections.deque` class, or the `queue` module.

```python
# Using list as a queue (not efficient for dequeue operations)
queue = []
# Enqueue operation
queue.append(1)
queue.append(2)
queue.append(3)
# Dequeue operation
print(queue.pop(0))  # Output: 1
# Front operation
print(queue[0])  # Output: 2
# isEmpty operation
print(len(queue) == 0)  # Output: False


# Using collections.deque as a queue
from collections import deque
queue = deque()
# Enqueue operation
queue.append(1)
queue.append(2)
queue.append(3)
# Dequeue operation
print(queue.popleft())  # Output: 1
# Front operation
print(queue[0])  # Output: 2
# isEmpty operation
print(len(queue) == 0)  # Output: False


# Using queue module
import queue
q = queue.Queue()
# Enqueue operation
q.put(1)
q.put(2)
q.put(3)
# Dequeue operation
print(q.get())  # Output: 1
# Front operation
print(q.queue[0])  # Output: 2
# isEmpty operation
print(q.empty())  # Output: False
```

## Important Functions in C++

In C++, queues can be implemented using the `queue` container from the Standard Template Library (STL).

```cpp
#include <iostream>
#include <queue>
using namespace std;

int main() {
    queue<int> q;
    // Enqueue operation
    q.push(1);
    q.push(2);
    q.push(3);
    // Dequeue operation
    cout << q.front() << endl;  // Output: 1
    q.pop();
    // Front operation
    cout << q.front() << endl;  // Output: 2
    // isEmpty operation
    cout << (q.empty() ? "Queue is empty" : "Queue is not empty") << endl;  // Output: Queue is not empty
    return 0;
}
```

## Important Patterns to Identify Queues
1. **Level-Based Traversal**: The problem involves processing nodes or elements level by level (e.g., BFS, level order traversal of a tree).
2. **FIFO Requirement**: You need to process elements in the order they arrive (e.g., scheduling tasks, managing requests).
3. **Sliding Window**: The problem involves maintaining a fixed-size window of elements and processing it as it slides through the collection (e.g., finding maximum in a sliding window).
4. **Multi-Producer/Multi-Consumer**: Synchronizing between multiple producers and consumers, ensuring data is processed in the order it was produced.
5. **Round Robin**: Allocating resources or time slices in a cyclic manner (e.g., round-robin scheduling in operating systems).

---

#### [[Stacks|Back]]                                                                                                                               [[Linked List| Next]]
