# 0003 - Longest Substring Without Repeating Characters

## Problem Description
Given a string `s`, find the length of the longest substring without duplicate characters.

## My Approach
I implemented the **Sliding Window** technique using two pointers (`left` and `right`) and a **Set** to keep track of unique characters.
- The `right` pointer expands the window.
- If a duplicate is found, the `left` pointer moves forward (shrinking the window) until the duplicate is removed from the set.
- The maximum window size during this process is our answer.

- **Time Complexity:** $O(n)$
- **Space Complexity:** $O(min(m, n))$
