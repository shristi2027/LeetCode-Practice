# 0001 - Two Sum

## Problem Description
Given an array of integers `nums` and an integer `target`, return indices of the two numbers such that they add up to `target`.

## My Approach
I used a Hash Map (Python dictionary) to store the values we've already seen. This allows us to check if the "complement" (target minus current number) exists in O(1) time.

- Time Complexity: O(n)
- Space Complexity: O(n)
