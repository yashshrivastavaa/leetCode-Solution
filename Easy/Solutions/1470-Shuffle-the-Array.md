##### [Click Here To See The Question](https://leetcode.com/problems/shuffle-the-array/)

## Java
```Java
class Solution {
    public int[] shuffle(int[] nums, int n) {
        int[] arr = new int[n*2];
        int i = 0;
        int j = n;
        int count = 0;
        while(i<n){
            arr[count]=nums[i];
            i++;
            count++;
            arr[count]=nums[j];
            j++;
            count++;
        }
        return arr;
    }
}
```

## C++ 
```cpp
class Solution {
public:
    vector<int> shuffle(vector<int>& nums, int n) {
        vector<int> res;
        for(int i=0, j=n; j<nums.size(); i++, j++){
            res.push_back(nums[i]);
            res.push_back(nums[j]);
        } return res;
    }
};
```
