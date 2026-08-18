# Arrays in DSA — Complete Topic Guide

Arrays are one of the most important DSA topics. Many advanced patterns such as Sliding Window, Two Pointers, Prefix Sum, Binary Search, Dynamic Programming, Hashing, and Range Queries are built around arrays.

This roadmap is designed for **DSA + LeetCode + coding interviews**.

---

## 1. Array Basics

### Topics
- Declaration and initialization
- Indexing
- Traversal
- Updating elements
- Insertion
- Deletion
- Searching
- Length / size
- Static vs dynamic arrays
- 1D arrays
- 2D arrays

### Complexity

| Operation | Complexity |
|---|---:|
| Access | O(1) |
| Search | O(n) |
| Update | O(1) |
| Insert at end | O(1) amortized |
| Insert at beginning | O(n) |
| Delete from beginning | O(n) |

---

## 2. Array Traversal

Common operations:

- Find maximum
- Find minimum
- Sum
- Count elements
- Count even / odd
- Reverse an array
- Copy an array
- Compare arrays
- Find second largest

### Basic pattern

```cpp
for (int i = 0; i < arr.size(); i++) {
    cout << arr[i] << " ";
}
```

---

## 3. Searching

### Linear Search

Search each element one by one.

**Time:** O(n)

### Binary Search

Works on a sorted array.

**Time:** O(log n)

Important patterns:

- Basic Binary Search
- First occurrence
- Last occurrence
- Lower Bound
- Upper Bound
- Search Insert Position
- Binary Search on Answer

---

## 4. Sorting

Important sorting algorithms:

| Algorithm | Average Time |
|---|---:|
| Bubble Sort | O(n²) |
| Selection Sort | O(n²) |
| Insertion Sort | O(n²) |
| Merge Sort | O(n log n) |
| Quick Sort | O(n log n) |
| Heap Sort | O(n log n) |

C++:

```cpp
sort(arr.begin(), arr.end());
```

Important problems:

- Sort Colors
- 3Sum
- 4Sum
- Merge Intervals
- Kth Largest Element

---

## 5. Hashing + Arrays

Use hashing to store elements or their frequencies.

Common structures:

```cpp
unordered_map<int, int> freq;
unordered_set<int> st;
```

### Typical use cases

- Find duplicates
- Count frequencies
- Find pairs
- Prefix-sum + hashing
- Group elements

Important problems:

- Two Sum — #1
- Contains Duplicate — #217
- Majority Element — #169
- Subarray Sum Equals K — #560
- Longest Consecutive Sequence — #128
- Top K Frequent Elements — #347

---

## 6. Frequency Array

When values lie in a small known range, a frequency array can replace a hash map.

Example:

```cpp
vector<int> freq(1001, 0);

for (int x : arr)
    freq[x]++;
```

Useful for:

- Counting occurrences
- Duplicates
- Character frequency
- Counting Sort

---

## 7. Two Pointers

One of the most important array patterns.

Use it when:

- The array is sorted
- Looking for pairs
- Working from both ends
- Removing duplicates
- Partitioning elements

### Basic pattern

```text
left = 0
right = n - 1

while left < right:
    check condition
    move left or right
```

Important problems:

- Two Sum II
- 3Sum
- Container With Most Water
- Remove Duplicates from Sorted Array
- Move Zeroes
- Valid Palindrome

---

## 8. Sliding Window

Used mainly for **contiguous subarrays**.

### Fixed-size window

Example:

> Maximum sum of a subarray of size K.

Pattern:

```text
Create first window
Slide the window
Remove left element
Add right element
Update answer
```

### Variable-size window

```text
left = 0

for right:
    add arr[right]

    while condition is invalid:
        remove arr[left]
        left++

    update answer
```

Important problems:

- Maximum Average Subarray I — #643
- Minimum Size Subarray Sum — #209
- Maximum Consecutive Ones — #485

---

## 9. Prefix Sum

Prefix Sum is used for efficient range-sum queries.

For:

```text
arr = [2, 4, 1, 5, 3]
```

Prefix:

```text
[2, 6, 7, 12, 15]
```

Formula:

```text
prefix[i] = prefix[i - 1] + arr[i]
```

Range sum:

```text
sum(l...r) = prefix[r] - prefix[l - 1]
```

### Complexity

- Build: O(n)
- Range query: O(1)

Important problems:

- Range Sum Query
- Subarray Sum Equals K — #560
- Find Pivot Index — #724
- Contiguous Array — #525

---

## 10. Difference Array

Useful when there are many range updates.

Instead of updating every element from `l` to `r`:

```text
diff[l] += x
diff[r + 1] -= x
```

Then calculate the prefix sum of the difference array.

### Complexity

Usually:

**O(n + q)**

instead of:

**O(n × q)**

Useful for:

- Range updates
- Scheduling
- Competitive programming

---

## 11. Kadane's Algorithm

Used to find the **maximum subarray sum**.

Example:

```text
[-2,1,-3,4,-1,2,1,-5,4]
```

Answer:

```text
6
```

Core idea:

```text
current = max(arr[i], current + arr[i])
answer = max(answer, current)
```

**Time:** O(n)  
**Space:** O(1)

Important problems:

- Maximum Subarray — #53
- Maximum Circular Subarray — #918
- Maximum Product Subarray — #152

---

## 12. Subarray

A subarray must be **contiguous**.

For:

```text
[1,2,3,4]
```

Valid:

```text
[1,2]
[2,3,4]
[3]
```

Invalid:

```text
[1,3]
```

because the elements are not contiguous.

Common techniques:

- Brute Force
- Prefix Sum
- Hashing
- Sliding Window
- Kadane
- Two Pointers

---

## 13. Subsequence

A subsequence does **not** need to be contiguous.

For:

```text
[1,2,3,4]
```

Examples:

```text
[1,3]
[2,4]
[1,2,4]
```

Common techniques:

- Dynamic Programming
- Greedy
- Binary Search
- Two Pointers

Important problem:

- Longest Increasing Subsequence — #300

---

## 14. Subset

Each element can either be selected or not selected.

For an array of `n` elements:

```text
Number of subsets = 2^n
```

Common techniques:

- Backtracking
- Bit Manipulation

Important problems:

- Subsets — #78
- Subsets II — #90
- Partition Equal Subset Sum — #416

---

## 15. Binary Search on Answer

Instead of searching for an element, search for the **minimum/maximum possible answer**.

Important problems:

- Koko Eating Bananas — #875
- Capacity To Ship Packages Within D Days — #1011
- Split Array Largest Sum — #410
- Magnetic Force Between Two Balls — #1552

---

## 16. Rotated Sorted Arrays

Example:

```text
[4,5,6,7,0,1,2]
```

Important problems:

- Search in Rotated Sorted Array — #33
- Search in Rotated Sorted Array II — #81
- Find Minimum in Rotated Sorted Array — #153
- Find Minimum in Rotated Sorted Array II — #154

Main technique:

**Binary Search**

---

## 17. Merge Intervals

Usually:

1. Sort intervals.
2. Compare current interval with the previous interval.
3. Merge if they overlap.

Example:

```text
[1,3]
[2,6]
```

becomes:

```text
[1,6]
```

Important problems:

- Merge Intervals — #56
- Insert Interval — #57
- Non-overlapping Intervals — #435
- Meeting Rooms
- Meeting Rooms II

---

## 18. Matrix / 2D Array

Important concepts:

- Row traversal
- Column traversal
- Diagonal traversal
- Transpose
- Rotation
- Spiral traversal
- Matrix search
- Grid traversal

Important problems:

- Spiral Matrix — #54
- Rotate Image — #48
- Set Matrix Zeroes — #73
- Search a 2D Matrix — #74
- Number of Islands — #200

---

## 19. Matrix Rotation

For a square matrix, 90° clockwise rotation can be performed using:

```text
Transpose
+
Reverse every row
```

This gives an O(n²) in-place solution.

Important problem:

- Rotate Image — #48

---

## 20. Spiral Matrix

Traverse the matrix in:

```text
Right → Down → Left → Up
```

Maintain:

```text
top
bottom
left
right
```

Important problem:

- Spiral Matrix — #54

---

## 21. Dutch National Flag

Used to sort an array containing:

```text
0, 1, 2
```

Use three pointers:

```text
low
mid
high
```

### Complexity

- Time: O(n)
- Space: O(1)

Important problem:

- Sort Colors — #75

---

## 22. Partitioning

Partition the array based on a condition.

Examples:

```text
negative | positive
even | odd
zero | non-zero
small | large
```

Techniques:

- Two Pointers
- Dutch National Flag
- QuickSort Partition

---

## 23. Cyclic Sort

Useful when numbers are in a known range such as:

```text
1 to n
```

Place each number at its correct index.

Important problems:

- Missing Number — #268
- Find All Numbers Disappeared in an Array — #448
- Find the Duplicate Number — #287
- Set Mismatch — #645
- First Missing Positive — #41

---

## 24. Monotonic Array

An array is monotonic if it is entirely:

- Increasing, or
- Decreasing

Example:

```text
[1,2,2,3,4]
```

Important problem:

- Monotonic Array — #896

---

## 25. Monotonic Stack + Arrays

Used for:

- Next Greater Element
- Next Smaller Element
- Previous Greater Element
- Previous Smaller Element

Important problems:

- Next Greater Element
- Daily Temperatures — #739
- Largest Rectangle in Histogram — #84
- Trapping Rain Water — #42

Usually achievable in:

**O(n)** time.

---

## 26. Heap / Priority Queue + Arrays

Useful for:

- K largest
- K smallest
- Top K
- Running median
- Priority-based processing

Important problems:

- Kth Largest Element in an Array — #215
- Top K Frequent Elements — #347
- Find Median from Data Stream — #295

---

## 27. Greedy + Arrays

Many greedy problems use arrays.

Common problems:

- Best Time to Buy and Sell Stock — #121
- Jump Game — #55
- Jump Game II — #45
- Gas Station — #134
- Assign Cookies — #455
- Candy — #135

Core idea:

> Make the best valid local choice while maintaining the possibility of reaching the global optimum.

---

## 28. Dynamic Programming + Arrays

### 1D DP

Examples:

- Climbing Stairs — #70
- House Robber — #198
- Maximum Subarray — #53

Typical state:

```text
dp[i]
```

### 2D DP

Examples:

- Unique Paths — #62
- Minimum Path Sum — #64
- Longest Common Subsequence — #1143

Typical state:

```text
dp[i][j]
```

---

## 29. Prefix + Suffix Techniques

Calculate information from both directions.

Examples:

```text
prefix maximum
suffix maximum
prefix product
suffix product
```

Important problems:

- Product of Array Except Self — #238
- Trapping Rain Water — #42
- Maximum Difference

---

## 30. Product of Array Except Self

Example:

```text
Input:
[1,2,3,4]

Output:
[24,12,8,6]
```

Can be solved using:

```text
Prefix Product
+
Suffix Product
```

without division.

Problem:

**Product of Array Except Self — #238**

---

## 31. XOR + Arrays

Important XOR properties:

```text
a ^ a = 0
a ^ 0 = a
```

Therefore, XOR can identify numbers appearing an odd number of times.

Important problems:

- Single Number — #136
- Missing Number — #268
- Single Number II — #137
- Single Number III — #260
- XOR Queries of a Subarray — #1310

---

## 32. Majority Element

An element is a majority element if it appears more than:

```text
n / 2
```

times.

Solutions:

1. Hash Map
2. Sorting
3. Boyer-Moore Voting Algorithm

Boyer-Moore:

**Time:** O(n)  
**Space:** O(1)

Problem:

- Majority Element — #169

---

## 33. Randomization + Arrays

Important concepts:

- Fisher-Yates Shuffle
- Random selection
- Reservoir Sampling

Problems:

- Shuffle an Array — #384
- Random Pick Index — #398
- Random Pick with Weight — #528

---

## 34. Range Queries

When there are many queries such as:

```text
sum(l, r)
min(l, r)
max(l, r)
```

use preprocessing/data structures.

Important techniques:

- Prefix Sum
- Sparse Table
- Fenwick Tree
- Segment Tree

---

## 35. Fenwick Tree / Binary Indexed Tree

Used for:

- Dynamic prefix sums
- Range queries
- Point updates

Typical complexity:

| Operation | Complexity |
|---|---:|
| Update | O(log n) |
| Query | O(log n) |

---

## 36. Segment Tree

Useful for dynamic range queries.

Can support:

- Range Sum
- Range Minimum
- Range Maximum
- Point Update
- Range Update

Typical complexity:

```text
Build   → O(n)
Query   → O(log n)
Update  → O(log n)
```

---

## 37. 2D Prefix Sum

Used for matrix range queries.

Example:

```text
Find sum of a rectangular region
```

Important problem:

- Range Sum Query 2D — #304

---

## 38. Difference Matrix

Extension of the difference-array concept to 2D.

Useful for:

- Rectangle updates
- Grid operations
- Competitive programming

---

## 39. Coordinate Compression

Useful when array values are very large but only their relative ordering matters.

Example:

```text
10
100000000
50000000
```

Can be compressed to:

```text
10          → 0
50000000    → 1
100000000   → 2
```

Useful with:

- Fenwick Tree
- Segment Tree
- Range Queries
- Large-value arrays

---

## 40. Inversion Count

An inversion exists when:

```text
i < j
```

but:

```text
arr[i] > arr[j]
```

Example:

```text
[3,1,2]
```

Inversions:

```text
(3,1)
(3,2)
```

Answer:

```text
2
```

Efficient technique:

**Merge Sort**

Complexity:

**O(n log n)**

---

## 41. QuickSelect

Used to find:

- Kth smallest element
- Kth largest element

Average complexity:

**O(n)**

Important problem:

- Kth Largest Element in an Array — #215

---

## 42. Array as a Graph

Sometimes:

```text
nums[i]
```

represents the next node.

This allows graph/cycle techniques to be applied to arrays.

Important problem:

- Find the Duplicate Number — #287

Technique:

**Floyd's Cycle Detection**

---

# Complete Array Pattern Roadmap

```text
ARRAYS
│
├── 01. Basics
├── 02. Traversal
├── 03. Searching
│   ├── Linear Search
│   └── Binary Search
├── 04. Sorting
├── 05. Hashing
├── 06. Frequency Array
├── 07. Two Pointers
├── 08. Sliding Window
├── 09. Prefix Sum
├── 10. Difference Array
├── 11. Kadane's Algorithm
├── 12. Subarray
├── 13. Subsequence
├── 14. Subset
├── 15. Binary Search on Answer
├── 16. Rotated Array
├── 17. Merge Intervals
├── 18. Matrix / 2D Array
├── 19. Matrix Rotation
├── 20. Spiral Matrix
├── 21. Dutch National Flag
├── 22. Partitioning
├── 23. Cyclic Sort
├── 24. Monotonic Array
├── 25. Monotonic Stack
├── 26. Heap + Array
├── 27. Greedy + Array
├── 28. DP + Array
├── 29. Prefix / Suffix
├── 30. Product Array
├── 31. XOR + Array
├── 32. Majority Element
├── 33. Randomization
├── 34. Range Queries
├── 35. Fenwick Tree
├── 36. Segment Tree
├── 37. 2D Prefix Sum
├── 38. Difference Matrix
├── 39. Coordinate Compression
├── 40. Inversion Count
├── 41. QuickSelect
└── 42. Array as Graph
```

# Recommended Learning Order

For LeetCode, follow this order:

**Beginner**

1. Array Basics
2. Traversal
3. Searching
4. Sorting
5. Hashing
6. Frequency Array

**Intermediate**

7. Two Pointers
8. Sliding Window
9. Prefix Sum
10. Kadane
11. Subarray
12. Binary Search
13. Cyclic Sort
14. Matrix
15. Merge Intervals
16. Greedy

**Advanced**

17. Monotonic Stack
18. Heap + Array
19. Binary Search on Answer
20. DP + Array
21. XOR Patterns
22. Range Queries
23. Fenwick Tree
24. Segment Tree
25. Coordinate Compression
26. Inversion Count
27. QuickSelect
28. Advanced 2D techniques

---

## Goal

Before moving to the next major DSA topic, try to solve:

- **10–15 Easy array problems**
- **20–30 Medium array problems**
- **5–10 Hard array problems**

Focus on recognizing the **pattern**, not memorizing individual solutions.
