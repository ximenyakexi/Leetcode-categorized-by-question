**1. Two Sum**

Given an array of integers, return indices of the two numbers such that they add up to a specific target.

You may assume that each input would have exactly one solution, and you may not use the same element twice.

Example:

Given nums = [2, 7, 11, 15], target = 9,

Because nums[0] + nums[1] = 2 + 7 = 9,

return [0, 1].

**Method 1. Brutal force**

```
class Solution:
    def twoSum(self, nums: List[int], target: int) -> List[int]:
        for i in range(len(nums)):
            for j in range(i+1, len(nums)):
                if nums[i] + nums[j] == target:
                    return [i, j]  
```
Time complexity: O(n^2), Space complexity: O(1)

**Method 2. Dictionary(Hashmap)**

Look-up in dictionary is O(1). This saves searching time. However, the prerequisite is that no two elements are the same.

```
class Solution:
    def twoSum(self, nums: List[int], target: int) -> List[int]:
        map = {}
        for i in range(len(nums)):
            complement = target - nums[i]
            if complement in map:
                return [map[complement], i]
            map[nums[i]] = i
    
```
Time complexity: O(n), Space complexity: O(n)
