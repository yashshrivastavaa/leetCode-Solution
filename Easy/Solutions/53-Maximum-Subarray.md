#### [Click here to see the question](https://leetcode.com/problems/maximum-subarray/)

## Java

```Java
class Solution {
    public int maxSubArray(int[] nums) {
        int maxSum = Integer.MIN_VALUE;
        int currentSum = 0;
        if(nums.length == 1)
            return nums[0];
        for(int i = 0;i< nums.length;i++) {
            maxSum = Math.max(maxSum,currentSum += nums[i]);
            if(currentSum < 0) {
                currentSum = 0;
            }
        }
        return maxSum;
    }
}
```
