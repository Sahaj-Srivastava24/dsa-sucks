## **1. Dynamic Programming (DP) Patterns**

DP problems follow specific patterns. Identifying the pattern is key to solving them efficiently.

### **(a) 0/1 Knapsack Pattern**

- Given a set of items, each with a weight and value, find the maximum value that can be obtained while staying within a weight limit.
- **Common Questions:**
  - 0/1 Knapsack Problem
  - Subset Sum Problem
  - Partition Equal Subset Sum (Leetcode 416)
  - Target Sum (Leetcode 494)

### **(b) Unbounded Knapsack Pattern**

- Similar to 0/1 knapsack, but you can take unlimited instances of an item.
- **Common Questions:**
  - Coin Change I & II (Leetcode 322, 518)
  - Rod Cutting Problem
  - Combination Sum IV (Leetcode 377)

### **(c) Fibonacci Sequence**

- Problems that require breaking a problem into smaller overlapping subproblems.
- **Common Questions:**
  - Fibonacci Number (Leetcode 509)
  - Climbing Stairs (Leetcode 70)
  - House Robber I & II (Leetcode 198, 213)
  - Decode Ways (Leetcode 91)
  - Jump Game II (Leetcode 45)

### **(d) Longest Common Subsequence (LCS)**

- Find the longest common sequence between two strings or variations of it.
- **Common Questions:**
  - Longest Common Subsequence (Leetcode 1143)
  - Edit Distance (Leetcode 72)
  - Longest Palindromic Subsequence (Leetcode 516)
  - Minimum Insertions to Make String a Palindrome (Leetcode 1312)

### **(e) Matrix Chain Multiplication**

- Problems where order of operations affects the result.
- **Common Questions:**
  - Matrix Chain Multiplication
  - Burst Balloons (Leetcode 312)
  - Palindrome Partitioning II (Leetcode 132)

### **(f) Subsequence and Substring Problems**

- Find the longest increasing, decreasing, or other variations of subsequences.
- **Common Questions:**
  - Longest Increasing Subsequence (Leetcode 300)
  - Russian Doll Envelopes (Leetcode 354)
  - Number of Longest Increasing Subsequences (Leetcode 673)

### **(g) Partition DP**

- Problems that involve breaking an array or string into partitions and finding the best result.
- **Common Questions:**
  - Palindrome Partitioning II (Leetcode 132)
  - Partition Array for Maximum Sum (Leetcode 1043)

### **(h) DP on Grids**

- Problems that involve moving on a 2D grid while optimizing cost.
- **Common Questions:**
  - Unique Paths I & II (Leetcode 62, 63)
  - Minimum Path Sum (Leetcode 64)
  - Cherry Pickup (Leetcode 741)

### **(i) Bitmask DP**

- Used when we need to track subsets efficiently.
- **Common Questions:**
  - Traveling Salesman Problem (TSP)
  - Minimum XOR Sum of Two Arrays (Leetcode 1879)
  - Maximum Students Taking Exam (Leetcode 1349)

---

## **2. Dynamic Programming Approach**

For each problem, follow these steps:

1. **Define the state:**

   - Identify what needs to be stored in `dp[i]`.
   - Example: `dp[i]` represents the max profit, min cost, or count at step `i`.

2. **Formulate the recurrence relation:**

   - Find a relation using smaller subproblems.
   - Example:
     - Fibonacci: `dp[i] = dp[i-1] + dp[i-2]`
     - Knapsack: `dp[i][w] = max(dp[i-1][w], value[i] + dp[i-1][w-weight[i]])`

3. **Base case initialization:**

   - Example:
     - Fibonacci: `dp[0] = 0, dp[1] = 1`
     - Knapsack: `dp[i][0] = 0` (0 capacity means 0 value)

4. **Iterate and compute the result:**

   - Use recursion + memoization (top-down) or iteration (bottom-up).

5. **Optimize space if possible:**
   - Convert 2D DP to 1D if only the previous state is needed.

---

## **3. Famous DP Problems & Solutions**

### **Basic DP**

| **Problem**      | **Pattern**        | **Leetcode** |
| ---------------- | ------------------ | ------------ |
| Fibonacci Number | Fibonacci Sequence | 509          |
| Climbing Stairs  | Fibonacci Sequence | 70           |
| House Robber     | Knapsack           | 198          |
| House Robber II  | Knapsack           | 213          |
| Jump Game        | Greedy / DP        | 55           |

### **Knapsack Variants**

| **Problem**                | **Pattern**        | **Leetcode** |
| -------------------------- | ------------------ | ------------ |
| 0/1 Knapsack               | 0/1 Knapsack       | -            |
| Partition Equal Subset Sum | 0/1 Knapsack       | 416          |
| Target Sum                 | 0/1 Knapsack       | 494          |
| Coin Change                | Unbounded Knapsack | 322          |
| Coin Change II             | Unbounded Knapsack | 518          |

### **String & Subsequence DP**

| **Problem**                | **Pattern**         | **Leetcode** |
| -------------------------- | ------------------- | ------------ |
| Longest Common Subsequence | LCS                 | 1143         |
| Edit Distance              | LCS variation       | 72           |
| Longest Palindromic Subseq | LCS variation       | 516          |
| Decode Ways                | Fibonacci variation | 91           |

### **Grid-Based DP**

| **Problem**      | **Pattern**              | **Leetcode** |
| ---------------- | ------------------------ | ------------ |
| Unique Paths     | Grid DP                  | 62           |
| Unique Paths II  | Grid DP (With obstacles) | 63           |
| Minimum Path Sum | Grid DP                  | 64           |
| Cherry Pickup    | Advanced Grid DP         | 741          |

### **Partition & Merging DP**

| **Problem**                 | **Pattern**                 | **Leetcode** |
| --------------------------- | --------------------------- | ------------ |
| Palindrome Partitioning II  | Partition DP                | 132          |
| Partition Array for Max Sum | Partition DP                | 1043         |
| Burst Balloons              | Matrix Chain Multiplication | 312          |

### **Bitmask DP**

| **Problem**                      | **Pattern** | **Leetcode** |
| -------------------------------- | ----------- | ------------ |
| Traveling Salesman Problem (TSP) | Bitmask DP  | -            |
| Minimum XOR Sum of Two Arrays    | Bitmask DP  | 1879         |

---

## **4. Space Optimization in DP**

Some problems can be optimized from `O(n^2)` to `O(n)` or `O(1)`, like:

- Fibonacci (`O(n) → O(1)`)
- Knapsack (`O(nW) → O(W)`)
- Grid DP (`O(m*n) → O(n)` by keeping only the last row)

---

## **5. How to Practice?**

1. Start with **Easy DP** (Climbing Stairs, Fibonacci, House Robber).
2. Move to **Knapsack Problems** (0/1 Knapsack, Coin Change).
3. Try **String Problems** (LCS, Edit Distance).
4. Work on **Grid DP** (Unique Paths, Minimum Path Sum).
5. Finally, attempt **Advanced DP** (Palindrome Partitioning, TSP, Burst Balloons).
