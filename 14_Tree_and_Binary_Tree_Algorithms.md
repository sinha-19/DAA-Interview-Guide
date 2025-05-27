# 14. Tree & Binary Tree Algorithms

---

## What is a Tree?

A **tree** is a hierarchical data structure consisting of nodes, with a single root and zero or more child nodes.  
A **binary tree** is a tree where each node has at most two children (left and right).

---

## Key Terminology

- **Root:** Topmost node.
- **Leaf:** Node with no children.
- **Parent/Child:** Relationship between connected nodes.
- **Height/Depth:** Height = longest path from node to leaf; Depth = distance from root.

---

## Common Types of Trees

- **Binary Tree:** Each node ≤2 children.
- **Binary Search Tree (BST):** Left < node < right.
- **AVL/Red-Black Tree:** Self-balancing BSTs.
- **Heap:** Complete tree with heap property.
- **Trie:** Prefix tree for strings.
- **Segment/Fenwick Tree:** For range queries.

---

## Binary Tree Traversals

### 1. Inorder (Left, Root, Right)

- For BST, yields sorted order.
- **Iterative or recursive.**

### 2. Preorder (Root, Left, Right)

- Used to copy tree or serialize/deserialize.

### 3. Postorder (Left, Right, Root)

- Used to delete tree, evaluate expressions.

### 4. Level Order (BFS)

- Traverses tree level by level using a queue.

---

## Traversal Examples (Python)

```python
# Inorder Traversal (recursive)
def inorder(root):
    if root:
        inorder(root.left)
        print(root.val)
        inorder(root.right)

# Level Order Traversal (BFS)
from collections import deque
def level_order(root):
    q = deque([root])
    while q:
        node = q.popleft()
        print(node.val)
        if node.left: q.append(node.left)
        if node.right: q.append(node.right)
```

---

## Important Tree Algorithms

| Problem                      | Approach/Algorithm                | Complexity        |
|------------------------------|-----------------------------------|-------------------|
| Height/Depth of tree         | DFS/recursion                     | O(n)              |
| Search in BST                | BST property, recursion/loop      | O(h), h=height    |
| Insert/Delete in BST         | BST property, recursion/loop      | O(h)              |
| Validate BST                 | Inorder traversal or bounds check | O(n)              |
| Lowest Common Ancestor (LCA) | Recursion, parent pointers        | O(n)              |
| Diameter of tree             | DFS, track heights                | O(n)              |
| Balanced tree check          | DFS, check heights                | O(n)              |
| Mirror/Invert tree           | DFS, swap left/right              | O(n)              |
| Serialize/Deserialize        | Preorder/Level order              | O(n)              |

---

## Binary Search Tree (BST) Properties

- Left subtree < node < right subtree
- Efficient search, insert, delete: O(h) time (O(log n) if balanced, O(n) if skewed)

---

## Advanced/Tricky Interview Problems

- **Kth smallest/largest in BST:** Inorder traversal with counter.
- **Check if two trees are identical:** Recursive node comparison.
- **Path sum problems:** DFS/backtracking.
- **Convert sorted array to BST:** Recursively choose middle as root.
- **Boundary/zigzag/vertical order traversal:** Use queues, stacks, hash maps.

---

## Tips for Interviews

- Draw recursion trees for clarity.
- Practice both recursive and iterative solutions.
- Know time/space complexities for each operation.
- For balanced BSTs, mention AVL or Red-Black Trees.

---

## Common Interview Questions

1. Write inorder, preorder, postorder traversals.
2. Insert/delete/search in a BST.
3. Find the height of a tree.
4. Find the lowest common ancestor of two nodes.
5. Check if a tree is balanced or a valid BST.
6. Serialize and deserialize a binary tree.

---

## Quick Revision Table

| Traversal Order | Use Case             | Output for BST      |
|-----------------|----------------------|---------------------|
| Inorder         | Sorted output        | Yes                 |
| Preorder        | Copy/serialize tree  | No                  |
| Postorder       | Delete/eval tree     | No                  |
| Level Order     | BFS, shortest path   | No                  |

---

## References

- [GeeksforGeeks: Tree Data Structure](https://www.geeksforgeeks.org/binary-tree-data-structure/)
- [LeetCode: Tree problems](https://leetcode.com/tag/tree/)
- [Wikipedia: Tree (data structure)](https://en.wikipedia.org/wiki/Tree_(data_structure))

---

Happy Learning! 🌳🚀
