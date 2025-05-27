# 4. Recurrences and Master Theorem

---

## What is a Recurrence Relation?

A **recurrence relation** expresses the running time of a recursive algorithm in terms of its running time on smaller inputs.  
It’s an equation or inequality that describes a function in terms of its value on smaller inputs.

---

### Example

- **Binary Search:**  
  T(n) = T(n/2) + c  
  (Where c is the constant time for comparison and splitting)

- **Merge Sort:**  
  T(n) = 2T(n/2) + cn  
  (Divide into two subproblems of size n/2, merge takes linear time)

---

## Why Solve Recurrences?

- To determine the time complexity of recursive algorithms.
- Many divide-and-conquer and dynamic programming algorithms are naturally represented by recurrences.

---

## Methods to Solve Recurrences

1. **Substitution Method:**  
   Guess the solution and then use induction to prove it.

2. **Recursion Tree Method:**  
   Visualize the recurrence as a tree and sum the work at each level.

3. **Master Theorem:**  
   Provides a shortcut to get asymptotic bounds for recurrences of a specific form.

---

## Master Theorem

The **Master Theorem** is a direct way to find the time complexity for recurrences of the form:

```
T(n) = aT(n/b) + f(n)
```
Where:  
- **a** = number of subproblems in the recursion  
- **n/b** = size of each subproblem  
- **f(n)** = cost of work done outside the recursive calls (divide/merge/combine steps)

---

### Cases of Master Theorem

Let **k = log_b(a)**

1. **Case 1:** If f(n) = O(n^c) where c < k  
   **T(n) = Θ(n^k)**
2. **Case 2:** If f(n) = Θ(n^k)  
   **T(n) = Θ(n^k * log n)**
3. **Case 3:** If f(n) = Ω(n^c) where c > k and regularity condition holds  
   **T(n) = Θ(f(n))**

---

### Examples

- **Merge Sort:**  
  T(n) = 2T(n/2) + cn  
  a = 2, b = 2, f(n) = Θ(n)  
  k = log₂2 = 1, f(n) = Θ(n^1)  
  → Case 2 ⇒ T(n) = Θ(n log n)

- **Binary Search:**  
  T(n) = T(n/2) + c  
  a = 1, b = 2, f(n) = Θ(1)  
  k = log₂1 = 0, f(n) = Θ(1)  
  → Case 2 ⇒ T(n) = Θ(log n)

- **Strassen’s Matrix Multiplication:**  
  T(n) = 7T(n/2) + Θ(n²)  
  a = 7, b = 2, f(n) = Θ(n²)  
  k = log₂7 ≈ 2.81, f(n) = O(n²) (c < k)  
  → Case 1 ⇒ T(n) = Θ(n^log₂7) ≈ Θ(n^2.81)

---

## When Not to Use Master Theorem

- The recurrence is not in the required form (e.g., T(n) = T(n-1) + T(n-2) + O(1))
- Subproblems are of different sizes
- a or b are not constants

---

## Common Interview Questions

1. What is a recurrence relation? Provide an example.
2. State the Master Theorem and its cases.
3. Use the Master Theorem to solve T(n) = 3T(n/2) + n.
4. Why can’t you use the Master Theorem on T(n) = T(n-1) + T(n-2)?
5. Explain the recursion tree method briefly.

---

## Quick Revision Table

| Recurrence                         | a | b | f(n)      | Case | Complexity         |
|-------------------------------------|---|---|-----------|------|--------------------|
| T(n) = 2T(n/2) + n                 | 2 | 2 | n         | 2    | Θ(n log n)         |
| T(n) = T(n/2) + 1                  | 1 | 2 | 1         | 2    | Θ(log n)           |
| T(n) = 4T(n/2) + n²                | 4 | 2 | n²        | 2    | Θ(n² log n)        |
| T(n) = 7T(n/2) + n²                | 7 | 2 | n²        | 1    | Θ(n^2.81)          |

---

## References

- [GeeksforGeeks: Master Theorem](https://www.geeksforgeeks.org/analysis-algorithms-set-4-master-method-solving-recurrences/)
- [MIT OCW: Recurrences & Master Theorem](https://ocw.mit.edu/courses/6-006-introduction-to-algorithms-fall-2011/resources/lecture-2-models-of-computation/)
- [Wikipedia: Recurrence Relation](https://en.wikipedia.org/wiki/Recurrence_relation)

---

Happy Learning! 🚀
