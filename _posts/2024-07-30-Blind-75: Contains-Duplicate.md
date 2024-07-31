https://leetcode.com/problems/two-sum/description/

```
class Solution:
    def containsDuplicate(self, nums: List[int]) -> bool:
        hashset = set()
        for num in nums:
            if num in hashset:
                return True
            hashset.add(num)

        return False
```

# Explanation
To check if there is a duplicate, check if we have already seen the current element by checking a hashset of previously seen elements.

Time Complexity = O(N) because we only need to iterate through `nums` once.

Space Complexity = O(N) because we only need to store ~N elements in the hashset.
