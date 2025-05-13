# Data Structures and Algorithms Study Notes

## Table of Contents
1. [Time and Space Complexity](#time-and-space-complexity)
2. [Arrays](#arrays)
3. [Linked Lists](#linked-lists)
4. [Stacks and Queues](#stacks-and-queues)
5. [Trees](#trees)
6. [Graphs](#graphs)
7. [Sorting Algorithms](#sorting-algorithms)
8. [Searching Algorithms](#searching-algorithms)
9. [Dynamic Programming](#dynamic-programming)
10. [Practice Problems](#practice-problems)

---

## Time and Space Complexity
### Big-O Notation
- O(1) - Constant time
- O(n) - Linear time
- O(log n) - Logarithmic time
- O(n²) - Quadratic time
- O(2^n) - Exponential time

### Calculating Complexity
- Analyze worst-case scenario
- Drop constants and lower order terms
- Common patterns:
  - Single loop → O(n)
  - Nested loops → O(n²)
  - Divide and conquer → O(log n)

---

## Arrays
### Basic Operations
- Access: O(1)
- Search: O(n)
- Insertion: O(n)
- Deletion: O(n)

### Important Problems
1. Two Sum
2. Maximum Subarray
3. Rotate Array
4. Contains Duplicate

---

## Linked Lists
### Types
- Singly Linked List
- Doubly Linked List
- Circular Linked List

### Operations
- Insertion at head: O(1)
- Deletion at head: O(1)
- Search: O(n)
- Insertion/deletion at tail: O(n) (O(1) if tail pointer maintained)

### Important Problems
1. Reverse a Linked List
2. Detect Cycle
3. Merge Two Sorted Lists
4. Remove Nth Node From End

---

## Stacks and Queues
### Stack (LIFO)
- Operations: push(), pop(), peek() - all O(1)
- Applications: Function calls, undo operations, DFS

### Queue (FIFO)
- Operations: enqueue(), dequeue() - O(1)
- Applications: BFS, task scheduling

### Important Problems
1. Valid Parentheses
2. Implement Queue using Stacks
3. Next Greater Element
4. Sliding Window Maximum

---

## Trees
### Binary Tree
- Traversals:
  - In-order (Left, Root, Right)
  - Pre-order (Root, Left, Right)
  - Post-order (Left, Right, Root)
  - Level-order (BFS)

### Binary Search Tree
- Property: Left < Root < Right
- Search: O(log n) in balanced tree

### Important Problems
1. Invert Binary Tree
2. Validate BST
3. Lowest Common Ancestor
4. Tree Traversals

---

## Graphs
### Representations
1. Adjacency Matrix
2. Adjacency List

### Algorithms
- BFS: O(V + E)
- DFS: O(V + E)
- Dijkstra's (Shortest Path)
- Topological Sort

### Important Problems
1. Clone Graph
2. Course Schedule
3. Number of Islands
4. Network Delay Time

---

## Sorting Algorithms
| Algorithm | Time (Best) | Time (Avg) | Time (Worst) | Space | Stable |
|-----------|------------|------------|-------------|-------|--------|
| Bubble    | O(n)       | O(n²)      | O(n²)       | O(1)  | Yes    |
| Selection | O(n²)      | O(n²)      | O(n²)       | O(1)  | No     |
| Insertion | O(n)       | O(n²)      | O(n²)       | O(1)  | Yes    |
| Merge     | O(n log n) | O(n log n) | O(n log n)  | O(n)  | Yes    |
| Quick     | O(n log n) | O(n log n) | O(n²)       | O(1)  | No     |
| Heap      | O(n log n) | O(n log n) | O(n log n)  | O(1)  | No     |

---

## Searching Algorithms
### Linear Search
- O(n) time
- Works on any list

### Binary Search
- O(log n) time
- Requires sorted array

### Important Problems
1. Search in Rotated Sorted Array
2. Find Peak Element
3. First Bad Version
4. Find Minimum in Rotated Sorted Array

---

## Dynamic Programming
### Key Concepts
- Overlapping subproblems
- Optimal substructure
- Memoization (top-down)
- Tabulation (bottom-up)

### Common Patterns
1. Fibonacci sequence
2. 0/1 Knapsack
3. Longest Common Subsequence
4. Coin Change

### Important Problems
1. Climbing Stairs
2. House Robber
3. Longest Increasing Subsequence
4. Edit Distance

---

## Practice Problems
### Easy
1. Two Sum
2. Valid Parentheses
3. Merge Two Sorted Lists
4. Maximum Subarray

### Medium
1. Add Two Numbers
2. Longest Substring Without Repeating Characters
3. 3Sum
4. Container With Most Water

### Hard
1. Median of Two Sorted Arrays
2. Regular Expression Matching
3. Merge k Sorted Lists
4. Trapping Rain Water