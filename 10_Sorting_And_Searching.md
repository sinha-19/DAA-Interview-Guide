# 10. Sorting & Searching Algorithms

---

## Sorting Algorithms

Sorting is the process of arranging data in a particular order (ascending/descending). Efficient sorting is crucial for optimizing other algorithms.

---

### Common Sorting Algorithms

| Algorithm      | Best Case | Worst Case | Space Complexity | Stable | Technique           |
|----------------|-----------|------------|------------------|--------|---------------------|
| Bubble Sort    | O(n)      | O(n²)      | O(1)             | Yes    | Comparison-based    |
| Selection Sort | O(n²)     | O(n²)      | O(1)             | No     | Comparison-based    |
| Insertion Sort | O(n)      | O(n²)      | O(1)             | Yes    | Comparison-based    |
| Merge Sort     | O(n log n)| O(n log n) | O(n)             | Yes    | Divide & Conquer    |
| Quick Sort     | O(n log n)| O(n²)      | O(log n)         | No     | Divide & Conquer    |
| Heap Sort      | O(n log n)| O(n log n) | O(1)             | No     | Heap-based          |
| Counting Sort  | O(n+k)    | O(n+k)     | O(k)             | Yes    | Non-comparison      |
| Radix Sort     | O(nk)     | O(nk)      | O(n+k)           | Yes    | Non-comparison      |
| Bucket Sort    | O(n+k)    | O(n²)      | O(n+k)           | Yes    | Non-comparison      |

---

### Example: Merge Sort (Divide and Conquer)

**Idea:** Split array into halves, recursively sort, then merge.

**Pseudocode:**
```python
def merge_sort(arr):
    if len(arr) > 1:
        mid = len(arr)//2
        L, R = arr[:mid], arr[mid:]
        merge_sort(L)
        merge_sort(R)
        # Merge step
        i = j = k = 0
        while i < len(L) and j < len(R):
            if L[i] < R[j]:
                arr[k] = L[i]
                i += 1
            else:
                arr[k] = R[j]
                j += 1
            k += 1
        arr[k:] = L[i:] + R[j:]
```

---

### Example: Quick Sort (Divide and Conquer)

**Idea:** Pick a pivot, partition array, recursively sort subarrays.

**Pseudocode:**
```python
def quick_sort(arr):
    if len(arr) <= 1:
        return arr
    pivot = arr[0]
    left  = [x for x in arr[1:] if x < pivot]
    right = [x for x in arr[1:] if x >= pivot]
    return quick_sort(left) + [pivot] + quick_sort(right)
```

---

### Stability in Sorting

- **Stable sort:** Maintains the relative order of equal elements (e.g., Merge Sort, Insertion Sort).
- **Unstable sort:** May change the order of equal elements (e.g., Quick Sort, Heap Sort).

---

## Searching Algorithms

Searching is the process of finding the location of a given element in a dataset.

---

### Common Searching Algorithms

| Algorithm       | Data Structure      | Time Complexity | Technique         |
|-----------------|---------------------|-----------------|-------------------|
| Linear Search   | Array/List          | O(n)            | Sequential        |
| Binary Search   | Sorted Array/List   | O(log n)        | Divide & Conquer  |
| Hash Search     | Hash Table          | O(1) average    | Hashing           |

---

### Example: Linear Search

**Idea:** Check each element until found.

**Pseudocode:**
```python
def linear_search(arr, x):
    for i in range(len(arr)):
        if arr[i] == x:
            return i
    return -1
```

---

### Example: Binary Search (on sorted array)

**Idea:** Repeatedly divide search interval in half.

**Pseudocode:**
```python
def binary_search(arr, x):
    left, right = 0, len(arr)-1
    while left <= right:
        mid = (left + right) // 2
        if arr[mid] == x:
            return mid
        elif arr[mid] < x:
            left = mid + 1
        else:
            right = mid - 1
    return -1
```

---

## Tips for Interviews

- Know time and space complexities of all common algorithms.
- Explain stability and in-place sorting.
- For searching, clarify if input is sorted (use binary search if yes).

---

## Common Interview Questions

1. Compare Merge Sort and Quick Sort.
2. When is counting sort preferred over comparison-based sorts?
3. What is a stable sort? Which algorithms are stable?
4. Implement binary search on a sorted array.
5. Why is quicksort's worst-case O(n²)? How can it be avoided?

---

## Quick Revision Table

| Algorithm     | Best Case | Avg Case | Worst Case | Stable | In-place |
|---------------|-----------|----------|------------|--------|----------|
| Bubble Sort   | O(n)      | O(n²)    | O(n²)      | Yes    | Yes      |
| Merge Sort    | O(n log n)| O(n log n)| O(n log n)| Yes    | No       |
| Quick Sort    | O(n log n)| O(n log n)| O(n²)     | No     | Yes      |
| Heap Sort     | O(n log n)| O(n log n)| O(n log n)| No     | Yes      |
| Binary Search | O(1)      | O(log n) | O(log n)   | --     | --       |

---

## References

- [GeeksforGeeks: Sorting Algorithms](https://www.geeksforgeeks.org/sorting-algorithms/)
- [GeeksforGeeks: Searching Algorithms](https://www.geeksforgeeks.org/searching-algorithms/)
- [MIT OCW: Sorting & Searching](https://ocw.mit.edu/courses/6-006-introduction-to-algorithms-fall-2011/resources/lecture-4-sorting/)
- [Wikipedia: Sorting Algorithm](https://en.wikipedia.org/wiki/Sorting_algorithm)

---

Happy Learning! 🚀
