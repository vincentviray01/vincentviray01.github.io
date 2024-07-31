https://leetcode.com/problems/best-time-to-buy-and-sell-stock/description/

```
class Solution:
    def maxProfit(self, prices: List[int]) -> int:
        maxProfit = 0
        maxPrice = None

        for x in range(len(prices) - 1, -1, -1):
            if maxPrice is None:
                maxPrice = prices[x]
            else:
                maxProfit = max(maxProfit, maxPrice - prices[x])
                maxPrice = max(maxPrice, prices[x])
        return maxProfit
```

# Explanation
Iterate through the prices in reverse order and keep track of the maximum price found so far. 

This keeps track of the maximum possible sell price (since we start from the right side) for each index we iterate through. 

Then simply compare the current element with the maximum sell price and keep track of the greatest difference.

Time Complexity is O(N) because you only need to loop through the List a single time.

Space Complexity is O(1) because you only need two variables to hold the maximum sell price and max profit.

# Alternate Solution
2 pointers, left and right.

Left is the buy price. Right is the sell price.

If the buy price is greater than the sell price, then move the left pointer to the right pointer in order to ensure that the buy price is the lowest it could be.

If the sell price is greater or equal to the buy price, then move the right pointer to the right by one in order to try and find an even higher sell price for more profit.

Every iteration keep track of the maximum profit.
