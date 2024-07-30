https://leetcode.com/problems/two-sum/description/

```
class Solution:
    def twoSum(self, nums: List[int], target: int) -> List[int]:
        # Time Complexity = O(N)
        # Space Complexity = O(N)
        hashmap = {}
        for index, num in enumerate(nums):
            difference = target - num
            if difference in hashmap:
                return [index, hashmap[difference]]
            hashmap[num] = index
```

# Explanation
For each element, check if `difference = target - element` is in the list by using a hashmap with O(1) lookup.

Only a single loop is needed because adding elements to the hashmap after checking if the current element is part of the solution avoids counting the same index twice. 

Additionally, since there is guaranteed to be on solution to this problem, by the time the higher-valued index of the solution is reached, the lower-valued index of the solution will already be in the hashmap and the solution will then be returned.

Time Complexity is O(N) because you only need to loop through the List a single time.

Space Complexity is O(N) because you only need a single Hashmap that at the most would hold ~N elements.
