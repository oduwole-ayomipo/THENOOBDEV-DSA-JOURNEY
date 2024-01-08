# Two Sum - LeetCode Challenge

## Level - Easy

### Question

Given an array of integers nums and an integer target, return indices of the two numbers such that they add up to target.

    - You may assume that each input would have exactly one solution, and you may not use the same element twice.

    - You can return the answer in any order.

#### Example 1:

Input: nums = [2,7,11,15], target = 9
Output: [0,1]
Explanation: Because nums[0] + nums[1] == 9, we return [0, 1].

#### Example 2:

Input: nums = [3,2,4], target = 6
Output: [1,2]

#### Example 3:

Input: nums = [3,3], target = 6
Output: [0,1]

#### Constraints:

2 <= nums.length <= 10^4
-10^9 <= nums[i] <= 10^9
-10^9 <= target <= 10^9
Only one valid answer exists.

### Solution

#### Step 1: Understand the problem

- We are given an array of integers nums and an integer target.
- We need to find and return the indices of two numbers in the array such that they add up to the given target.
- That is, if nums = [3,2,5] and target is 7 => return [1,2]: Because 2+5 = 7

#### Step 2: Plan the Solution

- Iterate through the array and, for each element i, we are gonna check if there exists another element in the array such that their sum equals the target.

- Since we are guaranteed that there is exactly one solution, we can stop as soon as we find a pair.

#### Step 3: Pseudocode

- Use nested loops to iterate through each pair of elements.
- Check if the sum of the current pair equals the target.
- If it does, return the index of the two elements.

#### Step 4: Code Implementation

```js
function twoSum(nums, target) {
  for (var i = 0; i <= nums.length; i++) {
    for (j = i + 1; j <= nums.length; j++) {
      if (nums[i] + nums[j] == target) {
        return [i, j];
      }
    }
  }
}
```

#### Step 5: Test the solution

```js
// Test cases
console.log(twoSum([2, 7, 11, 15], 9)); // Output: [0, 1]
console.log(twoSum([3, 2, 4], 6)); //Output: [1, 2]
console.log(twoSum([3, 3], 6)); // Output: [0, 1]
```

#### Step 6: Analyze Complexity

**Time Complexity:** The time complexity of this solution is O(n^2) due to the nested loops, where n is the length of the array.

**Explanation:** There are two loops, the first loop has a complexity of o(n), because time spent to check each element in the array is highly depending on th length of the array. The the second loop also has a time complexity of o(n). Merging both of them gives us o(n^2)

**Space Complexity:** The space complexity is O(1) as we are not using any additional data structures.

#### Conclusion:

You may be wondering that this solution is not optimal, of course we can come up with an algorithm that is less than O(n^2) time complexity by using hashmaps. But that is beyond this scope of file. Do visit the hashmap folder to see an optimal solution!
