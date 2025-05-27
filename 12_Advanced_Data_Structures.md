# 12. Advanced Data Structures

---

## Why Advanced Data Structures?

Advanced data structures are used when basic structures (arrays, stacks, queues, linked lists, hash tables, trees, graphs) are not efficient or suitable for certain operations or constraints.  
They are crucial for optimizing complex algorithms and solving advanced interview or competitive programming problems.

---

## 1. Heaps

- **Binary Heap:** Complete binary tree; supports efficient min/max retrieval.
  - **Min-Heap:** Parent ≤ children; root is minimum.
  - **Max-Heap:** Parent ≥ children; root is maximum.
  - **Applications:** Priority Queue, Heap Sort, Dijkstra's, Prim's.
  - **Time Complexity:** Insertion/Deletion: O(log n), Peek: O(1)

---

## 2. Balanced Binary Search Trees (BBST)

- Keeps height ≈ log n for fast search, insert, delete.
- **Types:**
  - **AVL Tree:** Strictly balanced, height difference ≤ 1.
  - **Red-Black Tree:** Less strict, used in STL (C++), TreeMap (Java).
- **Time Complexity:** Search/Insert/Delete: O(log n)

---

## 3. Trie (Prefix Tree)

- **Definition:** N-ary tree for storing strings, especially prefixes.
- **Applications:** Autocomplete, dictionary word search, IP routing.
- **Time Complexity:** Insert/Search: O(L) where L = word length

---

## 4. Segment Tree

- **Definition:** Tree for range queries and updates (sum, min, max) on arrays.
- **Applications:** Range Sum/Min/Max Query, Lazy Propagation.
- **Time Complexity:** Build: O(n), Query/Update: O(log n)

---

## 5. Fenwick Tree (Binary Indexed Tree)

- **Definition:** Efficient structure for prefix sums and updates.
- **Applications:** Range sum queries, competitive programming.
- **Time Complexity:** Update/Query: O(log n)

---

## 6. Disjoint Set (Union-Find)

- **Definition:** Partition a set into non-overlapping subsets, supports union and find operations.
- **Applications:** Kruskal's MST, Connected components in graphs.
- **Optimizations:** Path compression, union by rank.
- **Time Complexity:** O(α(n)), where α is the inverse Ackermann function (almost constant).

---

## 7. Suffix Tree & Suffix Array

- **Suffix Tree:** Compressed trie of all suffixes of a string.
- **Suffix Array:** Sorted array of all suffixes’ start indices.
- **Applications:** String matching, bioinformatics, substring queries.
- **Time Complexity:** Build: O(n) (advanced algorithms)

---

## 8. LRU Cache (LinkedHashMap, Doubly Linked List + Hash Map)

- **Definition:** Stores most recently used items; supports O(1) get and put.
- **Applications:** Caching, memory management.

---

## Quick Revision Table

| Data Structure   | Best Use Case           | Typical Operations/Complexity          |
|------------------|------------------------|----------------------------------------|
| Heap             | Priority Queue         | Insert/Delete: O(log n), Peek: O(1)    |
| AVL/Red-Black    | Ordered Map/Set        | Search/Insert/Delete: O(log n)         |
| Trie             | Prefix search          | Insert/Search: O(L), L = word length   |
| Segment Tree     | Range Query/Update     | Build: O(n), Query/Update: O(log n)    |
| Fenwick Tree     | Prefix sum             | Update/Query: O(log n)                 |
| Union-Find       | Disjoint Set Queries   | Union/Find: O(α(n))                    |
| Suffix Tree/Array| String search          | Build O(n), Query O(m), m = pattern    |
| LRU Cache        | Recent item caching    | Get/Put: O(1)                          |

---

## Tips for Interviews

- Know when and why to use each structure.
- Be able to code at least heap, trie, union-find, and LRU cache.
- Understand trade-offs: space vs. time, mutable vs. immutable, etc.
- For segment/fenwick trees, be clear about range vs. point queries.

---

## Common Interview Questions

1. Implement a min-heap or a priority queue.
2. Design a trie for autocomplete.
3. Range sum queries using segment/fenwick tree.
4. Find connected components using union-find.
5. Design an LRU cache.

---

## References

- [GeeksforGeeks: Advanced Data Structures](https://www.geeksforgeeks.org/advanced-data-structures/)
- [MIT OCW: Trees, Range Queries](https://ocw.mit.edu/courses/6-006-introduction-to-algorithms-fall-2011/)
- [Wikipedia: Data Structure](https://en.wikipedia.org/wiki/Data_structure)

---

Happy Learning! 🚀
