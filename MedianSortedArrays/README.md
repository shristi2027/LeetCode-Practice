# 0004 - Median of Two Sorted Arrays

## Difficulty: Hard

## Problem Description
Given two sorted arrays `nums1` and `nums2` of size `m` and `n` respectively, return the median of the two sorted arrays.
**Constraint:** The overall run time complexity must be $O(\log (m+n))$.

## My Approach: Binary Search on Partitions
The "brute force" way to solve this is to merge the two arrays, but that takes $O(m+n)$ time. To achieve **Logarithmic time**, we must use a modified **Binary Search**.

### The Logic:
1. **Partitioning:** Instead of merging, I "cut" both arrays at a specific point so that the total number of elements on the left side equals the total on the right.
2. **Binary Search:** I perform the binary search on the **smaller array** to find the perfect partition point where:
   - `maxLeftX <= minRightY`
   - `maxLeftY <= minRightX`
3. **Handling Edges:** I used `float('-inf')` and `float('inf')` to handle cases where a partition falls at the very beginning or end of an array.
4. **Median Calculation:** - If total elements are **odd**, the median is the maximum of the left partition.
   - If total elements are **even**, the median is the average of the maximum of the left and the minimum of the right.

### Complexity Analysis
- **Time Complexity:** $O(\log(\min(m, n)))$ — We only binary search through the shorter array.
- **Space Complexity:** $O(1)$ — No extra arrays are created; we only use a few pointer variables.
