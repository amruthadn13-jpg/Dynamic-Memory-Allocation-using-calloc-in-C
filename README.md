# Dynamic Memory Allocation using calloc() in C

## Overview

This project demonstrates how to use the `calloc()` function in C for dynamic memory allocation. The program allocates memory for an integer array at runtime, stores values in the allocated memory, and prints the stored data.

---

## Concepts Covered

- Dynamic Memory Allocation
- `calloc()` Function
- Pointers
- Array Access using Pointers
- Memory Initialization
- Runtime Memory Management

---

## Project Description

The program dynamically allocates memory for **4 integer elements** using `calloc()`.

```c
ptr = calloc(4, sizeof(*ptr));
```

- `4` → Number of elements to allocate
- `sizeof(*ptr)` → Size of one integer element
- `calloc()` initializes all allocated memory to zero.

After allocation, values are stored in the memory locations using pointer and array notation.

```c
*ptr = 2;
ptr[1] = 4;
ptr[2] = 6;
```

The stored values are then printed using `printf()`.

---

## How calloc() Works

```c
ptr = calloc(number_of_elements, size_of_each_element);
```

Example:

```c
ptr = calloc(4, sizeof(int));
```

This allocates memory for:

```text
4 × 4 bytes = 16 bytes
```

and initializes all values to:

```text
0 0 0 0
```

---

## Memory Representation

```text
Index      Value

ptr[0]  ->   2
ptr[1]  ->   4
ptr[2]  ->   6
ptr[3]  ->   0
```

The last element remains `0` because `calloc()` automatically initializes allocated memory to zero.

---

## Sample Output

```text
2
4 6 0
```

---

## Key Difference: calloc() vs malloc()

| calloc() | malloc() |
|----------|-----------|
| Initializes memory to zero | Memory contains garbage values |
| Requires two arguments | Requires one argument |
| Slightly slower | Faster |
| Suitable when initialized memory is needed | Suitable for raw memory allocation |

---

## Learning Outcomes

- Understanding dynamic memory allocation
- Using `calloc()` for allocating arrays dynamically
- Working with pointers and array indexing
- Understanding memory initialization
- Managing memory at runtime

---

## Real-World Applications

- Dynamic Arrays
- Embedded Systems
- Data Structures
- Memory-Constrained Applications
- Operating Systems
- Buffer Allocation

---

## Time Complexity

```text
O(1)
```

Memory allocation is performed in constant time for this fixed-size example.

---

## Space Complexity

```text
O(n)
```

Where `n` is the number of allocated elements.

---

## Key Takeaway

`calloc()` is used to dynamically allocate memory and automatically initialize all allocated bytes to zero, making it safer and more convenient than `malloc()` when initialized memory is required.

---

## Author

**Amrutha D N**
