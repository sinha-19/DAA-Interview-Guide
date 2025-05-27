# 3. Asymptotic Notations (Big O, Omega, Theta)

---

## What are Asymptotic Notations?

Asymptotic notations describe the behavior of an algorithm's time or space complexity as the input size (n) grows toward infinity.  
They help compare algorithms independent of machine, compiler, or implementation.

---

## Common Asymptotic Notations

### 1. Big O Notation (O)

- **Definition:** Describes the upper bound (worst-case) of an algorithm's running time.
- **Interpretation:** "The algorithm takes at most O(f(n)) time for large n."
- **Example:**  
  For Linear Search: O(n) — running time increases linearly with input size.

### 2. Omega Notation (Ω)

- **Definition:** Describes the lower bound (best-case) of an algorithm's running time.
- **Interpretation:** "The algorithm takes at least Ω(g(n)) time for large n."
- **Example:**  
  For Linear Search: Ω(1) — best case, the element is at the start.

### 3. Theta Notation (Θ)

- **Definition:** Describes the tight bound (both upper and lower) of an algorithm.
- **Interpretation:** "The algorithm runs in Θ(h(n)) time for large n."
- **Example:**  
  For Linear Search: Θ(n) — running time is linear in both best and worst cases (on average).

---

## Mathematical Definitions

- **Big O:**  
  An algorithm is O(f(n)) if there are positive constants c and n₀ such that for all n ≥ n₀:  
  T(n) ≤ c × f(n)

- **Omega:**  
  An algorithm is Ω(g(n)) if there are positive constants c and n₀ such that for all n ≥ n₀:  
  T(n) ≥ c × g(n)

- **Theta:**  
  An algorithm is Θ(h(n)) if there are positive constants c₁, c₂, and n₀ such that for all n ≥ n₀:  
  c₁ × h(n) ≤ T(n) ≤ c₂ × h(n)

---

## Example Table

| Algorithm      | Best Case      | Worst Case     | Average Case   |
|----------------|---------------|---------------|---------------|
| Linear Search  | Ω(1)          | O(n)          | Θ(n)          |
| Binary Search  | Ω(1)          | O(log n)      | Θ(log n)      |
| Bubble Sort    | Ω(n)          | O(n²)         | Θ(n²)         |
| Merge Sort     | Ω(n log n)    | O(n log n)    | Θ(n log n)    |

---

## Why Use Asymptotic Notation?

- To **abstract away machine-dependent details**.
- To **focus on dominant terms** and ignore constants/lower-order terms.
- To **compare growth rates** of different algorithms.

---

## Notes

- **Big O** — Most commonly asked in interviews; always mention worst-case unless specified.
- **Theta** — Used for precise/tight bounds.
- **Omega** — Used to show that an algorithm cannot be faster than a certain rate.

---

## Common Interview Questions

1. What is Big O notation? Give an example.
2. What is the difference between O, Ω, and Θ notations?
3. Why do we ignore constants and lower-order terms?
4. What is the asymptotic complexity of merge sort? (Θ(n log n))
5. When do you use each notation in analysis?

---

## Quick Revision Table

| Notation | Meaning          | Bound Type     |
|----------|------------------|---------------|
| O(f(n))  | Upper Bound      | Worst Case    |
| Ω(g(n))  | Lower Bound      | Best Case     |
| Θ(h(n))  | Tight Bound      | Avg/Exact     |

---

## References

- [GeeksforGeeks: Asymptotic Analysis](https://www.geeksforgeeks.org/asymptotic-analysis/)
- [Wikipedia: Big O Notation](https://en.wikipedia.org/wiki/Big_O_notation)
- [CLRS Book: Section 3.1](https://mitpress.mit.edu/9780262046305/introduction-to-algorithms/)

---

Happy Learning! 🚀
