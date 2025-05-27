# 2. Analysis of Algorithms: Time & Space Complexity

---

## Why Analyze Algorithms?

- To compare different algorithms and choose the most efficient one for a problem.
- To predict the resources (time and memory) an algorithm will need as input size grows.
- Essential for interviews and competitive programming.

---

## Types of Analysis

1. **Worst Case**  
   Maximum time/space taken for any input of size n.  
   Example: Linear search in an unsorted array when the element is not present.

2. **Best Case**  
   Minimum time/space taken for any input of size n.  
   Example: Linear search when the element is the first item.

3. **Average Case**  
   Expected time/space taken over all inputs of size n.

---

## Algorithm Complexity Measures

### 1. Time Complexity

- **Definition:** Total number of elementary operations or steps executed by the algorithm as a function of input size (n).
- **Goal:** Estimate how running time increases as input size grows.

#### Common Time Complexities

| Complexity      | Example Algorithm                    |
|-----------------|-------------------------------------|
| O(1)            | Accessing array element by index     |
| O(log n)        | Binary Search                       |
| O(n)            | Linear Search, Traversing an array  |
| O(n log n)      | Merge Sort, Heap Sort               |
| O(n²)           | Bubble Sort, Selection Sort         |
| O(2ⁿ)           | Recursive Fibonacci                 |
| O(n!)           | Generating all permutations         |

### 2. Space Complexity

- **Definition:** Amount of memory space required by an algorithm as a function of input size.
- Includes input storage, auxiliary space (variables, function call stack, etc.).

#### Example

```plaintext
Algorithm SumArray(A, n):
    sum = 0
    for i = 0 to n-1
        sum = sum + A[i]
    return sum
```
- Time Complexity: O(n)
- Space Complexity: O(1) (uses only a constant amount of extra space)

---

## How to Calculate Complexity

1. **Identify Basic Operations:** Count the most significant operations inside loops or recursions.
2. **Express as a Function of n:** How many times does the operation run as input size grows?
3. **Ignore Constants & Lower Order Terms:** Focus on the most dominant term as n → ∞.

---

## Asymptotic Analysis

- Focuses on input size approaching infinity (large n).
- Uses notations: Big O, Omega, and Theta (covered in the next chapter).

---

## Tips for Interviews

- Always explain your analysis (not just give the Big O).
- Compare alternatives if possible.
- Mention both time and space complexity.

---

## Common Interview Questions

1. What is time complexity? Why is it important?
2. What is the difference between time complexity and space complexity?
3. Give examples of O(1), O(n), O(n²), O(log n) algorithms.
4. How do you analyze the complexity of nested loops?
5. What is worst-case vs. average-case complexity?

---

## Quick Revision Table

| Complexity | Example Algorithm      | Typical Scenario         |
|------------|-----------------------|-------------------------|
| O(1)       | Hash table lookup     | Direct access           |
| O(log n)   | Binary search         | Divide and conquer      |
| O(n)       | Linear search         | List traversal          |
| O(n²)      | Bubble sort           | Nested loops            |

---

## References

- [GeeksforGeeks: Analysis of Algorithms](https://www.geeksforgeeks.org/analysis-of-algorithms-set-1-asymptotic-analysis/)
- [MIT OCW: Algorithm Analysis](https://ocw.mit.edu/courses/6-006-introduction-to-algorithms-fall-2011/resources/lecture-1-algorithmic-thinking-peak-finding/)
- [Wikipedia: Analysis of Algorithms](https://en.wikipedia.org/wiki/Analysis_of_algorithms)

---

Happy Learning! 🚀
