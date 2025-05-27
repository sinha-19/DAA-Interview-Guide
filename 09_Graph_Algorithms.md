# 9. Graph Algorithms (BFS, DFS, Shortest Path, MST, etc.)

---

## What is a Graph?

A **graph** is a collection of **nodes** (vertices) and **edges** (connections) between them.  
Graphs can be **directed** or **undirected**, **weighted** or **unweighted**, **cyclic** or **acyclic**.

---

## Common Graph Representations

- **Adjacency Matrix:** 2D array, O(V²) space.
- **Adjacency List:** Array/list of lists, O(V + E) space.

---

## Traversal Algorithms

### 1. Breadth-First Search (BFS)

- Explores nodes in all directions, level by level.
- Uses a queue (FIFO).
- Finds shortest path in unweighted graphs.
- **Time Complexity:** O(V + E)
- **Applications:** Shortest path, finding connected components, bipartite check.

**Pseudocode:**
```python
def BFS(graph, start):
    visited = set()
    queue = [start]
    while queue:
        node = queue.pop(0)
        if node not in visited:
            visited.add(node)
            queue.extend(neighbor for neighbor in graph[node] if neighbor not in visited)
```

---

### 2. Depth-First Search (DFS)

- Explores as far as possible along each branch before backtracking.
- Uses a stack (can be implemented recursively).
- **Time Complexity:** O(V + E)
- **Applications:** Cycle detection, topological sort, connected components.

**Pseudocode:**
```python
def DFS(graph, node, visited=set()):
    if node not in visited:
        visited.add(node)
        for neighbor in graph[node]:
            DFS(graph, neighbor, visited)
```

---

## Shortest Path Algorithms

### 1. Dijkstra’s Algorithm

- Finds shortest path from a source node to all others in a weighted graph (no negative weights).
- Uses a priority queue.
- **Time Complexity:** O((V + E) log V) with min-heap.

### 2. Bellman-Ford Algorithm

- Handles negative weights.
- **Time Complexity:** O(VE)
- Detects negative cycles.

### 3. Floyd-Warshall Algorithm

- All-pairs shortest path.
- **Time Complexity:** O(V³)

---

## Minimum Spanning Tree (MST) Algorithms

### 1. Kruskal’s Algorithm

- Greedily adds lowest-weight edge without creating cycles.
- Uses Union-Find data structure.
- **Time Complexity:** O(E log V)

### 2. Prim’s Algorithm

- Grows MST from a starting vertex, always adding the smallest-weight edge.
- **Time Complexity:** O(E log V)

---

## Other Important Graph Algorithms

- **Topological Sort:** For Directed Acyclic Graphs (DAGs).
- **Connected Components:** Find clusters in the graph (BFS/DFS).
- **Cycle Detection:** Detects if a graph contains cycles (BFS/DFS).
- **Bipartite Check:** Checks if a graph can be colored with two colors.

---

## Applications

- Social networks, navigation/maps, scheduling, circuit design, networking, recommendation systems, etc.

---

## Quick Revision Table

| Algorithm           | Problem Solved                 | Time Complexity     |
|---------------------|-------------------------------|--------------------|
| BFS                 | Traversal, shortest path (unweighted) | O(V + E)   |
| DFS                 | Traversal, cycle detection     | O(V + E)           |
| Dijkstra            | Shortest path (weighted, +ve) | O((V+E) log V)     |
| Bellman-Ford        | Shortest path (neg weights)   | O(VE)              |
| Floyd-Warshall      | All-pairs shortest path       | O(V³)              |
| Kruskal             | Minimum Spanning Tree         | O(E log V)         |
| Prim                | Minimum Spanning Tree         | O(E log V)         |
| Topological Sort    | Ordering in DAG               | O(V + E)           |

---

## Common Interview Questions

1. How do you represent a graph in code?
2. What’s the difference between BFS and DFS? When to use which?
3. How does Dijkstra’s algorithm work? What if there are negative weights?
4. Explain how to find Minimum Spanning Tree.
5. Give real-world applications for graph algorithms.

---

## References

- [GeeksforGeeks: Graph Data Structure and Algorithms](https://www.geeksforgeeks.org/graph-data-structure-and-algorithms/)
- [MIT OCW: Graph Algorithms](https://ocw.mit.edu/courses/6-006-introduction-to-algorithms-fall-2011/resources/lecture-12-graphs/)
- [Wikipedia: Graph Theory](https://en.wikipedia.org/wiki/Graph_theory)

---

Happy Learning! 🚀
