# 13. Strings & Pattern Matching

---

## String Algorithms Overview

String manipulation and pattern matching are common topics in coding interviews and competitive programming. Efficient algorithms are required to process, search, and analyze text data.

---

## Core String Concepts

- **String Searching**: Finding a substring (pattern) within a larger string (text).
- **Pattern Matching**: Identifying all occurrences of a pattern in a string.

---

## Naive String Matching

- **Idea:** Check for the pattern at every position in the text.
- **Time Complexity:** O((n-m+1) * m) where n = text length, m = pattern length.
- **Drawback:** Inefficient for large texts/patterns.

---

## Efficient Pattern Matching Algorithms

### 1. Knuth-Morris-Pratt (KMP) Algorithm

- **Key Idea:** Avoid redundant comparisons by using information from previous matches.
- **Preprocess**: Build an LPS (Longest Prefix Suffix) array.
- **Time Complexity:** O(n + m)
- **Use Case:** Finding all occurrences of a pattern efficiently.

### 2. Rabin-Karp Algorithm

- **Key Idea:** Use hash values to quickly compare substrings.
- **Preprocess**: Compute hash for pattern; slide window and compare hashes.
- **Time Complexity:** Average O(n + m), Worst O(nm) (rare).
- **Use Case:** Multiple pattern search.

### 3. Z Algorithm

- **Key Idea:** Create a Z-array where Z[i] is the length of the longest substring starting from i which matches the prefix of the string.
- **Time Complexity:** O(n + m)
- **Use Case:** Pattern matching and string analysis.

### 4. Boyer-Moore Algorithm

- **Key Idea:** Start matching from the end of the pattern and use bad character and good suffix heuristics to skip sections.
- **Time Complexity:** Best O(n/m), Worst O(nm)
- **Use Case:** Large alphabets, long patterns.

---

## Advanced String Data Structures

| Data Structure     | Use Case                  | Complexity           |
|--------------------|--------------------------|----------------------|
| Trie               | Prefix searches, autocomplete | O(L) per operation   |
| Suffix Tree        | Fast substring search, repetitions | O(n) build, O(m) search |
| Suffix Array       | Efficient substring queries | O(n log n) build    |

---

## Example: KMP Algorithm (Python)

```python
def compute_lps(pattern):
    lps = [0] * len(pattern)
    length = 0
    i = 1
    while i < len(pattern):
        if pattern[i] == pattern[length]:
            length += 1
            lps[i] = length
            i += 1
        else:
            if length != 0:
                length = lps[length-1]
            else:
                lps[i] = 0
                i += 1
    return lps

def kmp_search(text, pattern):
    n, m = len(text), len(pattern)
    lps = compute_lps(pattern)
    i = j = 0
    while i < n:
        if pattern[j] == text[i]:
            i += 1
            j += 1
        if j == m:
            print(f"Pattern found at index {i-j}")
            j = lps[j-1]
        elif i < n and pattern[j] != text[i]:
            if j != 0:
                j = lps[j-1]
            else:
                i += 1
```

---

## Palindrome Problems

- **Palindrome:** String that reads the same forward and backward ("racecar").
- **Common Interview Questions:**
  - Longest Palindromic Substring (Manacher’s Algorithm, DP)
  - Palindrome Partitioning

---

## Other Important String Algorithms

- **Anagram Checking:** Use sorting or hash maps.
- **Substring/Permutation Problems:** Sliding window technique.
- **Longest Common Substring/Subsequence:** DP algorithms.
- **String Compression:** Run-length encoding, etc.

---

## Tips for Interviews

- Clarify if a naive solution is acceptable, or if efficient matching is required.
- Be able to implement KMP and explain the LPS array.
- Know how to use tries and suffix arrays for advanced pattern matching.
- Practice sliding window and hash map techniques for substring/anagram problems.

---

## Common Interview Questions

1. Implement KMP/Rabin-Karp for pattern matching.
2. Find the longest palindromic substring.
3. Check if two strings are anagrams.
4. Find all permutations of a string in another.
5. Explain the use of tries in autocomplete.
6. Longest common subsequence between two strings.

---

## Quick Revision Table

| Algorithm    | Best Use Case          | Time Complexity |
|--------------|-----------------------|-----------------|
| KMP          | Fast pattern matching  | O(n + m)        |
| Rabin-Karp   | Multiple patterns      | O(n + m) avg    |
| Z Algorithm  | All pattern positions  | O(n + m)        |
| Naive        | Small inputs           | O(nm)           |

---

## References

- [GeeksforGeeks: Pattern Searching](https://www.geeksforgeeks.org/pattern-searching/)
- [KMP Algorithm Explained](https://www.geeksforgeeks.org/kmp-algorithm-for-pattern-searching/)
- [Wikipedia: String-searching algorithm](https://en.wikipedia.org/wiki/String-searching_algorithm)

---

Happy Learning! 🚀
