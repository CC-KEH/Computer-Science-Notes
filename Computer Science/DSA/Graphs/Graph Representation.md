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

6. **Compressed Sparse Row (CSR) or Compressed Sparse Column (CSC)**:
   - **Description**: These representations are used for large sparse graphs, efficiently storing graph information.
   - **Example**: 
     These representations are not typically shown directly with examples but are data structures optimized for sparse graphs to save memory.

7. **Graph Database**:
   - **Description**: Graph databases like Neo4j or Amazon Neptune store graph data in specialized data structures and allow for efficient querying.
   - **Example**: 
     A social network might use a graph database to represent user profiles and their relationships.

8. **Object-Oriented Representation**:
   - **Description**: Custom classes for vertices and edges are created, allowing for flexibility and customization.
   - **Example**: 
     In Python, you can create a `Vertex` class with properties like name and a list of neighbors. Edges can be represented as instances of an `Edge` class.

9. **Property Graph**:
   - **Description**: Property graphs associate properties or attributes with nodes and edges.
   - **Example**:
     In a recommendation system, you might have a user node with properties like name and age, and an edge representing "likes" with properties like "timestamp" and "rating."

10. **Spatial Data Structures (e.g., Quadtree or R-tree)**:
    - **Description**: These structures are used for spatial or geographical applications where nodes represent geographical areas, and edges represent spatial relationships.
    - **Example**: 
      In geographic information systems (GIS), a quadtree can be used to represent hierarchical divisions of a region.

11. **GraphML and other Serialization Formats**:
    - **Description**: These formats are used for storing and exchanging graph data between applications.
    - **Example**: 
      A graph of web page links can be saved in GraphML format with nodes representing web pages and edges representing links between them.

12. **3D Graph Representation**:
    - **Description**: In 3D representations, nodes and edges are used to model 3D structures and relationships.
    - **Example**: 
      In computer graphics, a 3D mesh can be represented as a graph where nodes are vertices in 3D space, and edges connect them to form faces.
