#Easy
Given an array of integers `nums` and an integer `target`, return _indices of the two numbers such that they add up to `target`_.

You may assume that each input would have **_exactly_ one solution**, and you may not use the _same_ element twice.

You can return the answer in any order.

**Example 1:**

**Input:** nums = [2,7,11,15], target = 9
**Output:** [0,1]
**Explanation:** Because nums[0] + nums[1] == 9, we return [0, 1].

**Example 2:**

**Input:** nums = [3,2,4], target = 6
**Output:** [1,2]

**Example 3:**

**Input:** nums = [3,3], target = 6
**Output:** [0,1]

**Constraints:**

- `2 <= nums.length <= 104`
- `-109 <= nums[i] <= 109`
- `-109 <= target <= 109`
- **Only one valid answer exist**


# Solution
```
class Solution(object):
    def twoSum(self, nums, target):
		dict={}
		for i,n in enumerate(nums):
			diff=n-target
			if diff in dict:
				return [dict[diff],i]
			dict[n]=i

```
# Explanation
The solution uses the concept of #Hashmaps
- A hashmap is used where keys are the number from nums and 
  values are their indices
  This is so that numbers can be searched in O(1) complexity
- for each num in the nums list, it is subtracted from the target 
- if the difference exists in the hashmap dict, then the current number and dict[diff] is returned as a list
- if the difference is not present, the number itself is stored in the dict for future checking
![[Two Sum.png]]