# 121. Best Time to Buy and Sell Stock

### Level - Easy

## Question

    - You are given an array prices where prices[i] is the price of a given stock on the ith day.

    - You want to maximize your profit by choosing a single day to buy one stock and choosing a different day in the future to sell that stock.

    - Return the maximum profit you can achieve from this transaction. If you cannot achieve any profit, return 0.

### Example 1:

Input: prices = [7,1,5,3,6,4]
Output: 5
Explanation: Buy on day 2 (price = 1) and sell on day 5 (price = 6), profit = 6-1 = 5.
Note that buying on day 2 and selling on day 1 is not allowed because you must buy before you sell.

### Example 2:

Input: prices = [7,6,4,3,1]
Output: 0
Explanation: In this case, no transactions are done and the max profit = 0.

### Solution

#### Step 1: Understand the problem

We are given an array of stock prices,

    - we aim to find the maximum profit that can be obtained by buying and selling one stock. Keeping in mind that:

    - we can only sell the stock after buying,

    - and we must maximuze profit.

#### Step 2: Plan the problem

We could approach this problem by, iterating through the array, while keepting track of the minimum buying price and updating the maximum profit when a higher selling price is found. To do this, we can:

    - check if the array items is greater than 1 (inclusive)

    - Initialize variables to store the minimum and maximum price, this would be the basis of our comparison.

    - Iterate through the price in price

    - If the minimum buying price is higher than the current price, update the value of the minimum price

    - calculate the potential profit if hte current price allows for a better profit

    - Update the maximum profit

#### Step 3: Pseudocode

```plaintext
function maxProfit(prices):
    if length of prices <= 1:
        return 0  // Not enough days to make a profit

    minPrice = prices[0]
    maxProfit = 0

    for i from 1 to length of prices - 1:
        if prices[i] < minPrice:
            minPrice = prices[i]  // Update the minimum buying price
        else:
            maxProfit = max(maxProfit, prices[i] - minPrice)  // Update the maximum profit

    return maxProfit
```

#### Step 3: Code the solution

```js
var maxProfit = function (prices) {
  if (prices.length <= 1) {
    return 0;
  }

  let minPrice = prices[0];
  let maxProfit = 0;

  for (let i = 1; i < prices.length; i++) {
    if (prices[i] < minPrice) {
      minPrice = prices[i];
    } else {
      maxProfit = Math.max(maxProfit, prices[i] - minPrice);
    }
  }

  return maxProfit;
};
```

#### Step 3: Test the solution:

```js
console.log(maxProfit([7, 1, 5, 3, 6, 4])); // Expected output: 5
console.log(maxProfit([7, 6, 4, 3, 1])); // Expected output: 0
```

#### Step 6: Analyze Complexity

**Time Complexity:** This approach has a time complexity of O(n), where n is the length of the prices array, as it only iterates through the array once.

**Space Complexity:** The space complexity is O(1) as we are not creating any additional data structures.
