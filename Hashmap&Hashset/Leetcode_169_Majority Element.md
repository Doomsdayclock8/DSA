#Easy  #Hashmaps 
Given an array `nums` of size `n`, return _the majority element_.

The majority element is the element that appears more than `⌊n / 2⌋` times. You may assume that the majority element always exists in the array.

**Example 1:**

**Input:** nums = [3,2,3]
**Output:** 3

**Example 2:**

**Input:** nums = [2,2,1,1,1,2,2]
**Output:** 2

**Constraints:**

- `n == nums.length`
- `1 <= n <= 5 * 104`
- `-109 <= nums[i] <= 109`
# Solution



# My Solution
```
from collections import defaultdict

class Solution(object):

    def majorityElement(self, nums):

        n=len(nums)

        dict=defaultdict(int)

        for x in nums:

            dict[x]+=1

        def find_keys_by_value(dictionary, target_value):

            return [k for k, v in dictionary.items() if v == target_value]

        result = find_keys_by_value(dict, max(dict.values()))

        return result[0]
```