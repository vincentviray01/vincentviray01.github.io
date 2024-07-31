https://leetcode.com/problems/maximum-subarray/

```
class Solution:
    def maxSubArray(self, nums: List[int]) -> int:
        max_sum = nums[0]
        cur_sum = 0

        for index, num in enumerate(nums):
            cur_sum += num
            max_sum = max(max_sum, cur_sum)
            
            if cur_sum < 0:
                cur_sum = 0

        return max_sum
```

# Explanation
Keep a running sum of elements as you traverse the `nums` array and keep track of the maximum sum found.

To ensure that the sum comes from a (continuous) subarray, check if `cur_sum` is negative. If it is negative, then start a new subarray on the next element by resetting `cur_sum` to 0 to indicate an empty subarray.
