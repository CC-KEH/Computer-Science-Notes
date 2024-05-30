1. **Adjacency Matrix**:
   - **Description**: An adjacency matrix is a 2D array where each cell (i, j) represents an edge between vertex i and vertex j.
   - **Example**:

```css
    A B C
A   0 1 1
B   1 0 0
C   1 0 0
```

   - In this example, there are edges from A to B, A to C, and B to A. The absence of a 1 in a cell indicates no edge between the respective vertices.

2. **Adjacency List**:
   - **Description**: In an adjacency list representation, each vertex maintains a list of its adjacent vertices.
   - **Example**:

```css
A -> [B, C]
B -> [A]
C -> [A]
```

   - Here, vertex A has edges to vertices B and C, while vertices B and C have edges to vertex A.

3. **Edge List**:
   - **Description**: An edge list stores all edges as pairs of vertices.
   - **Example**:

```css
(A, B), (A, C), (B, A), (C, A)
```

   - This represents the same graph as the previous examples with pairs of vertices indicating edges.

4. **Incidence Matrix**:
   - **Description**: An incidence matrix uses rows for vertices and columns for edges. Each cell (i, j) indicates if vertex i is incident to edge j.
   - **Example**:

```css
    E1 E2
A   1  1
B   1  0
C   0  1
```

   - In this example, vertex A is incident to edges E1 and E2, while vertex B is incident only to E1, and vertex C is incident to E2.

5. **Adjacency Set**:
   - **Description**: In this representation, each vertex maintains a set of its neighbors.
   - **Example**:

```css
A -> {B, C}
B -> {A}
C -> {A}
```

   - It's similar to the adjacency list, but it uses sets to store neighbors, which can help efficiently check for the existence of an edge.

## Graph Representation using Adjacency List
```python
class Graph:
    def __init__(self,Nodes):
        self.nodes = Nodes
        self.graph = {}
        for node in self.nodes:
            self.graph[node] = []

    def addEdge(self,V1,V2,w):
        self.graph[V1].append([V2,w])
        self.graph[V2].append([V1,w])

    def add_directed_Edge(self,V1,V2,w):
        self.graph[V1].append([V2,w])

    def addVertex(self,V):
        if V in self.graph:
            pass
        else:
            self.graph[V]=[]

    def printGraph(self):
        for node in self.nodes:
            print(node,'->',self.graph[node])
```
