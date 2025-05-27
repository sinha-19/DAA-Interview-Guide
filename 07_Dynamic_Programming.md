# 7. Dynamic Programming

---

## What is Dynamic Programming?

**Dynamic Programming (DP)** is an algorithmic technique for solving optimization problems by breaking them down into simpler overlapping subproblems and storing the results of subproblems to avoid redundant calculations.

---

## Key Features

- **Optimal Substructure:** The problem can be broken into subproblems, which can be solved independently and combined for the solution.
- **Overlapping Subproblems:** The same subproblems are solved multiple times.

---

## Types of Dynamic Programming

- **Top-Down (Memoization):**  
  Solve the problem recursively and store the results of subproblems in a table to avoid recomputation.

- **Bottom-Up (Tabulation):**  
  Solve all subproblems starting from the simplest and combine them to solve bigger subproblems, typically using iteration and tables.

---

## Steps to Solve a DP Problem

1. **Characterize the structure of an optimal solution.**
2. **Define the value of an optimal solution recursively in terms of smaller subproblems.**
3. **Compute the value of an optimal solution (typically using a table).**
4. **Construct an optimal solution from the computed information (if required).**

---

## Classic Examples

| Problem                       | DP Approach                  | Time Complexity |
|-------------------------------|------------------------------|----------------|
| **Fibonacci Numbers**         | Store previous results       | O(n)           |
| **0/1 Knapsack**              | Table by weight and items    | O(nW)          |
| **Longest Common Subsequence**| Table by indices             | O(mn)          |
| **Matrix Chain Multiplication**| Table for subproblems        | O(n³)          |
| **Edit Distance**             | Table by string indices      | O(mn)          |
| **Coin Change**               | Table for min coins          | O(nW)          |

---

## Example: Fibonacci (with Memoization)

```python
def fib(n, memo={}):
    if n in memo:
        return memo[n]
    if n <= 1:
        return n
    memo[n] = fib(n-1, memo) + fib(n-2, memo)
    return memo[n]
```
- **Without DP:** Exponential time O(2^n)
- **With DP:** Linear time O(n)

---

## Example: 0/1 Knapsack (Tabulation)

- Build a table `dp[i][w]` where `i` is item and `w` is weight.
- `dp[i][w] = max(dp[i-1][w], value[i] + dp[i-1][w-weight[i]])` if `weight[i] <= w`.

---

## When to use DP?

- When there are overlapping subproblems and optimal substructure.
- When a recursive solution has redundant calculations.

---

## Tips for Interviews

- Carefully identify state variables (parameters that define subproblems).
- Write down the recurrence and think about memoization or tabulation.
- Consider space optimization (sometimes you only need the last row/column).
- Be able to reconstruct the solution (not just the value).

---

## Common Interview Questions

1. What is dynamic programming? How is it different from divide-and-conquer?
2. What are overlapping subproblems and optimal substructure?
3. Solve the Fibonacci sequence using DP.
4. Provide a DP solution for the 0/1 Knapsack problem.
5. When should you use memoization vs. tabulation?

---

## Quick Revision Table

| DP Type     | Approach          | Example Problem          |
|-------------|-------------------|-------------------------|
| Top-Down    | Recursion + Memo  | Fibonacci, LCS          |
| Bottom-Up   | Iterative Table   | Knapsack, Coin Change   |

---

## References

- [GeeksforGeeks: Dynamic Programming](https://www.geeksforgeeks.org/dynamic-programming/)
- [MIT OCW: Dynamic Programming](https://ocw.mit.edu/courses/6-006-introduction-to-algorithms-fall-2011/resources/lecture-16-dynamic-programming-i/)
- [Wikipedia: Dynamic Programming](https://en.wikipedia.org/wiki/Dynamic_programming)

---

Happy Learning! 🚀
