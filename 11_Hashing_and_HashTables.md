# 11. Hashing and Hash Tables

---

## What is Hashing?

**Hashing** is a technique used to uniquely identify a specific object from a group of similar objects, using a function called a **hash function**.  
It converts input (key) into a fixed-size value (hash code), which is used as an index to store/retrieve data efficiently.

---

## Hash Functions

A **hash function** maps keys to integers (bucket indices) in a fixed range, ideally distributing keys uniformly.

**Good hash function properties:**
- Fast to compute
- Uniform distribution of keys
- Minimizes collisions

---

## What is a Hash Table?

A **hash table** (hash map) is a data structure that stores key-value pairs, using a hash function to compute an index for storing each key.

- **Average Time Complexity:**  
  - Insert: O(1)
  - Search: O(1)
  - Delete: O(1)

- **Worst-case Time Complexity:**  
  - O(n), if all keys collide (rare with good hash function and resizing)

---

## Handling Collisions

A **collision** occurs when two keys hash to the same index.

**Collision resolution strategies:**
- **Chaining:** Store multiple elements at the same index using a linked list or another data structure.
- **Open Addressing:** Find another open slot (using probing):
  - Linear probing
  - Quadratic probing
  - Double hashing

---

## Hash Table Operations

| Operation | Description                                | Average Time Complexity |
|-----------|--------------------------------------------|------------------------|
| Insert    | Add a key-value pair                       | O(1)                   |
| Search    | Find value by key                          | O(1)                   |
| Delete    | Remove key-value pair                      | O(1)                   |

---

## Load Factor and Resizing

- **Load Factor (α):** Number of elements / Table size
- **High load factor** → more collisions → slower operations
- **Hash tables dynamically resize** (rehash) when load factor crosses a threshold (e.g., 0.7)

---

## Applications of Hash Tables

- Implementing dictionaries/maps
- Caching (LRU cache)
- Counting frequencies
- Database indexing
- Unique data storage (sets)

---

## Example: Hash Table in Python

```python
# Using Python's built-in dict (hash table)
my_dict = {}
my_dict["apple"] = 5
my_dict["banana"] = 10
print(my_dict["apple"])  # Output: 5
```

---

## Pros and Cons

**Advantages:**
- Very fast for insert/search/delete
- Simple implementation

**Disadvantages:**
- Not sorted (unordered)
- Poor worst-case performance if badly designed
- Requires good hash functions

---

## Tips for Interviews

- Always mention collision handling method if asked to implement from scratch.
- Discuss average vs. worst-case complexities.
- Know open addressing vs. chaining.
- Know Python dict, Java HashMap, C++ unordered_map.

---

## Common Interview Questions

1. What is a hash table? How does it work?
2. What are collisions and how are they resolved?
3. Compare chaining and open addressing.
4. What is the load factor? Why is resizing needed?
5. How do you implement a hash table from scratch?

---

## Quick Revision Table

| Topic               | Key Points                       |
|---------------------|----------------------------------|
| Hash Function       | Maps key to index                |
| Collision           | Two keys map to same index       |
| Chaining            | Linked list at each index        |
| Open Addressing     | Probe for next open slot         |
| Load Factor         | n / table size                   |
| Rehashing           | Resize when load is high         |

---

## References

- [GeeksforGeeks: Hashing Data Structure](https://www.geeksforgeeks.org/hashing-data-structure/)
- [Wikipedia: Hash Table](https://en.wikipedia.org/wiki/Hash_table)
- [MIT OCW: Hash Tables](https://ocw.mit.edu/courses/6-006-introduction-to-algorithms-fall-2011/resources/lecture-8-hashing-with-chaining/)
- [Python dict docs](https://docs.python.org/3/tutorial/datastructures.html#dictionaries)

---

Happy Learning! 🚀
