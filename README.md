LeetCode Pattern-Based DSA Roadmap

A pattern-based collection of LeetCode problems organized by problem-solving technique rather than random question order.

The goal is simple:

Don't memorize solutions. Learn the pattern, understand when to use it, and solve multiple variations of the same pattern.

📚 Patterns Covered
 Arrays & Hashing
 Two Pointers
 Sliding Window
 Prefix Sum
 Binary Search
 Linked List
 Stack
 Queue & Deque
 Heap / Priority Queue
 Intervals
 Binary Tree
 Binary Search Tree
 Graph DFS/BFS
 Topological Sort
 Union Find / DSU
 Shortest Path
 Backtracking
 Greedy
 Dynamic Programming
 Trie
 Bit Manipulation
 Math
 Divide & Conquer
🗂️ Repository Structure
LeetCode-DSA/
│
├── 01-Arrays-Hashing/
├── 02-Two-Pointers/
├── 03-Sliding-Window/
├── 04-Prefix-Sum/
├── 05-Binary-Search/
├── 06-Linked-List/
├── 07-Stack/
├── 08-Queue/
├── 09-Heap/
├── 10-Intervals/
├── 11-Binary-Tree/
├── 12-BST/
├── 13-Graph/
├── 14-Topological-Sort/
├── 15-Union-Find/
├── 16-Shortest-Path/
├── 17-Backtracking/
├── 18-Greedy/
├── 19-Dynamic-Programming/
├── 20-Trie/
├── 21-Bit-Manipulation/
├── 22-Math/
└── 23-Divide-and-Conquer/
1. Arrays & Hashing
HashSet
#	Problem	Difficulty
217	Contains Duplicate	Easy
349	Intersection of Two Arrays	Easy
128	Longest Consecutive Sequence	Medium
202	Happy Number	Easy
HashMap / Frequency
#	Problem	Difficulty
1	Two Sum	Easy
49	Group Anagrams	Medium
347	Top K Frequent Elements	Medium
560	Subarray Sum Equals K	Medium

Recognition:
Duplicate, frequency, lookup, counting → Hashing

2. Two Pointers
Opposite Direction
#	Problem	Difficulty
125	Valid Palindrome	Easy
167	Two Sum II	Medium
11	Container With Most Water	Medium
15	3Sum	Medium
18	4Sum	Medium
42	Trapping Rain Water	Hard
Same Direction
#	Problem	Difficulty
26	Remove Duplicates	Easy
27	Remove Element	Easy
283	Move Zeroes	Easy
392	Is Subsequence	Easy
287	Find the Duplicate Number	Medium

Recognition:
Sorted array, pair search, left/right movement → Two Pointers

3. Sliding Window
Fixed Window
 643 — Maximum Average Subarray I
 1343 — Number of Sub-arrays of Size K
 1456 — Maximum Number of Vowels
Variable Window
 3 — Longest Substring Without Repeating Characters
 209 — Minimum Size Subarray Sum
 904 — Fruit Into Baskets
 1004 — Max Consecutive Ones III
 424 — Longest Repeating Character Replacement
 76 — Minimum Window Substring

Recognition:

Longest / Shortest + Substring / Subarray + Condition = Sliding Window

4. Prefix Sum
5. 
 1480 — Running Sum
 724 — Find Pivot Index
 303 — Range Sum Query
 560 — Subarray Sum Equals K
 974 — Subarray Sums Divisible by K
 525 — Contiguous Array

Recognition:

Repeated range/subarray sum → Prefix Sum

5. Binary Search
   
Standard
 704 — Binary Search
 35 — Search Insert Position
 34 — First and Last Position
 33 — Search in Rotated Sorted Array
 81 — Search in Rotated Sorted Array II
   
Binary Search on Answer ⭐

 875 — Koko Eating Bananas
 1011 — Capacity To Ship Packages Within D Days
 1482 — Minimum Number of Days to Make m Bouquets
 1552 — Magnetic Force Between Two Balls
 410 — Split Array Largest Sum

Recognition:

Minimize the maximum
Maximize the minimum

→ Binary Search on Answer

6. Linked List
Basic
 206 — Reverse Linked List
 21 — Merge Two Sorted Lists
 876 — Middle of Linked List
 203 — Remove Linked List Elements
Fast & Slow Pointer
 141 — Linked List Cycle
 142 — Linked List Cycle II
 234 — Palindrome Linked List
 19 — Remove Nth Node From End
Advanced
 143 — Reorder List
 138 — Copy List with Random Pointer
 23 — Merge k Sorted Lists
 25 — Reverse Nodes in k-Group
7. Stack
Basic Stack
 20 — Valid Parentheses
 155 — Min Stack
 150 — Evaluate Reverse Polish Notation
Monotonic Stack ⭐
 496 — Next Greater Element I
 503 — Next Greater Element II
 739 — Daily Temperatures
 901 — Online Stock Span
 84 — Largest Rectangle in Histogram
 42 — Trapping Rain Water

Recognition:

Next Greater / Next Smaller → Monotonic Stack

8. Heap / Priority Queue
Top K
 215 — Kth Largest Element
 347 — Top K Frequent Elements
 973 — K Closest Points to Origin
 692 — Top K Frequent Words
Two Heaps
 295 — Find Median from Data Stream
 480 — Sliding Window Median
K Sorted
 23 — Merge k Sorted Lists
 378 — Kth Smallest Element in a Sorted Matrix
 373 — Find K Pairs with Smallest Sums

Recognition:

Top K / Kth largest / Kth smallest → Heap

9. Intervals
 56 — Merge Intervals
 57 — Insert Interval
 986 — Interval List Intersections
 252 — Meeting Rooms
 253 — Meeting Rooms II
 435 — Non-overlapping Intervals
 452 — Minimum Number of Arrows

Recognition:

Overlapping ranges / meetings / schedules → Intervals

10. Binary Tree
DFS
 100 — Same Tree
 104 — Maximum Depth
 226 — Invert Binary Tree
 543 — Diameter of Binary Tree
 110 — Balanced Binary Tree
BFS
 102 — Level Order Traversal
 103 — Zigzag Level Order
 199 — Right Side View
 515 — Largest Value in Each Row
Path
 112 — Path Sum
 113 — Path Sum II
 437 — Path Sum III
 124 — Binary Tree Maximum Path Sum
11. Graph
DFS/BFS
 1971 — Find if Path Exists
 547 — Number of Provinces
 841 — Keys and Rooms
 200 — Number of Islands
 695 — Max Area of Island
 733 — Flood Fill
 994 — Rotting Oranges
 542 — 01 Matrix

Recognition:

Connected components / islands / paths → DFS or BFS

12. Topological Sort
 207 — Course Schedule
 210 — Course Schedule II
 802 — Find Eventual Safe States
 310 — Minimum Height Trees
 269 — Alien Dictionary

Recognition:

Prerequisites
Dependencies
Ordering

→ Topological Sort

13. Union Find / DSU
 547 — Number of Provinces
 684 — Redundant Connection
 721 — Accounts Merge
 1319 — Network Connected
 947 — Most Stones Removed

Recognition:

Groups + connections + merging → DSU

14. Backtracking
Subsets
 78 — Subsets
 90 — Subsets II
Permutations
 46 — Permutations
 47 — Permutations II
Combination
 77 — Combinations
 39 — Combination Sum
 40 — Combination Sum II
Advanced
 51 — N-Queens
 37 — Sudoku Solver
 131 — Palindrome Partitioning

Recognition:

Generate ALL possibilities
        ↓
Backtracking
15. Greedy
 121 — Best Time to Buy and Sell Stock
 122 — Best Time to Buy and Sell Stock II
 455 — Assign Cookies
 860 — Lemonade Change
 55 — Jump Game
 45 — Jump Game II
 134 — Gas Station
 763 — Partition Labels
 135 — Candy

Recognition:

Best local decision → Greedy

16. Dynamic Programming
1D DP
 70 — Climbing Stairs
 746 — Min Cost Climbing Stairs
 198 — House Robber
 213 — House Robber II
 91 — Decode Ways
Knapsack
 322 — Coin Change
 518 — Coin Change II
 416 — Partition Equal Subset Sum
 494 — Target Sum
Subsequence
 300 — Longest Increasing Subsequence
 1143 — Longest Common Subsequence
 1035 — Uncrossed Lines
Grid DP
 62 — Unique Paths
 63 — Unique Paths II
 64 — Minimum Path Sum
 120 — Triangle
String DP
 72 — Edit Distance
 97 — Interleaving String
 115 — Distinct Subsequences

Recognition:

Current answer depends on previous answers
        ↓
Dynamic Programming
17. Trie
 208 — Implement Trie
 211 — Design Add and Search Words
 212 — Word Search II
 648 — Replace Words
 677 — Map Sum Pairs

Recognition:

Prefix / dictionary / autocomplete → Trie

18. Bit Manipulation
XOR
 136 — Single Number
 268 — Missing Number
 260 — Single Number III
    
Bit Counting
 191 — Number of 1 Bits
 338 — Counting Bits
 461 — Hamming Distance
 
🎯 My Learning Order

Arrays
   ↓
Hashing
   ↓
Two Pointers
   ↓
Sliding Window
   ↓
Prefix Sum
   ↓
Binary Search
   ↓
Linked List
   ↓
Stack
   ↓
Queue
   ↓
Heap
   ↓
Intervals
   ↓
Trees
   ↓
Graphs
   ↓
Backtracking
   ↓
Greedy
   ↓
Dynamic Programming
   ↓
Advanced Topics


⭐ Golden Rule

For every LeetCode problem, write down:

1. What is the pattern?
2. Why does this pattern apply?
3. What is the brute-force solution?
4. What is the optimized solution?
5. Time Complexity?
6. Space Complexity?
7. What other problems use the same idea?

Goal: Solve patterns, not individual problems.

Progress
Easy       ⬜⬜⬜⬜⬜
Medium     ⬜⬜⬜⬜⬜
Hard       ⬜⬜⬜⬜⬜


Patterns   0 / 23
Problems   0 / 100+

This repository is intended as a pattern-based LeetCode learning journey, with solutions, algorithms, complexity analysis, and notes for each problem.
