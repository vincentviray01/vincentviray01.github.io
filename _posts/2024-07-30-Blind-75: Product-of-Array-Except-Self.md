https://leetcode.com/problems/product-of-array-except-self/

```
class Solution:
    def productExceptSelf(self, nums: List[int]) -> List[int]:
        left = [1] * len(nums)
        right = [1] * len(nums)
        answer = []

        for index in range(1, len(nums)):
            left[index] = left[index-1] * nums[index-1]
        
        for index in range(len(nums)-2, -1, -1):
            right[index] = right[index+1] * nums[index+1]

        for index in range(len(nums)):
            answer.append(left[index] * right[index])

        return answer
        
```

# Explanation
Use a `left` array to keep track of the product of elements to the left of the current element.

Use a `right` array to keep track of the product of elements to the right of the current element.

Multiply the corresponding elements of the `left` and `right` arrays to get the product of entire array without multiplying the element at the current index of the original `nums` array.

Time Complexity = O(N) because this algorithm only needs to iterate the `nums` array three times.

Space Complexity = O(N) because this algorithm only needs two extra Lists that are the same size of `nums`. We don't need an `answer` variable as we could change the original `nums` array instead after computing `left` and `right`.
