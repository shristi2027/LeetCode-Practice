# 0005 - Longest Palindromic Substring

## Problem Description
Given a string `s`, return the longest palindromic substring in `s`.

## My Approach
I used the **Expand Around Center** strategy. 
- For every character in the string, I treated it as the center of a potential palindrome.
- I expanded outwards as long as the characters matched.
- I checked for both **Odd-length** centers (e.g., "aba") and **Even-length** centers (e.g., "baab") to ensure all possible palindromes were captured.

- **Time Complexity:** $O(n^2)$
- **Space Complexity:** $O(1)$
