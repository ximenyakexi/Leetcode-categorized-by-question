**1. Add Two Numbers**

You are given two non-empty linked lists representing two non-negative integers. The digits are stored in

reverse order and each of their nodes contain a single digit. Add the two numbers and return it as a linked

list.

You may assume the two numbers do not contain any leading zero, except the number 0 itself.

Example:

Input: [2 -> 4 -> 3] + [5 -> 6 -> 4]

Output: 7 -> 0 -> 8

Explanation: 342 + 465 = 807.

**Method 1. Brutal force**

```
# Definition for singly-linked list.
# class ListNode:
#     def __init__(self, x):
#         self.val = x
#         self.next = None

class Solution:
    def addTwoNumbers(self, l1: ListNode, l2: ListNode) -> ListNode:
```
Time complexity: O(n^2), Space complexity: O(1)

