# 8. Backtracking and Branch & Bound

---

## Backtracking

### What is Backtracking?

**Backtracking** is a general algorithmic technique for finding all (or some) solutions to problems that incrementally build candidates and abandon candidates (“backtrack”) as soon as it determines that the candidate cannot possibly lead to a valid solution.

---

### Key Features

- Systematically searches for a solution to a problem among all available options.
- Abandons a path as soon as it determines it cannot result in a valid solution (pruning).
- Often implemented using recursion.

---

### Applications

| Problem Type              | Example Problems                |
|---------------------------|---------------------------------|
| Constraint Satisfaction   | N-Queens, Sudoku, Crossword     |
| Combinatorial Optimization| Subset Sum, Hamiltonian Cycle   |
| Permutation Problems      | String Permutations, Anagrams   |

---

### General Structure (Pseudocode)

```plaintext
function backtrack(candidate):
    if candidate is a solution:
        output candidate
        return
    for next_choice in possible_next_choices:
        if next_choice is valid:
            backtrack(candidate + next_choice)
```

---

### Example: N-Queens Problem

- Place N queens on an N×N chessboard such that no two queens attack each other.
- Try each row for queen placement and backtrack if placement leads to conflict.

---

### Complexity

- Exponential in general: O(k^n) for k choices at n steps.
- Efficient pruning is key to practical performance.

---

## Branch and Bound

### What is Branch and Bound?

**Branch and Bound** is an optimization technique similar to backtracking, but it is used for solving combinatorial optimization problems (finding the best solution) by systematically enumerating candidate solutions and using bounds to prune branches that cannot yield a better solution than the current best.

---

### Key Features

- Used to find optimal solutions (not just any feasible solution).
- Uses bounding functions to avoid exploring branches that cannot improve the current best solution.
- Typically uses a queue or priority queue (BFS or Best-First Search).

---

### Applications

| Problem Type                | Example Problems                 |
|-----------------------------|----------------------------------|
| Optimization                | Traveling Salesman Problem (TSP) |
| Integer Programming         | Knapsack Problem (0/1)           |
| Assignment Problems         | Job Assignment, Branch & Bound   |

---

### General Structure (Pseudocode)

```plaintext
function branch_and_bound():
    initialize queue with root node
    best_solution = ∞
    while queue not empty:
        node = remove from queue
        if node is a solution and better than best_solution:
            best_solution = node
        else:
            for each child of node:
                if bound(child) < best_solution:
                    add child to queue
    return best_solution
```

---

### Example: 0/1 Knapsack (Branch and Bound)

- At each node, compute the upper bound of the best possible value.
- If the upper bound is less than the current best, prune the branch.

---

## Backtracking vs. Branch and Bound

| Aspect         | Backtracking                  | Branch and Bound           |
|----------------|------------------------------|---------------------------|
| Goal           | Find any/all feasible solution| Find optimal solution     |
| Pruning        | By infeasibility              | By infeasibility & bounds |
| Usage          | CSPs, permutations            | Optimization problems     |
| Data Structure | Usually recursion stack       | Queue/Priority Queue      |

---

## Tips for Interviews

- For backtracking, always describe your pruning logic.
- For branch and bound, explain how you compute and use bounds.
- Practice writing recursive solutions for backtracking.
- Know real-world examples: N-Queens, TSP, Subset Sum, Sudoku.

---

## Common Interview Questions

1. What is backtracking? Give an example.
2. How does branch and bound differ from backtracking?
3. Solve the N-Queens problem using backtracking.
4. What is pruning in backtracking?
5. Describe the branch and bound approach for the 0/1 knapsack problem.

---

## Quick Revision Table

| Technique        | Typical Use                  | Key Feature            |
|------------------|-----------------------------|------------------------|
| Backtracking     | CSPs, all solutions         | Prune invalid paths    |
| Branch & Bound   | Optimization, best solution | Prune by bounds        |

---

## References

- [GeeksforGeeks: Backtracking](https://www.geeksforgeeks.org/backtracking-algorithms/)
- [GeeksforGeeks: Branch and Bound](https://www.geeksforgeeks.org/branch-and-bound-set-1-introduction/)
- [Wikipedia: Backtracking](https://en.wikipedia.org/wiki/Backtracking)
- [Wikipedia: Branch and Bound](https://en.wikipedia.org/wiki/Branch_and_bound)

---

Happy Learning! 🚀
