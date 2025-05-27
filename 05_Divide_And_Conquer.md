# 5. Divide and Conquer

---

## What is Divide and Conquer?

**Divide and Conquer** is a fundamental algorithm design paradigm that works by recursively breaking a problem into two or more subproblems of the same (or related) type, solving them independently, and then combining their solutions to solve the original problem.

---

## Steps in Divide and Conquer

1. **Divide:** Break the problem into smaller subproblems.
2. **Conquer:** Solve each subproblem recursively. If subproblem is small enough, solve it directly (base case).
3. **Combine:** Merge the solutions of the subproblems to get the solution to the original problem.

---

## General Structure (Pseudocode)

```plaintext
Algorithm DivideAndConquer(A, n):
    if n is small:
        Solve directly
    else:
        Divide A into subproblems A1, A2, ..., Ak
        Solve each subproblem recursively
        Combine solutions of subproblems
```

---

## Classic Examples

| Problem           | How D&C is Applied                         | Time Complexity      |
|-------------------|--------------------------------------------|---------------------|
| **Merge Sort**    | Divide array in halves, sort/merge         | O(n log n)          |
| **Quick Sort**    | Partition array, sort partitions           | O(n log n) avg      |
| **Binary Search** | Search one half recursively                | O(log n)            |
| **Matrix Multiplication (Strassen’s)** | Split matrices, combine | O(n^2.81)           |
| **Closest Pair of Points** | Divide points, merge result        | O(n log n)          |

---

## Example: Merge Sort

- **Divide:** Split array into two halves.
- **Conquer:** Recursively sort the two halves.
- **Combine:** Merge the sorted halves.

**Recurrence Relation:**  
T(n) = 2T(n/2) + O(n)  
(Solved using the Master Theorem: T(n) = O(n log n))

---

## Advantages

- **Reduces complexity:** Breaks complex problems into manageable parts.
- **Parallelism:** Subproblems can often be solved in parallel.
- **Optimal for recursive problems:** Many naturally recursive problems fit this pattern.

---

## Disadvantages

- **Overhead:** Recursive calls and combining solutions may add overhead.
- **Space:** May use additional memory (e.g., merge sort uses O(n) extra space).

---

## Tips for Interviews

- Identify if the problem can be divided into similar, smaller subproblems.
- Write the recurrence relation for time complexity.
- Use the Master Theorem to solve the recurrence.
- Discuss base cases and combination logic.

---

## Common Interview Questions

1. What is the divide and conquer approach? Give examples.
2. How does merge sort use divide and conquer?
3. Write and solve the recurrence for binary search.
4. When is divide and conquer less suitable?
5. Compare divide and conquer with dynamic programming.

---

## Quick Revision Table

| Step      | Description                                    |
|-----------|------------------------------------------------|
| Divide    | Break into subproblems                         |
| Conquer   | Solve subproblems (recursively)                |
| Combine   | Merge subproblem solutions                     |

---

## References

- [GeeksforGeeks: Divide and Conquer](https://www.geeksforgeeks.org/divide-and-conquer-algorithm/)
- [MIT OCW: Divide & Conquer](https://ocw.mit.edu/courses/6-006-introduction-to-algorithms-fall-2011/resources/lecture-3-divide-and-conquer/)
- [Wikipedia: Divide and Conquer](https://en.wikipedia.org/wiki/Divide-and-conquer_algorithm)

---

Happy Learning! 🚀
