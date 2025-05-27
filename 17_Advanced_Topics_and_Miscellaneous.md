# 17. Advanced Topics & Miscellaneous (Randomized, Approximation, etc.)

---

## 1. Randomized Algorithms

Randomized algorithms use random numbers to influence their behavior and can offer better average performance or simplicity compared to deterministic algorithms.

### Types

- **Las Vegas Algorithms**: Always produce correct results; runtime varies (e.g., Randomized QuickSort).
- **Monte Carlo Algorithms**: May produce incorrect results with some (usually small) probability; runtime is fixed (e.g., Randomized Primality Testing).

### Examples

- **Randomized QuickSort**: Selects a random pivot to avoid worst-case input.  
  - Expected Time Complexity: O(n log n)
- **Randomized Primality Test**: Miller-Rabin, Fermat's test.
- **Hashing with Randomization**: Universal hashing to reduce collisions.

---

## 2. Approximation Algorithms

Used for NP-hard problems where finding the exact solution is infeasible. Approximation algorithms provide near-optimal solutions with guaranteed bounds.

### Key Concepts

- **Approximation Ratio**: The ratio between the value of the approximate solution and the value of the optimal solution.
- **Polynomial-Time Approximation Scheme (PTAS)**: For any ε > 0, gives (1+ε)-approximate solution in poly-time.
- **Fully Polynomial-Time Approximation Scheme (FPTAS)**: PTAS with runtime polynomial in both input size and 1/ε.

### Examples

- **Vertex Cover**: 2-approximation using a simple greedy approach.
- **Metric TSP**: Christofides’ algorithm gives a 1.5-approximation.
- **Set Cover**: Greedy algorithm gives an O(log n)-approximation.

---

## 3. Online Algorithms

Algorithms that process input piece-by-piece, without knowledge of the future. Performance is measured by the **competitive ratio**.

### Examples

- **Caching (Paging)**: Least Recently Used (LRU), FIFO.
- **Online Bipartite Matching**.

---

## 4. Amortized Analysis

Amortized analysis provides the average time per operation over a sequence, even if single operations might be expensive.

### Examples

- **Dynamic Array Resize**: Occasional costly resize, but O(1) amortized insertion.
- **Incrementing a Binary Counter**: O(1) amortized per increment.

---

## 5. Probabilistic Data Structures

Use randomness to achieve space/time efficiency with probabilistic guarantees.

### Examples

- **Bloom Filters**: Space-efficient, probabilistic set membership testing (false positives possible, no false negatives).
- **Skip Lists**: Probabilistic alternative to balanced trees (O(log n) expected time).

---

## 6. Parallel and Distributed Algorithms

Algorithms designed to run on multiple processors/cores or machines.

### Examples

- **MapReduce**: For massive data processing.
- **Parallel BFS/DFS**: For large graphs.

---

## 7. External Memory and Cache-Efficient Algorithms

- **External Sorting**: Merge sort adapted for huge datasets.
- **Blocking Techniques**: Reduce cache misses.

---

## Tips for Interviews

- Know when randomization, approximation, or online approaches are appropriate.
- Understand how to prove approximation ratios.
- Be ready to discuss pros/cons of probabilistic data structures.
- Recognize real-world scenarios where these techniques are useful (big data, streaming, etc.).

---

## Common Interview Questions

1. What is a randomized algorithm? Give an example.
2. Explain the concept of approximation ratio.
3. How does a bloom filter work?
4. What is amortized analysis? Give an example.
5. Describe an online algorithm with a use-case.
6. How can you process data that does not fit into memory?

---

## Quick Revision Table

| Topic            | Example/Algorithm      | Key Property            |
|------------------|-----------------------|-------------------------|
| Randomized       | QuickSort, Hashing    | Uses random choices     |
| Approximation    | Vertex Cover, TSP     | Near-optimal solution  |
| Online           | LRU Cache             | Processes sequentially  |
| Amortized        | Dynamic Array         | Avg. over sequences    |
| Probabilistic DS | Bloom Filter, SkipList| Probabilistic accuracy  |
| Parallel         | MapReduce             | Multiple processors     |

---

## References

- [GeeksforGeeks: Randomized Algorithms](https://www.geeksforgeeks.org/randomized-algorithms/)
- [Approximation Algorithms (Stanford)](https://web.stanford.edu/class/cs161/lectures/approximation.pdf)
- [Wikipedia: Probabilistic Data Structure](https://en.wikipedia.org/wiki/Probabilistic_data_structure)
- [Online Algorithms (Competitive Ratio)](https://en.wikipedia.org/wiki/Competitive_analysis_(online_algorithm))

---

Happy Learning! 🚀
