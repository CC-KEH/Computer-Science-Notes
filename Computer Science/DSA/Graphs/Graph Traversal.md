
### Depth-First Search (DFS)

- **Definition**:
  - DFS is a graph traversal algorithm that explores as far as possible along a branch before backtracking. It uses a stack or recursion to keep track of visited nodes.

- **Key Points**:
  - DFS can be used to find connected components, detect cycles, and solve problems involving depth-related exploration.
  - It can be implemented using either recursion or an explicit stack data structure.

- **Algorithm**:
  - Start at an initial node.
  - Explore one of its unvisited neighbors.
  - Repeat the process recursively (or using a stack) until you reach a leaf node.
  - Backtrack if necessary and explore other branches.
  - Mark visited nodes to avoid revisiting them.

- **Pseudocode (Recursive)**:

```python
   DFS(node):
       if node is not visited:
           mark node as visited
           for each neighbor of node:
               DFS(neighbor)
```

- **Example**:
  - DFS can be used to find a path between two nodes in a maze, explore all connected components of a graph, or perform topological sorting.

### Breadth-First Search (BFS)

- **Definition**:
  - BFS is a graph traversal algorithm that explores all the neighbors of a node before moving on to their neighbors. It uses a queue data structure to ensure nodes are visited in a breadth-first manner.

- **Key Points**:
  - BFS is used for finding the shortest path, connectivity, and exploring nodes level by level.
  - It guarantees the shortest path in unweighted graphs.

- **Algorithm**:
  - Start at an initial node.
  - Add it to the queue.
  - Dequeue the front node and explore its unvisited neighbors.
  - Enqueue these neighbors.
  - Continue until the queue is empty.

- **Pseudocode**:

```python
   BFS(start):
       initialize queue
       enqueue start node
       while queue is not empty:
           node = dequeue()
           mark node as visited
           for each neighbor of node:
               if neighbor is not visited:
                   enqueue neighbor
```

- **Example**:
  - BFS can be used to find the shortest path in a maze, determine if a graph is bipartite, or perform level-order traversal in a tree.

### Comparison

- **DFS vs. BFS**:
  - DFS is often used when you want to explore as deeply as possible before backtracking, while BFS is used for exploring nodes level by level.
  - DFS can be implemented recursively, which can be elegant but might lead to stack overflow errors for very deep graphs. BFS is implemented iteratively using a queue.
  - DFS is used for topological sorting, while BFS is used for shortest path algorithms.
  - In terms of memory, DFS may use less memory compared to BFS for very deep graphs.

- **Applications**:
  - DFS is suitable for tasks like maze solving, cycle detection, and finding strongly connected components.
  - BFS is suitable for finding shortest paths, checking bipartiteness, and exploring networks.
