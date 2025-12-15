# Running Sum of 1D Array  
**LeetCode 1480**

---

## Intuition
To calculate the running sum, we need the total of elements up to the current index.
Instead of calculating the sum again and again, we keep a variable that stores the
sum so far and update it while traversing the array.

---

## Approach
1. Initialize a variable `current_sum` as 0
2. Traverse the array from index 0 to the end
3. Add the current element to `current_sum`
4. Update the array at that index with `current_sum`
5. Return the updated array

---

## Complexity
- **Time Complexity:** O(n)  
  (We traverse the array once)

- **Space Complexity:** O(1)  
  (No extra space is used)

---

## Code (Python)

```python
class Solution(object):
    def runningSum(self, nums):
        current_sum = 0
        for i in range(len(nums)):
            current_sum += nums[i]
            nums[i] = current_sum
        return nums
