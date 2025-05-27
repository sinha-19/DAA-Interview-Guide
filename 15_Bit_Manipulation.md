# 15. Bit Manipulation

---

## What is Bit Manipulation?

**Bit manipulation** involves using bitwise operators to directly manipulate bits within integers.  
It's a powerful technique for optimizing code, often used in system programming, competitive coding, and interviews.

---

## Common Bitwise Operators

| Operator | Name             | Symbol | Example (A=5, B=3) | Result   |
|----------|------------------|--------|--------------------|----------|
| AND      | Bitwise AND      | &      | 5 & 3 (101 & 011)  | 1 (001)  |
| OR       | Bitwise OR       | \|     | 5 \| 3 (101 \| 011)| 7 (111)  |
| XOR      | Bitwise XOR      | ^      | 5 ^ 3 (101 ^ 011)  | 6 (110)  |
| NOT      | Bitwise NOT      | ~      | ~5 (~000...0101)   | -6       |
| LEFT     | Left Shift       | <<     | 5 << 1 (101 << 1)  | 10 (1010)|
| RIGHT    | Right Shift      | >>     | 5 >> 1 (101 >> 1)  | 2 (10)   |

---

## Common Uses

- Swapping values without temp variables
- Checking if a number is even/odd
- Setting, clearing, toggling, checking bits
- Counting set bits (1s)
- Finding single/multiple unique numbers in arrays
- Fast multiplication/division by powers of 2
- Subset/enumeration generation (bitmasking)

---

## Bit Tricks & Patterns

### 1. Check if a number is even/odd

```python
if n & 1 == 0:   # Even
if n & 1 == 1:   # Odd
```

### 2. Swap two numbers (XOR swap)

```python
a = a ^ b
b = a ^ b
a = a ^ b
```

### 3. Set, Clear, Toggle, and Check a Bit

```python
# Set i-th bit
n = n | (1 << i)

# Clear i-th bit
n = n & ~(1 << i)

# Toggle i-th bit
n = n ^ (1 << i)

# Check i-th bit
if n & (1 << i):
    # i-th bit is set
```

### 4. Count number of set bits

```python
# Brian Kernighan’s Algorithm
count = 0
while n:
    n = n & (n-1)
    count += 1
```

### 5. Check if a number is a power of two

```python
def is_power_of_two(n):
    return n > 0 and (n & (n-1)) == 0
```

### 6. Get the rightmost set bit

```python
rightmost = n & -n
```

---

## Typical Interview Problems

- Find the single number in an array where every element appears twice except one (XOR all numbers).
- Find two non-repeating elements in an array.
- Count the number of 1 bits (Hamming weight).
- Reverse bits of a number.
- Generate all subsets using bitmasks.

---

## Applications

- Cryptography, compression algorithms
- Network protocols
- Graphics/image processing
- Permissions/masks
- Game development (states, moves)

---

## Tips for Interviews

- Know bitwise operations, their symbols, and use cases.
- Practice common bit patterns and masking tricks.
- Be careful of signed/unsigned and overflow issues.
- Use bit manipulation to optimize space/time.

---

## Quick Revision Table

| Task                        | Bit Trick                       |
|-----------------------------|---------------------------------|
| Even/Odd                    | n & 1                           |
| Set/Clear/Toggle i-th bit   | n \| (1<<i), n & ~(1<<i), n ^ (1<<i) |
| Count set bits              | n = n & (n-1)                   |
| Power of two                | n & (n-1) == 0                  |
| Rightmost set bit           | n & -n                          |

---

## References

- [GeeksforGeeks: Bit Manipulation](https://www.geeksforgeeks.org/bitwise-algorithms/)
- [LeetCode: Bit Manipulation Problems](https://leetcode.com/tag/bit-manipulation/)
- [Wikipedia: Bit Manipulation](https://en.wikipedia.org/wiki/Bit_manipulation)

---

Happy Learning! 🚀
