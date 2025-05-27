# 6. Greedy Algorithms

---

## What is a Greedy Algorithm?

A **greedy algorithm** is an approach for solving optimization problems by making the locally optimal choice at each stage with the hope of finding a global optimum.  
Greedy algorithms do not always yield the best solution for every problem, but for many problems, they do provide optimal or near-optimal solutions efficiently.

---

## How Greedy Algorithms Work

1. **Make a choice that looks best at the moment (greedy choice).**
2. **Check if the current choice leads to a solution.**
3. **Repeat the process on the remaining subproblem.**
4. **Once all choices are made, check if the solution is feasible and optimal.**

---

## Characteristics of Greedy Algorithms

- **Greedy Choice Property:** A global optimum can be arrived at by selecting a local optimum.
- **Optimal Substructure:** An optimal solution to the problem contains optimal solutions to its subproblems.

---

## When Does Greedy Work?

- When the problem exhibits both the **greedy choice property** and **optimal substructure**.
- Examples: Minimum Spanning Tree (MST), Huffman coding, Activity selection.

---

## Popular Examples

| Problem                    | Greedy Approach Used            | Time Complexity      |
|----------------------------|---------------------------------|---------------------|
| **Activity Selection**     | Select earliest finishing task  | O(n log n)          |
| **Fractional Knapsack**    | Choose item with highest value/weight | O(n log n)   |
| **Huffman Coding**         | Merge least frequent symbols    | O(n log n)          |
| **Dijkstra’s Algorithm**   | Shortest path by picking minimum distance node | O(V²) or O((V+E) log V) |
| **Prim’s Algorithm**       | MST by growing tree with min edge | O(E log V)        |
| **Kruskal’s Algorithm**    | MST by adding least weight edge | O(E log V)          |

---

## Example: Activity Selection Problem

**Goal:** Select the maximum number of non-overlapping activities.

**Greedy Strategy:** Always pick the next activity that finishes earliest.

**Pseudocode:**
```plaintext
Sort activities by finish time
Select first activity
For each remaining activity:
    if start time >= finish time of last selected:
        select activity
```

---

## Example: Fractional Knapsack

**Goal:** Maximize value in a knapsack of capacity W. Items can be broken.

**Greedy Strategy:** Take item with highest value/weight ratio first.

---

## Advantages

- Simple and easy to implement.
- Efficient for many optimization problems.

## Disadvantages

- Does not always yield the global optimum.
- Must prove greedy choice property and optimal substructure.

---

## Tips for Interviews

- **Identify if greedy works:** Does the problem have greedy choice and optimal substructure?
- **Justify greedy choice:** Be ready to prove correctness.
- **Edge Cases:** Consider both integer and fractional/partial versions of problems.

---

## Common Interview Questions

1. What is a greedy algorithm? Give examples.
2. Why does the greedy approach work for activity selection but not for 0/1 knapsack?
3. Explain the difference between greedy algorithms and dynamic programming.
4. Describe the greedy solution to the fractional knapsack problem.
5. Prove the correctness of Kruskal’s or Prim’s algorithm.

---

## Quick Revision Table

| Problem             | Greedy Choice                          |
|---------------------|----------------------------------------|
| Activity Selection  | Earliest finish time                   |
| Fractional Knapsack | Highest value/weight ratio             |
| Dijkstra’s          | Node with minimum tentative distance   |
| Prim’s              | Minimum weight edge to expand tree     |
| Kruskal’s           | Next lowest-weight edge                |

---

## References

- [GeeksforGeeks: Greedy Algorithms](https://www.geeksforgeeks.org/greedy-algorithms/)
- [CLRS Book: Greedy Algorithms](https://mitpress.mit.edu/9780262046305/introduction-to-algorithms/)
- [Wikipedia: Greedy Algorithm](https://en.wikipedia.org/wiki/Greedy_algorithm)

---

Happy Learning! 🚀
