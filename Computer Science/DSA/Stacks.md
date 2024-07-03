## Introduction
A stack is a linear data structure that follows the Last In First Out (LIFO) principle. This means that the last element added to the stack will be the first one to be removed. Stacks are used in various applications, including function call management, expression evaluation, and backtracking algorithms.

## How Stacks Work
Stacks work by allowing two primary operations:
1. **Push**: Add an element to the top of the stack.
2. **Pop**: Remove the top element from the stack.

## Important Functions in Python

In Python, stacks can be implemented using lists or the `collections.deque` class.

```python
# Using list as a stack
stack = []
# Push operation
stack.append(1)
stack.append(2)
stack.append(3)
# Pop operation
print(stack.pop())  # Output: 3
# Peek/Top operation
print(stack[-1])  # Output: 2
# isEmpty operation
print(len(stack) == 0)  # Output: False

# Using collections.deque as a stack
from collections import deque
stack = deque()
# Push operation
stack.append(1)
stack.append(2)
stack.append(3)
# Pop operation
print(stack.pop())  # Output: 3
# Peek/Top operation
print(stack[-1])  # Output: 2
# isEmpty operation
print(len(stack) == 0)  # Output: False
```

## Important Functions in C++

In C++, stacks can be implemented using the `stack` container from the Standard Template Library (STL).

```cpp
#include <iostream>
#include <stack>
using namespace std;

int main() {
    stack<int> s;
    // Push operation
    s.push(1);
    s.push(2);
    s.push(3);
    // Pop operation
    cout << s.top() << endl;  // Output: 3
    s.pop();
    // Peek/Top operation
    cout << s.top() << endl;  // Output: 2
    // isEmpty operation
    cout << (s.empty() ? "Stack is empty" : "Stack is not empty") << endl;  // Output: Stack is not empty
    return 0;
}
```

## Important Patterns to Identify Stacks
1. The problem wants you to keep track of a sequence of operations or states.
2. The problem involves matching or pairing elements (e.g., parentheses, brackets).
3. You need to keep track of elements in a certain order and access the most recent one.
4. The solution requires maintaining a sequence of operations or states (e.g., undo operations).
5. The problem involves processing elements with a certain precedence or associativity (e.g., expression evaluation).
6. There is a need to traverse a data structure (e.g., tree, graph) without using recursion.
7. The task involves calculating ranges or spans based on previous elements.
8. You need to find the next greater or smaller element for each item in a collection.