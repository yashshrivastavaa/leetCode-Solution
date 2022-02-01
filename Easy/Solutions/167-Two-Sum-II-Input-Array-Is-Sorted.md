#### [Click here to see the question](https://leetcode.com/problems/two-sum-ii-input-array-is-sorted/)

## Java

```Java
class Solution {
    public int[] twoSum(int[] numbers, int target) {
        int start = 0, end = numbers.length-1;
        int[] ans = {-1,-1};
        while(start<=end){
            if(numbers[start]+numbers[end]>target){
                end = end -1;
            }else if(numbers[start]+numbers[end]<target){
                start = start +1;
            }else if(numbers[start]+numbers[end]==target){
                ans[0] = start + 1;
                ans[1] = end + 1;
                return ans;
            }
        }
        return ans;
    }
}
```
