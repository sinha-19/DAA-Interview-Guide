# 16. NP-Completeness & Computational Complexity

---

## What is Computational Complexity?

Computational complexity is the study of the resources (time, space) required to solve computational problems.  
Problems are grouped into classes based on the difficulty of solving them and verifying solutions.

---

## Basic Complexity Classes

| Class | Definition |
|-------|------------|
| **P** | Problems solvable in polynomial time by a deterministic Turing machine (efficiently solvable). |
| **NP** | Problems for which a solution can be verified in polynomial time by a deterministic Turing machine. |
| **co-NP** | Complements of problems in NP. |
| **EXP** | Problems solvable in exponential time. |

- **All P problems are also NP**: P ⊆ NP

---

## What is NP-Completeness?

- **NP-Complete (NPC)**: Problems in NP that are as hard as any other problem in NP.
  - A problem L is NP-complete if:
    1. L ∈ NP (a solution can be verified in polynomial time)
    2. Every problem in NP can be reduced to L in polynomial time (L is NP-hard)

- **NP-Hard**: At least as hard as the hardest problems in NP (may or may not be in NP, i.e., may not even be verifiable efficiently).

---

## The Big Question: P vs NP

- Does P = NP?
  - If yes: Every problem whose solution can be verified quickly (in polynomial time) can also be solved quickly.
  - If no: There are some problems easy to verify but hard to solve.
- **Open problem**: No known proof as of 2024.

---

## Reductions

- **Reduction**: Transforming one problem into another.
- If A ≤p B (A reduces to B in polynomial time), and B is easy, A is also easy.
- Used to prove NP-completeness: Reduce a known NP-complete problem to a new problem.

---

## How to Prove NP-Completeness

1. Show the problem is in NP (solution can be verified in polynomial time).
2. Choose a known NP-complete problem.
3. Show that the known NPC problem can be reduced to your problem in polynomial time.

---

## Famous NP-Complete Problems

- Satisfiability (SAT, 3-SAT)
- Subset Sum
- Traveling Salesman Problem (decision version)
- Vertex Cover
- Hamiltonian Cycle
- Clique
- Partition Problem
- Graph Coloring

---

## Examples

- **Subset Sum**: Given a set of integers, does any subset sum to zero?
- **Vertex Cover**: Is there a set of k vertices covering all edges in a graph?
- **3-SAT**: Given a boolean formula in CNF with 3 literals per clause, is it satisfiable?

---

## Polynomial-Time Approximation

- For many NP-complete problems, no known polynomial-time exact solution exists.
- We use **approximation algorithms** to get near-optimal solutions, e.g., for TSP, Vertex Cover.

---

## Tips for Interviews

- Know definitions of P, NP, NP-complete, and NP-hard.
- Understand polynomial-time reductions.
- Be familiar with classic NP-complete problems.
- Recognize which problems are tractable, intractable, or approximable.
- Be ready to explain the significance of P vs NP.

---

## Common Interview Questions

1. What is the difference between P, NP, NP-complete, and NP-hard?
2. Explain the significance of P vs NP.
3. How do you prove that a problem is NP-complete?
4. Give examples of NP-complete problems.
5. Why do we use approximation algorithms?

---

## Quick Revision Table

| Term        | Meaning                             | Example           |
|-------------|-------------------------------------|-------------------|
| P           | Solvable in polynomial time         | Sorting, MST      |
| NP          | Verifiable in polynomial time       | SAT, TSP (decision)|
| NP-complete | Hardest in NP                       | 3-SAT, Vertex Cover|
| NP-hard     | At least as hard as NPC             | Halting Problem   |

---

## References

- [GeeksforGeeks: NP-Completeness](https://www.geeksforgeeks.org/np-completeness-set-1/)
- [Wikipedia: NP-completeness](https://en.wikipedia.org/wiki/NP-completeness)
- [MIT OCW: Computational Complexity](https://ocw.mit.edu/courses/6-006-introduction-to-algorithms-fall-2011/pages/lecture-notes/)

---

Happy Learning! 🚀
