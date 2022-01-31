##### [Click Here To See The Question](https://leetcode.com/problems/build-array-from-permutation/)

## Java
```Java
class Solution {
    public int[] buildArray(int[] nums) {
        final int n = nums.length;
        int [] arr= new int[n];
        for(int i = 0;i<n;i++)
            arr[i]= nums[nums[i]];

    return arr;
    }
}
```

## Python
```Python
class Solution:
    def buildArray(self, nums: List[int]) -> List[int]:
        n = len(nums)
        for i in range(0, len(nums)):
            nums[i]=nums[i]+(n*(nums[nums[i]]%n))

        for i in range(0, len(nums)):
            nums[i] = int(nums[i]/n)

        return nums
```

## C++
```cpp
class Solution {
public:
    vector<int> buildArray(vector<int>& nums) {
        int n=nums.size();
        for(int i=0;i<n;i++){
            nums[i]=nums[i]+(n*(nums[nums[i]]%n));
        }
        for(int i=0;i<n;i++){
            nums[i]/=n;
        }
        return nums;
    }
};
```
