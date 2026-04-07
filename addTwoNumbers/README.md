# 0002 - Add Two Numbers

## Problem Description
You are given two non-empty linked lists representing two non-negative integers. The digits are stored in reverse order, and each of their nodes contains a single digit. Add the two numbers and return the sum as a linked list.

## My Approach
I treated this like elementary school addition. I iterated through both linked lists simultaneously, adding the values along with a `carry` variable. 
- If the sum of two nodes is 10 or more, the `1` is carried over to the next pair of nodes.
- I used a **Dummy Node** to simplify the creation of the resulting linked list.

- **Time Complexity:** $O(\max(m, n))$
- **Space Complexity:** $O(\max(m, n))$
